# MtOperationRpcClient 方法文档

## 概述

MtOperationRpcClient 是一个跨服务客户端，用于查询工序相关的信息，包括工序基本信息、工序工位分配关系、不合格品有效工序等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtOperationRpcClient** | `org.tarzan.boot.method.client.MtOperationRpcClient` |
| **MtOperationBaseVO** | `org.tarzan.method.domain.vo.MtOperationBaseVO` |
| **MtOperationVO** | `org.tarzan.method.domain.vo.MtOperationVO` |
| **MtOperationVO1** | `org.tarzan.method.domain.vo.MtOperationVO1` |
| **MtOperationVO2** | `org.tarzan.method.domain.vo.MtOperationVO2` |
| **MtOperationVO3** | `org.tarzan.method.domain.vo.MtOperationVO3` |
| **MtOperationWkcDispatchRelBaseVO** | `org.tarzan.method.domain.vo.MtOperationWkcDispatchRelBaseVO` |
| **MtNcValidOperationVO** | `org.tarzan.method.domain.vo.MtNcValidOperationVO` |
| **MtNcValidOperationVO1** | `org.tarzan.method.domain.vo.MtNcValidOperationVO1` |
| **MtNcValidOperationVO3** | `org.tarzan.method.domain.vo.MtNcValidOperationVO3` |
| **MtNcValidOperationVO4** | `org.tarzan.method.domain.vo.MtNcValidOperationVO4` |
| **MtNcValidOperationVO5** | `org.tarzan.method.domain.vo.MtNcValidOperationVO5` |

## 方法列表

### 1. operationBasicPropertyGet

**用途**：获取单个工序基本信息

**参数**：
- tenantId：租户ID
- operationId：工序ID

**返回值**：MtOperationBaseVO - 工序基本信息

### 2. operationBasicPropertyBatchGet

**用途**：批量获取工序基本信息

**参数**：
- tenantId：租户ID
- operationIds：工序ID列表

**返回值**：List<MtOperationBaseVO> - 工序基本信息列表

### 3. codeLimitOperationBasicBatchQuery

**用途**：根据编码批量查询工序基本信息

**参数**：
- tenantId：租户ID
- operationCodes：工序编码列表

**返回值**：List<MtOperationBaseVO> - 工序基本信息列表

### 4. operationPropertyGet

**用途**：获取单个工序详细信息

**参数**：
- tenantId：租户ID
- operationId：工序ID

**返回值**：MtOperationVO - 工序详细信息

### 5. operationPropertyBatchGet

**用途**：批量获取工序详细信息

**参数**：
- tenantId：租户ID
- operationIds：工序ID列表

**返回值**：List<MtOperationVO> - 工序详细信息列表

### 6. operationWkcDispatchRelPropertyGet

**用途**：获取单个工序工位分配关系信息

**参数**：
- tenantId：租户ID
- operationWkcDispatchRelId：工序工位分配关系ID

**返回值**：MtOperationWkcDispatchRelBaseVO - 工序工位分配关系信息

### 7. operationWkcDispatchRelPropertyBatchGet

**用途**：批量获取工序工位分配关系信息

**参数**：
- tenantId：租户ID
- operationWkcDispatchRelIds：工序工位分配关系ID列表

**返回值**：List<MtOperationWkcDispatchRelBaseVO> - 工序工位分配关系信息列表

### 8. operationLimitOperationWkcDispatchRelQuery

**用途**：查询工序工位分配关系

**参数**：
- tenantId：租户ID
- queryVO：工序工位分配关系查询对象

**返回值**：List<MtOperationWkcDispatchRelBaseVO> - 工序工位分配关系列表

### 9. ncValidOperationPropertyGet

**用途**：获取单个不合格品有效工序信息

**参数**：
- tenantId：租户ID
- ncValidOperationId：不合格品有效工序ID

**返回值**：MtNcValidOperationVO - 不合格品有效工序信息

### 10. ncValidOperationPropertyBatchGet

**用途**：批量获取不合格品有效工序信息

**参数**：
- tenantId：租户ID
- ncValidOperationIds：不合格品有效工序ID列表

**返回值**：List<MtNcValidOperationVO> - 不合格品有效工序信息列表

### 11. ncLimitNcValidOperationQuery

**用途**：查询不合格品有效工序

**参数**：
- tenantId：租户ID
- queryVO：不合格品有效工序查询对象

**返回值**：List<MtNcValidOperationVO1> - 不合格品有效工序列表

### 12. ncLimitNcValidOperationBatchQuery

**用途**：批量查询不合格品有效工序

**参数**：
- tenantId：租户ID
- queryVOs：不合格品有效工序查询对象列表

**返回值**：List<MtNcValidOperationVO3> - 不合格品有效工序列表

### 13. operationLimitOperationQuery

