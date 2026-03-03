# MtRouterRpcClient 方法文档

## 概述

MtRouterRpcClient 是一个跨服务客户端，用于查询工艺路线（Router）相关的信息，包括工艺路线基本信息、工艺路线步骤、工艺路线操作、工艺路线站点分配等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtRouterRpcClient** | `org.tarzan.boot.method.client.MtRouterRpcClient` |
| **MtRouterBaseVO** | `org.tarzan.method.domain.vo.MtRouterBaseVO` |
| **MtRouterVO1** | `org.tarzan.method.domain.vo.MtRouterVO1` |
| **MtRouterVO3** | `org.tarzan.method.domain.vo.MtRouterVO3` |
| **MtRouterStepBaseVO** | `org.tarzan.method.domain.vo.MtRouterStepBaseVO` |
| **MtRouterStepVO5** | `org.tarzan.method.domain.vo.MtRouterStepVO5` |
| **MtRouterStepVO6** | `org.tarzan.method.domain.vo.MtRouterStepVO6` |
| **MtRouterOperationVO1** | `org.tarzan.method.domain.vo.MtRouterOperationVO1` |
| **MtRouterOperationVO2** | `org.tarzan.method.domain.vo.MtRouterOperationVO2` |
| **MtRouterSiteAssignVO** | `org.tarzan.method.domain.vo.MtRouterSiteAssignVO` |
| **MtRouterSiteAssignVO2** | `org.tarzan.method.domain.vo.MtRouterSiteAssignVO2` |
| **MtRouterLinkVO** | `org.tarzan.method.domain.vo.MtRouterLinkVO` |
| **MtRouterLinkVO2** | `org.tarzan.method.domain.vo.MtRouterLinkVO2` |
| **MtRouterNextStepVO3** | `org.tarzan.method.domain.vo.MtRouterNextStepVO3` |
| **MtRouterNextStepVO4** | `org.tarzan.method.domain.vo.MtRouterNextStepVO4` |
| **MtRouterOpComponentVO** | `org.tarzan.method.domain.vo.MtRouterOpComponentVO` |
| **MtRouterOpComponentVO1** | `org.tarzan.method.domain.vo.MtRouterOpComponentVO1` |
| **MtMaterialRouterRelVO** | `org.tarzan.method.domain.vo.MtMaterialRouterRelVO` |
| **MtRouterAllDataVO** | `org.tarzan.method.domain.vo.MtRouterAllDataVO` |

## 方法列表

### 1. routerBasicPropertyGet

**用途**：获取单个工艺路线基本信息

**参数**：
- tenantId：租户ID
- routerId：工艺路线ID

**返回值**：MtRouterBaseVO - 工艺路线基本信息

### 2. routerBasicPropertyBatchGet

**用途**：批量获取工艺路线基本信息

**参数**：
- tenantId：租户ID
- routerIds：工艺路线ID列表

**返回值**：List<MtRouterBaseVO> - 工艺路线基本信息列表

### 3. codeLimitRouterBasicBatchQuery

**用途**：根据编码批量查询工艺路线基本信息

**参数**：
- tenantId：租户ID
- routerCodes：工艺路线编码列表

**返回值**：List<MtRouterBaseVO> - 工艺路线基本信息列表

### 4. routerStepPropertyGet

**用途**：获取单个工艺路线步骤信息

**参数**：
- tenantId：租户ID
- routerStepId：工艺路线步骤ID

**返回值**：MtRouterStepBaseVO - 工艺路线步骤信息

### 5. routerStepPropertyBatchGet

**用途**：批量获取工艺路线步骤信息

**参数**：
- tenantId：租户ID
- routerStepIds：工艺路线步骤ID列表

**返回值**：List<MtRouterStepBaseVO> - 工艺路线步骤信息列表

### 6. routerLimitRouterStepQuery

**用途**：查询工艺路线步骤

**参数**：
- tenantId：租户ID
- queryVO：工艺路线步骤查询对象

**返回值**：List<MtRouterStepVO5> - 工艺路线步骤列表

### 7. routerLimitRouterStepBatchQuery

**用途**：批量查询工艺路线步骤

**参数**：
- tenantId：租户ID
- queryVOs：工艺路线步骤查询对象列表

