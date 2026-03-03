# MtAreaRpcClient 方法文档

## 概述

MtAreaRpcClient 是一个跨服务客户端，用于查询区域相关的信息，包括区域基本信息、区域采购信息、区域调度信息等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtAreaRpcClient** | `org.tarzan.boot.model.client.MtAreaRpcClient` |
| **MtModAreaBaseVO** | `org.tarzan.model.domain.vo.MtModAreaBaseVO` |
| **MtModAreaPurchaseBaseVO** | `org.tarzan.model.domain.vo.MtModAreaPurchaseBaseVO` |
| **MtModAreaScheduleBaseVO** | `org.tarzan.model.domain.vo.MtModAreaScheduleBaseVO` |
| **MtModAreaVO1** | `org.tarzan.model.domain.vo.MtModAreaVO1` |
| **MtModAreaVO4** | `org.tarzan.model.domain.vo.MtModAreaVO4` |

## 方法列表

### 1. areaBasicPropertyGet

**用途**：获取单个区域基本信息

**参数**：
- tenantId：租户ID
- areaId：区域ID

**返回值**：MtModAreaBaseVO - 区域基本信息

### 2. areaBasicPropertyBatchGet

**用途**：批量获取区域基本信息

**参数**：
- tenantId：租户ID
- areaIds：区域ID列表

**返回值**：List<MtModAreaBaseVO> - 区域基本信息列表

### 3. codeLimitAreaBasicBatchQuery

**用途**：根据编码批量查询区域基本信息

**参数**：
- tenantId：租户ID
- areaCodes：区域编码列表

**返回值**：List<MtModAreaBaseVO> - 区域基本信息列表

### 4. areaPurchasePropertyGet

**用途**：获取单个区域采购信息

**参数**：
- tenantId：租户ID
- areaId：区域ID

**返回值**：MtModAreaPurchaseBaseVO - 区域采购信息

### 5. areaPurchasePropertyBatchGet

**用途**：批量获取区域采购信息

**参数**：
- tenantId：租户ID
- areaIds：区域ID列表

**返回值**：List<MtModAreaPurchaseBaseVO> - 区域采购信息列表

### 6. areaSchedulePropertyGet

**用途**：获取单个区域调度信息

**参数**：
- tenantId：租户ID
- areaId：区域ID

**返回值**：MtModAreaScheduleBaseVO - 区域调度信息

### 7. areaSchedulePropertyBatchGet

**用途**：批量获取区域调度信息

**参数**：
- tenantId：租户ID
- areaIds：区域ID列表

**返回值**：List<MtModAreaScheduleBaseVO> - 区域调度信息列表

### 8. areaLimitAllRelatedAreaQuery

**用途**：查询区域所有相关区域

**参数**：
- tenantId：租户ID
- queryVO：区域关系查询对象

**返回值**：List<MtModAreaVO4> - 相关区域列表

### 9. areaLimitRelatedAreaQuery

**用途**：查询区域相关区域

**参数**：
- tenantId：租户ID
- queryVO：区域关系查询对象

**返回值**：List<MtModAreaVO1> - 相关区域列表

## 使用示例

### 示例1：批量获取区域基本信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;

List<Long> areaIds = Arrays.asList(1L, 2L, 3L);
List<MtModAreaBaseVO> areas = mtAreaRpcClient.areaBasicPropertyBatchGet(tenantId, areaIds);
Map<Long, String> areaCodeMap = areas.stream()
    .collect(Collectors.toMap(MtModAreaBaseVO::getAreaId, MtModAreaBaseVO::getAreaCode));
```

### 示例2：根据编码批量查询区域基本信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;

List<String> areaCodes = Arrays.asList("AREA001", "AREA002", "AREA003");
List<MtModAreaBaseVO> areas = mtAreaRpcClient.codeLimitAreaBasicBatchQuery(tenantId, areaCodes);
Map<String, Long> areaIdMap = areas.stream()
    .collect(Collectors.toMap(MtModAreaBaseVO::getAreaCode, MtModAreaBaseVO::getAreaId));
```

### 示例3：获取区域采购信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaPurchaseBaseVO;

MtModAreaPurchaseBaseVO purchaseInfo = mtAreaRpcClient.areaPurchasePropertyGet(tenantId, areaId);
String purchaseOrgCode = purchaseInfo.getPurchaseOrganizationCode();
```

### 示例4：查询区域相关区域

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaVO1;
import org.tarzan.model.domain.vo.MtModAreaVO4;

// 查询所有相关区域
MtModAreaVO4 queryVO = new MtModAreaVO4();
queryVO.setAreaId(areaId);
queryVO.setAreaType("PRODUCTION");
List<MtModAreaVO4> allRelatedAreas = mtAreaRpcClient.areaLimitAllRelatedAreaQuery(tenantId, queryVO);

// 查询特定相关区域
MtModAreaVO1 queryVO1 = new MtModAreaVO1();
queryVO1.setAreaId(areaId);
queryVO1.setRelatedAreaType("STORAGE");
List<MtModAreaVO1> relatedAreas = mtAreaRpcClient.areaLimitRelatedAreaQuery(tenantId, queryVO1);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 区域关系查询需要正确设置查询对象的参数，以获取正确的区域关系信息
4. 不同方法返回的对象类型不同，使用时需要注意类型转换