**用途**：查询工序

**参数**：
- tenantId：租户ID
- queryVO：工序查询对象

**返回值**：List<MtOperationVO1> - 工序列表

### 14. operationLimitOperationBatchQuery

**用途**：批量查询工序

**参数**：
- tenantId：租户ID
- queryVOs：工序查询对象列表

**返回值**：List<MtOperationVO2> - 工序列表

### 15. operationLimitCurrentOperationQuery

**用途**：查询当前工序

**参数**：
- tenantId：租户ID
- queryVO：当前工序查询对象

**返回值**：List<MtOperationVO3> - 当前工序列表

### 16. operationAssemblePointQuery

**用途**：查询工序装配点

**参数**：
- tenantId：租户ID
- queryVO：工序装配点查询对象

**返回值**：List<MtNcValidOperationVO4> - 工序装配点列表

### 17. operationCurrentOperationBatchValidate

**用途**：批量验证当前工序

**参数**：
- tenantId：租户ID
- validateVOs：当前工序验证对象列表

**返回值**：List<MtNcValidOperationVO5> - 验证结果列表

## 使用示例

### 示例1：批量获取工序基本信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

List<Long> operationIds = Arrays.asList(1L, 2L, 3L);
List<MtOperationBaseVO> operations = mtOperationRpcClient.operationBasicPropertyBatchGet(tenantId, operationIds);
Map<Long, String> operationCodeMap = operations.stream()
    .collect(Collectors.toMap(MtOperationBaseVO::getOperationId, MtOperationBaseVO::getOperationCode));
```

### 示例2：根据编码批量查询工序基本信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

List<String> operationCodes = Arrays.asList("OP001", "OP002", "OP003");
List<MtOperationBaseVO> operations = mtOperationRpcClient.codeLimitOperationBasicBatchQuery(tenantId, operationCodes);
Map<String, Long> operationIdMap = operations.stream()
    .collect(Collectors.toMap(MtOperationBaseVO::getOperationCode, MtOperationBaseVO::getOperationId));
```

### 示例3：批量获取工序详细信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;

List<Long> operationIds = Arrays.asList(1L, 2L, 3L);
List<MtOperationVO> operations = mtOperationRpcClient.operationPropertyBatchGet(tenantId, operationIds);
Map<Long, String> operationNameMap = operations.stream()
    .collect(Collectors.toMap(MtOperationVO::getOperationId, MtOperationVO::getOperationName));
```

### 示例4：查询工序工位分配关系

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationWkcDispatchRelBaseVO;

MtOperationWkcDispatchRelBaseVO queryVO = new MtOperationWkcDispatchRelBaseVO();
queryVO.setOperationId(operationId);
queryVO.setWorkcellId(workcellId);
List<MtOperationWkcDispatchRelBaseVO> dispatchRels = mtOperationRpcClient.operationLimitOperationWkcDispatchRelQuery(tenantId, queryVO);
```

### 示例5：查询不合格品有效工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtNcValidOperationVO1;

MtNcValidOperationVO1 queryVO = new MtNcValidOperationVO1();
queryVO.setNcCodeId(ncCodeId);
queryVO.setOperationId(operationId);
List<MtNcValidOperationVO1> ncValidOperations = mtOperationRpcClient.ncLimitNcValidOperationQuery(tenantId, queryVO);
```

### 示例6：查询工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO1;

MtOperationVO1 queryVO = new MtOperationVO1();
queryVO.setOperationType("ASSEMBLY");
queryVO.setSiteId(siteId);
List<MtOperationVO1> operations = mtOperationRpcClient.operationLimitOperationQuery(tenantId, queryVO);
```

### 示例7：查询当前工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO3;

MtOperationVO3 queryVO = new MtOperationVO3();
queryVO.setEoId(eoId);
queryVO.setRouterStepId(routerStepId);
List<MtOperationVO3> currentOperations = mtOperationRpcClient.operationLimitCurrentOperationQuery(tenantId, queryVO);
```

### 示例8：批量验证当前工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtNcValidOperationVO5;

List<MtNcValidOperationVO5> validateVOs = Arrays.asList(
    new MtNcValidOperationVO5(eoId1, operationId1),
    new MtNcValidOperationVO5(eoId2, operationId2)
);
List<MtNcValidOperationVO5> results = mtOperationRpcClient.operationCurrentOperationBatchValidate(tenantId, validateVOs);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 工序工位分配关系查询需要提供工序ID和/或工位ID
4. 不合格品有效工序查询需要提供不合格品代码ID和/或工序ID
5. 工序查询支持按工序类型和站点查询
6. 当前工序查询需要提供执行作业ID和工艺路线步骤ID
7. 不同方法返回的对象类型不同，使用时需要注意类型转换
8. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
9. 工序是制造执行的核心，包含操作、资源需求等信息