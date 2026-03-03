# MtProdVersionRpcClient 方法文档

## 概述

MtProdVersionRpcClient 是一个跨服务客户端，用于查询生产版本相关的信息，包括生产版本分配、生产版本可用性验证、PFEP生产版本等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtProdVersionRpcClient** | `org.tarzan.boot.method.client.MtProdVersionRpcClient` |
| **MtProdVersionAssignVO** | `org.tarzan.method.domain.vo.MtProdVersionAssignVO` |
| **MtProdVersionAssignVO1** | `org.tarzan.method.domain.vo.MtProdVersionAssignVO1` |
| **MtProdVersionAssignVO2** | `org.tarzan.method.domain.vo.MtProdVersionAssignVO2` |
| **MtProdVersionAssignVO3** | `org.tarzan.method.domain.vo.MtProdVersionAssignVO3` |
| **MtProdVersionAssignUniqueVO** | `org.tarzan.method.domain.vo.MtProdVersionAssignUniqueVO` |
| **MtProdVersionAssignPriorityUniqueVO** | `org.tarzan.method.domain.vo.MtProdVersionAssignPriorityUniqueVO` |
| **MtProdVersionAvailableResultVO** | `org.tarzan.method.domain.vo.MtProdVersionAvailableResultVO` |
| **MtProdVersionAvailableResultVO1** | `org.tarzan.method.domain.vo.MtProdVersionAvailableResultVO1` |
| **MtProdVersionAvailableValidVO** | `org.tarzan.method.domain.vo.MtProdVersionAvailableValidVO` |
| **MtProdVersionAvailableValidVO1** | `org.tarzan.method.domain.vo.MtProdVersionAvailableValidVO1` |
| **MtPfepProdVersionVO** | `org.tarzan.method.domain.vo.MtPfepProdVersionVO` |
| **MtPfepProdVersionConditionVO** | `org.tarzan.method.domain.vo.MtPfepProdVersionConditionVO` |

## 方法列表

### 1. prodVersionAssignPropertyGet

**用途**：获取单个生产版本分配信息

**参数**：
- tenantId：租户ID
- assignId：分配ID

**返回值**：MtProdVersionAssignVO - 生产版本分配信息

### 2. prodVersionAssignPropertyBatchGet

**用途**：批量获取生产版本分配信息

**参数**：
- tenantId：租户ID
- assignIds：分配ID列表

**返回值**：List<MtProdVersionAssignVO> - 生产版本分配信息列表

### 3. prodVersionAssignUniqueValidate

**用途**：验证生产版本分配唯一性

**参数**：
- tenantId：租户ID
- validateVO：生产版本分配唯一性验证对象

**返回值**：MtProdVersionAssignUniqueVO - 验证结果

### 4. prodVersionAssignPriorityUniqueValidate

**用途**：验证生产版本分配优先级唯一性

**参数**：
- tenantId：租户ID
- validateVO：生产版本分配优先级唯一性验证对象

**返回值**：MtProdVersionAssignPriorityUniqueVO - 验证结果

### 5. prodVersionAvailableValidate

**用途**：验证生产版本可用性

**参数**：
- tenantId：租户ID
- validateVO：生产版本可用性验证对象

**返回值**：MtProdVersionAvailableResultVO - 可用性验证结果

### 6. prodVersionAvailableBatchValidate

**用途**：批量验证生产版本可用性

**参数**：
- tenantId：租户ID
- validateVOs：生产版本可用性验证对象列表

**返回值**：List<MtProdVersionAvailableResultVO> - 可用性验证结果列表

### 7. prodVersionAvailableValidQuery

**用途**：查询生产版本可用性验证

**参数**：
- tenantId：租户ID
- queryVO：生产版本可用性验证查询对象

**返回值**：List<MtProdVersionAvailableValidVO> - 可用性验证列表

### 8. prodVersionAvailableValidBatchQuery

**用途**：批量查询生产版本可用性验证

**参数**：
- tenantId：租户ID
- queryVOs：生产版本可用性验证查询对象列表

**返回值**：List<MtProdVersionAvailableValidVO1> - 可用性验证列表

### 9. pfepProdVersionPropertyGet

**用途**：获取PFEP生产版本信息

**参数**：
- tenantId：租户ID
- pfepProdVersionId：PFEP生产版本ID

**返回值**：MtPfepProdVersionVO - PFEP生产版本信息

### 10. pfepProdVersionPropertyBatchGet

**用途**：批量获取PFEP生产版本信息

**参数**：
- tenantId：租户ID
- pfepProdVersionIds：PFEP生产版本ID列表