**返回值**：List<MtRouterStepVO6> - 工艺路线步骤列表

### 8. routerOperationPropertyGet

**用途**：获取单个工艺路线操作信息

**参数**：
- tenantId：租户ID
- routerOperationId：工艺路线操作ID

**返回值**：MtRouterOperationVO1 - 工艺路线操作信息

### 9. routerOperationPropertyBatchGet

**用途**：批量获取工艺路线操作信息

**参数**：
- tenantId：租户ID
- routerOperationIds：工艺路线操作ID列表

**返回值**：List<MtRouterOperationVO1> - 工艺路线操作信息列表

### 10. routerLimitRouterOperationQuery

**用途**：查询工艺路线操作

**参数**：
- tenantId：租户ID
- queryVO：工艺路线操作查询对象

**返回值**：List<MtRouterOperationVO2> - 工艺路线操作列表

### 11. routerSiteAssignPropertyGet

**用途**：获取单个工艺路线站点分配信息

**参数**：
- tenantId：租户ID
- routerSiteAssignId：工艺路线站点分配ID

**返回值**：MtRouterSiteAssignVO - 工艺路线站点分配信息

### 12. routerSiteAssignPropertyBatchGet

**用途**：批量获取工艺路线站点分配信息

**参数**：
- tenantId：租户ID
- routerSiteAssignIds：工艺路线站点分配ID列表

**返回值**：List<MtRouterSiteAssignVO> - 工艺路线站点分配信息列表

### 13. routerLimitRouterSiteAssignQuery

**用途**：查询工艺路线站点分配

**参数**：
- tenantId：租户ID
- queryVO：工艺路线站点分配查询对象

**返回值**：List<MtRouterSiteAssignVO2> - 工艺路线站点分配列表

### 14. routerLinkPropertyGet

**用途**：获取单个工艺路线链接信息

**参数**：
- tenantId：租户ID
- routerLinkId：工艺路线链接ID

**返回值**：MtRouterLinkVO - 工艺路线链接信息

### 15. routerLinkPropertyBatchGet

**用途**：批量获取工艺路线链接信息

**参数**：
- tenantId：租户ID
- routerLinkIds：工艺路线链接ID列表

**返回值**：List<MtRouterLinkVO> - 工艺路线链接信息列表

### 16. routerLimitRouterLinkQuery

**用途**：查询工艺路线链接

**参数**：
- tenantId：租户ID
- queryVO：工艺路线链接查询对象

**返回值**：List<MtRouterLinkVO2> - 工艺路线链接列表

### 17. routerNextStepPropertyGet

**用途**：获取单个工艺路线下一步信息

**参数**：
- tenantId：租户ID
- routerNextStepId：工艺路线下一步ID

**返回值**：MtRouterNextStepVO3 - 工艺路线下一步信息

### 18. routerLimitRouterNextStepQuery

**用途**：查询工艺路线下一步

**参数**：
- tenantId：租户ID
- queryVO：工艺路线下一步查询对象

**返回值**：List<MtRouterNextStepVO4> - 工艺路线下一步列表

### 19. routerOpComponentPropertyGet

**用途**：获取单个工艺路线操作组件信息

**参数**：
- tenantId：租户ID
- routerOpComponentId：工艺路线操作组件ID

**返回值**：MtRouterOpComponentVO - 工艺路线操作组件信息

### 20. routerLimitRouterOpComponentQuery

**用途**：查询工艺路线操作组件

**参数**：
- tenantId：租户ID
- queryVO：工艺路线操作组件查询对象

**返回值**：List<MtRouterOpComponentVO1> - 工艺路线操作组件列表

### 21. materialLimitRouterRelQuery

**用途**：查询物料工艺路线关系

**参数**：
- tenantId：租户ID
- queryVO：物料工艺路线关系查询对象

**返回值**：List<MtMaterialRouterRelVO> - 物料工艺路线关系列表

### 22. routerLimitRouterQuery

**用途**：查询工艺路线

**参数**：
- tenantId：租户ID
- queryVO：工艺路线查询对象

**返回值**：List<MtRouterVO1> - 工艺路线列表

### 23. routerLimitRouterBatchQuery

**用途**：批量查询工艺路线

**参数**：
- tenantId：租户ID
- queryVOs：工艺路线查询对象列表

