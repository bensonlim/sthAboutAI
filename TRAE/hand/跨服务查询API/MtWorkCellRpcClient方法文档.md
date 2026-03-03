# MtWorkCellRpcClient 方法文档

## 概述

MtWorkCellRpcClient 是一个跨服务客户端，用于查询工位相关的信息，包括工位基本信息、工位制造信息等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtWorkCellRpcClient** | `org.tarzan.boot.model.client.MtWorkCellRpcClient` |
| **MtModWorkcellBaseVO** | `org.tarzan.model.domain.vo.MtModWorkcellBaseVO` |
| **MtModWorkcellManufacturingBaseVO** | `org.tarzan.model.domain.vo.MtModWorkcellManufacturingBaseVO` |
| **MtModWorkcellManufacturingVO1** | `org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO1` |
| **MtModWorkcellManufacturingVO2** | `org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO2` |
| **MtModWorkcellManufacturingVO3** | `org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO3` |
| **MtModWorkcellVO1** | `org.tarzan.model.domain.vo.MtModWorkcellVO1` |
| **MtModWorkcellVO5** | `org.tarzan.model.domain.vo.MtModWorkcellVO5` |

## 方法列表

### 1. workcellBasicPropertyGet

**用途**：获取单个工位基本信息

**参数**：
- tenantId：租户ID
- workcellId：工位ID

**返回值**：MtModWorkcellBaseVO - 工位基本信息

### 2. workcellBasicPropertyBatchGet

**用途**：批量获取工位基本信息

**参数**：
- tenantId：租户ID
- workcellIds：工位ID列表

**返回值**：List<MtModWorkcellBaseVO> - 工位基本信息列表

### 3. codeLimitWorkcellBasicBatchQuery

**用途**：根据编码批量查询工位基本信息

**参数**：
- tenantId：租户ID
- workcellCodes：工位编码列表

**返回值**：List<MtModWorkcellBaseVO> - 工位基本信息列表

### 4. workcellManufacturingPropertyGet

**用途**：获取单个工位制造信息

**参数**：
- tenantId：租户ID
- workcellId：工位ID

**返回值**：MtModWorkcellManufacturingBaseVO - 工位制造信息

### 5. workcellManufacturingPropertyBatchGet

**用途**：批量获取工位制造信息

**参数**：
- tenantId：租户ID
- workcellIds：工位ID列表

**返回值**：List<MtModWorkcellManufacturingBaseVO> - 工位制造信息列表

### 6. codeLimitWorkcellManufacturingBatchQuery

**用途**：根据编码批量查询工位制造信息

**参数**：
- tenantId：租户ID
- workcellCodes：工位编码列表

**返回值**：List<MtModWorkcellManufacturingBaseVO> - 工位制造信息列表

### 7. workcellLimitRelatedWorkcellQuery

**用途**：查询工位相关工位

**参数**：
- tenantId：租户ID
- queryVO：工位关系查询对象

**返回值**：List<MtModWorkcellVO1> - 相关工位列表

### 8. workcellLimitAllRelatedWorkcellQuery

**用途**：查询工位所有相关工位

**参数**：
- tenantId：租户ID
- queryVO：工位关系查询对象

**返回值**：List<MtModWorkcellVO5> - 所有相关工位列表

### 9. workcellCapacityQuery

**用途**：查询工位产能信息

**参数**：
- tenantId：租户ID
- queryVO：产能查询对象

**返回值**：List<MtModWorkcellManufacturingVO2> - 产能信息列表

### 10. workcellLimitWorkcellManufacturingQuery

**用途**：查询工位制造信息

**参数**：
- tenantId：租户ID
- queryVO：工位制造查询对象

**返回值**：List<MtModWorkcellManufacturingVO3> - 工位制造信息列表

## 使用示例

### 示例1：批量获取工位基本信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;

List<Long> workcellIds = Arrays.asList(1L, 2L, 3L);
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.workcellBasicPropertyBatchGet(tenantId, workcellIds);
Map<Long, String> workcellCodeMap = workcells.stream()
    .collect(Collectors.toMap(MtModWorkcellBaseVO::getWorkcellId, MtModWorkcellBaseVO::getWorkcellCode));
```

### 示例2：根据编码批量查询工位基本信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;

List<String> workcellCodes = Arrays.asList("WC001", "WC002", "WC003");
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.codeLimitWorkcellBasicBatchQuery(tenantId, workcellCodes);
Map<String, Long> workcellIdMap = workcells.stream()
    .collect(Collectors.toMap(MtModWorkcellBaseVO::getWorkcellCode, MtModWorkcellBaseVO::getWorkcellId));
```

### 示例3：批量获取工位制造信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingBaseVO;

List<Long> workcellIds = Arrays.asList(1L, 2L, 3L);
List<MtModWorkcellManufacturingBaseVO> workcells = mtWorkCellRpcClient.workcellManufacturingPropertyBatchGet(tenantId, workcellIds);
Map<Long, String> workcellNameMap = workcells.stream()
    .collect(Collectors.toMap(MtModWorkcellManufacturingBaseVO::getWorkcellId, MtModWorkcellManufacturingBaseVO::getWorkcellName));
```

### 示例4：查询工位相关工位

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellVO1;

MtModWorkcellVO1 queryVO = new MtModWorkcellVO1();
queryVO.setWorkcellId(workcellId);
queryVO.setRelatedWorkcellType("PARENT");
List<MtModWorkcellVO1> relatedWorkcells = mtWorkCellRpcClient.workcellLimitRelatedWorkcellQuery(tenantId, queryVO);
```

### 示例5：查询工位产能信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO2;

MtModWorkcellManufacturingVO2 queryVO = new MtModWorkcellManufacturingVO2();
queryVO.setWorkcellId(workcellId);
queryVO.setStartDate(startDate);
queryVO.setEndDate(endDate);
List<MtModWorkcellManufacturingVO2> capacities = mtWorkCellRpcClient.workcellCapacityQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 工位关系查询需要正确设置查询对象的参数，以获取正确的工位关系信息
4. 不同方法返回的对象类型不同，使用时需要注意类型转换
5. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
6. 工位产能查询需要提供时间范围参数（startDate和endDate）