**返回值**：List<MtPfepProdVersionVO> - PFEP生产版本信息列表

### 11. pfepProdVersionConditionQuery

**用途**：根据条件查询PFEP生产版本

**参数**：
- tenantId：租户ID
- conditionVO：PFEP生产版本条件查询对象

**返回值**：List<MtPfepProdVersionConditionVO> - PFEP生产版本列表

### 12. prodVersionLimitProdVersionAssignQuery

**用途**：查询生产版本分配

**参数**：
- tenantId：租户ID
- queryVO：生产版本分配查询对象

**返回值**：List<MtProdVersionAssignVO1> - 生产版本分配列表

### 13. prodVersionLimitProdVersionAssignBatchQuery

**用途**：批量查询生产版本分配

**参数**：
- tenantId：租户ID
- queryVOs：生产版本分配查询对象列表

**返回值**：List<MtProdVersionAssignVO2> - 生产版本分配列表

### 14. prodVersionLimitPriorityProdVersionAssignQuery

**用途**：查询优先级生产版本分配

**参数**：
- tenantId：租户ID
- queryVO：优先级生产版本分配查询对象

**返回值**：List<MtProdVersionAssignVO3> - 优先级生产版本分配列表

## 使用示例

### 示例1：批量获取生产版本分配信息

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionAssignVO;

List<Long> assignIds = Arrays.asList(1L, 2L, 3L);
List<MtProdVersionAssignVO> assigns = mtProdVersionRpcClient.prodVersionAssignPropertyBatchGet(tenantId, assignIds);
Map<Long, String> prodVersionMap = assigns.stream()
    .collect(Collectors.toMap(MtProdVersionAssignVO::getAssignId, MtProdVersionAssignVO::getProdVersion));
```

### 示例2：验证生产版本分配唯一性

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionAssignUniqueVO;

MtProdVersionAssignUniqueVO validateVO = new MtProdVersionAssignUniqueVO();
validateVO.setMaterialId(materialId);
validateVO.setSiteId(siteId);
validateVO.setProdVersion(prodVersion);
MtProdVersionAssignUniqueVO result = mtProdVersionRpcClient.prodVersionAssignUniqueValidate(tenantId, validateVO);
```

### 示例3：验证生产版本可用性

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionAvailableValidVO;
import org.tarzan.method.domain.vo.MtProdVersionAvailableResultVO;

MtProdVersionAvailableValidVO validateVO = new MtProdVersionAvailableValidVO();
validateVO.setMaterialId(materialId);
validateVO.setSiteId(siteId);
validateVO.setProdVersion(prodVersion);
MtProdVersionAvailableResultVO result = mtProdVersionRpcClient.prodVersionAvailableValidate(tenantId, validateVO);
```

### 示例4：批量验证生产版本可用性

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionAvailableValidVO;
import org.tarzan.method.domain.vo.MtProdVersionAvailableResultVO;

List<MtProdVersionAvailableValidVO> validateVOs = Arrays.asList(
    new MtProdVersionAvailableValidVO(materialId1, siteId1, prodVersion1),
    new MtProdVersionAvailableValidVO(materialId2, siteId2, prodVersion2)
);
List<MtProdVersionAvailableResultVO> results = mtProdVersionRpcClient.prodVersionAvailableBatchValidate(tenantId, validateVOs);
```

### 示例5：查询PFEP生产版本

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtPfepProdVersionConditionVO;

MtPfepProdVersionConditionVO conditionVO = new MtPfepProdVersionConditionVO();
conditionVO.setMaterialId(materialId);
conditionVO.setSiteId(siteId);
conditionVO.setProdVersion(prodVersion);
List<MtPfepProdVersionConditionVO> pfepVersions = mtProdVersionRpcClient.pfepProdVersionConditionQuery(tenantId, conditionVO);
```

### 示例6：查询生产版本分配

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionAssignVO1;

MtProdVersionAssignVO1 queryVO = new MtProdVersionAssignVO1();
queryVO.setMaterialId(materialId);
queryVO.setSiteId(siteId);
List<MtProdVersionAssignVO1> assigns = mtProdVersionRpcClient.prodVersionLimitProdVersionAssignQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 生产版本分配唯一性验证需要提供物料ID、站点ID和生产版本
4. 生产版本可用性验证需要确保物料、站点和生产版本的正确性
5. PFEP生产版本查询支持多种条件组合查询
6. 不同方法返回的对象类型不同，使用时需要注意类型转换
7. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
8. 生产版本分配优先级验证用于确保同一物料站点下生产版本分配的唯一性