**返回值**：List<MtRouterVO3> - 工艺路线列表

### 24. routerAllQuery

**用途**：查询工艺路线完整信息（包括步骤、操作等）

**参数**：
- tenantId：租户ID
- queryVO：工艺路线完整信息查询对象

**返回值**：MtRouterAllDataVO - 工艺路线完整信息

## 使用示例

### 示例1：批量获取工艺路线基本信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterBaseVO;

List<Long> routerIds = Arrays.asList(1L, 2L, 3L);
List<MtRouterBaseVO> routers = mtRouterRpcClient.routerBasicPropertyBatchGet(tenantId, routerIds);
Map<Long, String> routerCodeMap = routers.stream()
    .collect(Collectors.toMap(MtRouterBaseVO::getRouterId, MtRouterBaseVO::getRouterCode));
```

### 示例2：根据编码批量查询工艺路线基本信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterBaseVO;

List<String> routerCodes = Arrays.asList("ROUT001", "ROUT002", "ROUT003");
List<MtRouterBaseVO> routers = mtRouterRpcClient.codeLimitRouterBasicBatchQuery(tenantId, routerCodes);
Map<String, Long> routerIdMap = routers.stream()
    .collect(Collectors.toMap(MtRouterBaseVO::getRouterCode, MtRouterBaseVO::getRouterId));
```

### 示例3：查询工艺路线步骤

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterStepVO5;

MtRouterStepVO5 queryVO = new MtRouterStepVO5();
queryVO.setRouterId(routerId);
queryVO.setRouterStepName("ASSEMBLY");
List<MtRouterStepVO5> steps = mtRouterRpcClient.routerLimitRouterStepQuery(tenantId, queryVO);
```

### 示例4：批量获取工艺路线步骤信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterStepBaseVO;

List<Long> routerStepIds = Arrays.asList(1L, 2L, 3L);
List<MtRouterStepBaseVO> steps = mtRouterRpcClient.routerStepPropertyBatchGet(tenantId, routerStepIds);
Map<Long, String> stepNameMap = steps.stream()
    .collect(Collectors.toMap(MtRouterStepBaseVO::getRouterStepId, MtRouterStepBaseVO::getRouterStepName));
```

### 示例5：查询工艺路线站点分配

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterSiteAssignVO2;

MtRouterSiteAssignVO2 queryVO = new MtRouterSiteAssignVO2();
queryVO.setRouterId(routerId);
queryVO.setSiteId(siteId);
List<MtRouterSiteAssignVO2> siteAssigns = mtRouterRpcClient.routerLimitRouterSiteAssignQuery(tenantId, queryVO);
```

### 示例6：查询工艺路线链接

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterLinkVO2;

MtRouterLinkVO2 queryVO = new MtRouterLinkVO2();
queryVO.setRouterId(routerId);
queryVO.setFromRouterStepId(fromStepId);
List<MtRouterLinkVO2> links = mtRouterRpcClient.routerLimitRouterLinkQuery(tenantId, queryVO);
```

### 示例7：查询物料工艺路线关系

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtMaterialRouterRelVO;

MtMaterialRouterRelVO queryVO = new MtMaterialRouterRelVO();
queryVO.setMaterialId(materialId);
queryVO.setSiteId(siteId);
List<MtMaterialRouterRelVO> routerRels = mtRouterRpcClient.materialLimitRouterRelQuery(tenantId, queryVO);
```

### 示例8：查询工艺路线完整信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterAllDataVO;

MtRouterAllDataVO queryVO = new MtRouterAllDataVO();
queryVO.setRouterId(routerId);
queryVO.setRouterVersion(routerVersion);
MtRouterAllDataVO routerAll = mtRouterRpcClient.routerAllQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 工艺路线步骤查询需要提供工艺路线ID和/或步骤名称
4. 工艺路线站点分配查询需要提供工艺路线ID和站点ID
5. 工艺路线链接查询需要提供工艺路线ID和起始步骤ID
6. 物料工艺路线关系查询支持按物料和站点查询
7. 工艺路线完整信息查询会返回工艺路线的所有相关信息，包括步骤、操作等
8. 不同方法返回的对象类型不同，使用时需要注意类型转换
9. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
10. 工艺路线步骤是工艺路线的核心组成部分，包含操作、组件等信息