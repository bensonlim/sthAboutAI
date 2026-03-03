# MtLocatorRpcClient 方法文档

## 概述

MtLocatorRpcClient 是一个跨服务客户端，用于查询库位相关的信息，包括库位基本信息、库位关系、库位站点分配、用户库位权限等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtLocatorRpcClient** | `org.tarzan.boot.model.client.MtLocatorRpcClient` |
| **MtModLocatorBaseVO** | `org.tarzan.model.domain.vo.MtModLocatorBaseVO` |
| **MtModLocatorVO** | `org.tarzan.model.domain.vo.MtModLocatorVO` |
| **MtModLocatorVO1** | `org.tarzan.model.domain.vo.MtModLocatorVO1` |
| **MtModLocatorRelVO** | `org.tarzan.model.domain.vo.MtModLocatorRelVO` |
| **MtModLocatorRelVO2** | `org.tarzan.model.domain.vo.MtModLocatorRelVO2` |
| **MtModLocatorSiteAssignVO** | `org.tarzan.model.domain.vo.MtModLocatorSiteAssignVO` |
| **MtModLocatorSiteAssignVO1** | `org.tarzan.model.domain.vo.MtModLocatorSiteAssignVO1` |
| **MtModInvLocatorVO** | `org.tarzan.model.domain.vo.MtModInvLocatorVO` |
| **MtUserLocatorPermissionVO** | `org.tarzan.model.domain.vo.MtUserLocatorPermissionVO` |

## 方法列表

### 1. locatorBasicPropertyGet

**用途**：获取单个库位基本信息

**参数**：
- tenantId：租户ID
- locatorId：库位ID

**返回值**：MtModLocatorBaseVO - 库位基本信息

### 2. locatorBasicPropertyBatchGet

**用途**：批量获取库位基本信息

**参数**：
- tenantId：租户ID
- locatorIds：库位ID列表

**返回值**：List<MtModLocatorBaseVO> - 库位基本信息列表

### 3. codeLimitLocatorBasicBatchQuery

**用途**：根据编码批量查询库位基本信息

**参数**：
- tenantId：租户ID
- locatorCodes：库位编码列表

**返回值**：List<MtModLocatorBaseVO> - 库位基本信息列表

### 4. locatorLimitRelatedLocatorQuery

**用途**：查询库位相关库位

**参数**：
- tenantId：租户ID
- queryVO：库位关系查询对象

**返回值**：List<MtModLocatorVO1> - 相关库位列表

### 5. locatorLimitAllRelatedLocatorQuery

**用途**：查询库位所有相关库位

**参数**：
- tenantId：租户ID
- queryVO：库位关系查询对象

**返回值**：List<MtModLocatorVO> - 所有相关库位列表

### 6. locatorSiteAssignPropertyGet

**用途**：获取单个库位站点分配信息

**参数**：
- tenantId：租户ID
- locatorId：库位ID

**返回值**：MtModLocatorSiteAssignVO - 库位站点分配信息

### 7. locatorSiteAssignPropertyBatchGet

**用途**：批量获取库位站点分配信息

**参数**：
- tenantId：租户ID
- locatorIds：库位ID列表

**返回值**：List<MtModLocatorSiteAssignVO> - 库位站点分配信息列表

### 8. locatorLimitLocatorSiteAssignQuery

**用途**：查询库位站点分配

**参数**：
- tenantId：租户ID
- queryVO：库位站点分配查询对象

**返回值**：List<MtModLocatorSiteAssignVO1> - 库位站点分配列表

### 9. userLocatorPermissionValidate

**用途**：验证用户库位权限

**参数**：
- tenantId：租户ID
- queryVO：用户库位权限验证对象

**返回值**：MtUserLocatorPermissionVO - 用户库位权限信息

### 10. userLocatorPermissionBatchValidate

**用途**：批量验证用户库位权限

**参数**：
- tenantId：租户ID
- queryVO：用户库位权限验证对象列表

**返回值**：List<MtUserLocatorPermissionVO> - 用户库位权限信息列表

### 11. locatorLimitInvLocatorQuery

**用途**：查询库存库位

**参数**：
- tenantId：租户ID
- queryVO：库存库位查询对象

**返回值**：List<MtModInvLocatorVO> - 库存库位列表

### 12. locatorLimitLocatorRelQuery

**用途**：查询库位关系

**参数**：
- tenantId：租户ID
- queryVO：库位关系查询对象

**返回值**：List<MtModLocatorRelVO> - 库位关系列表

## 使用示例

### 示例1：批量获取库位基本信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<Long> locatorIds = Arrays.asList(1L, 2L, 3L);
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.locatorBasicPropertyBatchGet(tenantId, locatorIds);
Map<Long, String> locatorCodeMap = locators.stream()
    .collect(Collectors.toMap(MtModLocatorBaseVO::getLocatorId, MtModLocatorBaseVO::getLocatorCode));
```

### 示例2：根据编码批量查询库位基本信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<String> locatorCodes = Arrays.asList("LOC001", "LOC002", "LOC003");
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.codeLimitLocatorBasicBatchQuery(tenantId, locatorCodes);
Map<String, Long> locatorIdMap = locators.stream()
    .collect(Collectors.toMap(MtModLocatorBaseVO::getLocatorCode, MtModLocatorBaseVO::getLocatorId));
```

### 示例3：查询库位相关库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorVO1;

MtModLocatorVO1 queryVO = new MtModLocatorVO1();
queryVO.setLocatorId(locatorId);
queryVO.setRelatedLocatorType("PARENT");
List<MtModLocatorVO1> relatedLocators = mtLocatorRpcClient.locatorLimitRelatedLocatorQuery(tenantId, queryVO);
```

### 示例4：验证用户库位权限

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtUserLocatorPermissionVO;

MtUserLocatorPermissionValidateVO validateVO = new MtUserLocatorPermissionValidateVO();
validateVO.setUserId(userId);
validateVO.setLocatorId(locatorId);
validateVO.setPermissionType("OPERATE");
MtUserLocatorPermissionVO permission = mtLocatorRpcClient.userLocatorPermissionValidate(tenantId, validateVO);
```

### 示例5：查询库位站点分配

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorSiteAssignVO;

List<Long> locatorIds = Arrays.asList(1L, 2L, 3L);
List<MtModLocatorSiteAssignVO> siteAssigns = mtLocatorRpcClient.locatorSiteAssignPropertyBatchGet(tenantId, locatorIds);
Map<Long, Long> siteIdMap = siteAssigns.stream()
    .collect(Collectors.toMap(MtModLocatorSiteAssignVO::getLocatorId, MtModLocatorSiteAssignVO::getSiteId));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 库位关系查询需要正确设置查询对象的参数，以获取正确的库位关系信息
4. 用户库位权限验证需要提供用户ID和库位ID，以及权限类型
5. 不同方法返回的对象类型不同，使用时需要注意类型转换
6. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量