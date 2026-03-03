# Method模块跨服务接口文档

## 概述

Method模块包含了工艺方法相关的跨服务接口，用于查询和管理工艺路线、工序、BOM、工艺版本和方法属性等。

## 接口列表

### 1. MtRouterRpcClient

**类路径**：`org.tarzan.boot.method.client.MtRouterRpcClient`

**主要方法**：
- `routerBasicPropertyGet` - 获取单个工艺路线基本信息
- `routerBasicPropertyBatchGet` - 批量获取工艺路线基本信息
- `codeLimitRouterBasicBatchQuery` - 根据编码批量查询工艺路线基本信息
- `routerPropertyGet` - 获取单个工艺路线详细信息
- `routerPropertyBatchGet` - 批量获取工艺路线详细信息
- `routerLimitRouterQuery` - 查询工艺路线
- `routerLimitRouterBatchQuery` - 批量查询工艺路线

**用途**：用于查询工艺路线相关信息，支持单个和批量查询，可根据编码查询工艺路线基本信息。

### 2. MtOperationRpcClient

**类路径**：`org.tarzan.boot.method.client.MtOperationRpcClient`

**主要方法**：
- `operationBasicPropertyGet` - 获取单个工序基本信息
- `operationBasicPropertyBatchGet` - 批量获取工序基本信息
- `codeLimitOperationBasicBatchQuery` - 根据编码批量查询工序基本信息
- `operationPropertyGet` - 获取单个工序详细信息
- `operationPropertyBatchGet` - 批量获取工序详细信息
- `operationLimitOperationQuery` - 查询工序
- `operationLimitOperationBatchQuery` - 批量查询工序

**用途**：用于查询工序相关信息，支持单个和批量查询，可根据编码查询工序基本信息。

### 3. MtBomRpcClient

**类路径**：`org.tarzan.boot.method.client.MtBomRpcClient`

**主要方法**：
- `bomBasicPropertyGet` - 获取单个BOM基本信息
- `bomBasicPropertyBatchGet` - 批量获取BOM基本信息
- `codeLimitBomBasicBatchQuery` - 根据编码批量查询BOM基本信息
- `bomPropertyGet` - 获取单个BOM详细信息
- `bomPropertyBatchGet` - 批量获取BOM详细信息
- `bomLimitBomQuery` - 查询BOM
- `bomLimitBomBatchQuery` - 批量查询BOM

**用途**：用于查询BOM（物料清单）相关信息，支持单个和批量查询，可根据编码查询BOM基本信息。

### 4. MtProdVersionRpcClient

**类路径**：`org.tarzan.boot.method.client.MtProdVersionRpcClient`

**主要方法**：
- `prodVersionBasicPropertyGet` - 获取单个工艺版本基本信息
- `prodVersionBasicPropertyBatchGet` - 批量获取工艺版本基本信息
- `codeLimitProdVersionBasicBatchQuery` - 根据编码批量查询工艺版本基本信息
- `prodVersionPropertyGet` - 获取单个工艺版本详细信息
- `prodVersionPropertyBatchGet` - 批量获取工艺版本详细信息
- `prodVersionLimitProdVersionQuery` - 查询工艺版本
- `prodVersionLimitProdVersionBatchQuery` - 批量查询工艺版本

**用途**：用于查询工艺版本相关信息，支持单个和批量查询，可根据编码查询工艺版本基本信息。

### 5. MtMethodAttrRpcClient

**类路径**：`org.tarzan.boot.method.client.MtMethodAttrRpcClient`

**主要方法**：
- `disRouteAttrPropertyGet` - 获取单个工艺路线属性信息
- `disRouteAttrPropertyBatchGet` - 批量获取工艺路线属性信息
- `disRouteAttrLimitDisRouteAttrQuery` - 查询工艺路线属性
- `disRouteAttrLimitDisRouteAttrBatchQuery` - 批量查询工艺路线属性
- `disOperationAttrPropertyGet` - 获取单个工序属性信息
- `disOperationAttrPropertyBatchGet` - 批量获取工序属性信息
- `disOperationAttrLimitDisOperationAttrQuery` - 查询工序属性
- `disOperationAttrLimitDisOperationAttrBatchQuery` - 批量查询工序属性

**用途**：用于查询工艺方法属性相关信息，支持单个和批量查询，可查询工艺路线和工序的属性信息。

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

### 示例2：根据编码批量查询工序基本信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

List<String> operationCodes = Arrays.asList("OP001", "OP002");
List<MtOperationBaseVO> operations = mtOperationRpcClient.codeLimitOperationBasicBatchQuery(tenantId, operationCodes);
Map<String, Long> operationIdMap = operations.stream()
    .collect(Collectors.toMap(MtOperationBaseVO::getOperationCode, MtOperationBaseVO::getOperationId));
```

### 示例3：批量获取BOM详细信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomVO;

List<Long> bomIds = Arrays.asList(1L, 2L, 3L);
List<MtBomVO> boms = mtBomRpcClient.bomPropertyBatchGet(tenantId, bomIds);
Map<Long, String> bomNameMap = boms.stream()
    .collect(Collectors.toMap(MtBomVO::getBomId, MtBomVO::getBomName));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 工艺路线、工序、BOM等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法
6. 方法属性查询用于获取工艺路线和工序的扩展属性信息