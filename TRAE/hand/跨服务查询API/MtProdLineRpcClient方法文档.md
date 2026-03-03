# MtProdLineRpcClient 方法文档

## 概述

MtProdLineRpcClient 是一个跨服务客户端，用于查询生产线相关的信息，包括生产线基本信息、生产线制造信息、生产线调度信息等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtProdLineRpcClient** | `org.tarzan.boot.model.client.MtProdLineRpcClient` |
| **MtModProdLineManufacturingBaseVO** | `org.tarzan.model.domain.vo.MtModProdLineManufacturingBaseVO` |
| **MtModProdLineScheduleBaseVO** | `org.tarzan.model.domain.vo.MtModProdLineScheduleBaseVO` |
| **MtModProdLineDispatchOperationBaseVO** | `org.tarzan.model.domain.vo.MtModProdLineDispatchOperationBaseVO` |
| **MtModProdLineManufacturingVO** | `org.tarzan.model.domain.vo.MtModProdLineManufacturingVO` |
| **MtModProdLineScheduleVO** | `org.tarzan.model.domain.vo.MtModProdLineScheduleVO` |

## 方法列表

### 1. prodLineManufacturingPropertyGet

**用途**：获取单个生产线制造信息

**参数**：
- tenantId：租户ID
- prodLineId：生产线ID

**返回值**：MtModProdLineManufacturingBaseVO - 生产线制造信息

### 2. prodLineManufacturingPropertyBatchGet

**用途**：批量获取生产线制造信息

**参数**：
- tenantId：租户ID
- prodLineIds：生产线ID列表

**返回值**：List<MtModProdLineManufacturingBaseVO> - 生产线制造信息列表

### 3. codeLimitProdLineManufacturingBatchQuery

**用途**：根据编码批量查询生产线制造信息

**参数**：
- tenantId：租户ID
- prodLineCodes：生产线编码列表

**返回值**：List<MtModProdLineManufacturingBaseVO> - 生产线制造信息列表

### 4. prodLineSchedulePropertyGet

**用途**：获取单个生产线调度信息

**参数**：
- tenantId：租户ID
- prodLineId：生产线ID

**返回值**：MtModProdLineScheduleBaseVO - 生产线调度信息

### 5. prodLineSchedulePropertyBatchGet

**用途**：批量获取生产线调度信息

**参数**：
- tenantId：租户ID
- prodLineIds：生产线ID列表

**返回值**：List<MtModProdLineScheduleBaseVO> - 生产线调度信息列表

### 6. prodLineDispatchOperationPropertyGet

**用途**：获取单个生产线调度操作信息

**参数**：
- tenantId：租户ID
- prodLineId：生产线ID

**返回值**：MtModProdLineDispatchOperationBaseVO - 生产线调度操作信息

### 7. prodLineDispatchOperationPropertyBatchGet

**用途**：批量获取生产线调度操作信息

**参数**：
- tenantId：租户ID
- prodLineIds：生产线ID列表

**返回值**：List<MtModProdLineDispatchOperationBaseVO> - 生产线调度操作信息列表

### 8. prodLineLimitRelatedProdLineQuery

**用途**：查询生产线相关生产线

**参数**：
- tenantId：租户ID
- queryVO：生产线关系查询对象

**返回值**：List<MtModProdLineManufacturingVO> - 相关生产线列表

### 9. prodLineCapacityQuery

**用途**：查询生产线产能信息

**参数**：
- tenantId：租户ID
- queryVO：产能查询对象

**返回值**：List<MtModProdLineScheduleVO> - 产能信息列表

## 使用示例

### 示例1：批量获取生产线制造信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingBaseVO;

List<Long> prodLineIds = Arrays.asList(1L, 2L, 3L);
List<MtModProdLineManufacturingBaseVO> prodLines = mtProdLineRpcClient.prodLineManufacturingPropertyBatchGet(tenantId, prodLineIds);
Map<Long, String> prodLineCodeMap = prodLines.stream()
    .collect(Collectors.toMap(MtModProdLineManufacturingBaseVO::getProdLineId, MtModProdLineManufacturingBaseVO::getProdLineCode));
```

### 示例2：根据编码批量查询生产线制造信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingBaseVO;

List<String> prodLineCodes = Arrays.asList("PROD001", "PROD002", "PROD003");
List<MtModProdLineManufacturingBaseVO> prodLines = mtProdLineRpcClient.codeLimitProdLineManufacturingBatchQuery(tenantId, prodLineCodes);
Map<String, Long> prodLineIdMap = prodLines.stream()
    .collect(Collectors.toMap(MtModProdLineManufacturingBaseVO::getProdLineCode, MtModProdLineManufacturingBaseVO::getProdLineId));
```

### 示例3：获取生产线调度信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineScheduleBaseVO;

MtModProdLineScheduleBaseVO scheduleInfo = mtProdLineRpcClient.prodLineSchedulePropertyGet(tenantId, prodLineId);
String scheduleStatus = scheduleInfo.getScheduleStatus();
```

### 示例4：查询生产线相关生产线

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingVO;

MtModProdLineManufacturingVO queryVO = new MtModProdLineManufacturingVO();
queryVO.setProdLineId(prodLineId);
queryVO.setRelatedProdLineType("ASSEMBLY");
List<MtModProdLineManufacturingVO> relatedProdLines = mtProdLineRpcClient.prodLineLimitRelatedProdLineQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 生产线关系查询需要正确设置查询对象的参数，以获取正确的生产线关系信息
4. 不同方法返回的对象类型不同，使用时需要注意类型转换
5. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量