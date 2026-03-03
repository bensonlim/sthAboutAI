# Method模块跨服务接口文档

## 概述

Method模块包含了工艺方法相关的跨服务接口，用于查询和管理物料、工艺路线、工序、BOM、工艺版本和方法属性等。

## 接口列表

### 1. MtMaterialRpcClient

**类路径**：`org.tarzan.boot.method.client.MtMaterialRpcClient`

**主要方法**：
- `materialBasicInfoBatchGet` - 批量获取物料基本信息
- `materialBasicPropertyGet` - 获取单个物料基本信息（已过期）
- `materialBasicPropertyBatchGet` - 批量获取物料基本信息（已过期）
- `codeLimitMaterialBasicBatchQuery` - 根据编码批量查询物料基本信息
- `materialPropertyGet` - 获取单个物料详细信息
- `materialPropertyBatchGet` - 批量获取物料详细信息
- `materialLimitMaterialQuery` - 查询物料
- `materialLimitMaterialBatchQuery` - 批量查询物料
- `conditionLimitMaterialPropertyQuery` - 根据条件查询物料属性
- `propertyLimitMaterialPropertyQuery` - 根据属性查询物料属性
- `codeListLimitMaterialPropertyQuery` - 根据编码列表查询物料属性
- `uomLimitMaterialQuery` - 根据计量单位查询物料
- `nameLimitMaterialQuery` - 根据名称查询物料
- `propertyLimitMaterialGet` - 根据属性查询物料ID
- `materialUomGet` - 获取单个物料的计量单位
- `materialUomBatchGet` - 批量获取物料的计量单位
- `materialUomConversion` - 物料计量单位转换
- `materialDualUomValidate` - 验证物料双重计量单位
- `materialDualUomBatchValidate` - 批量验证物料双重计量单位
- `materialUomTypeValidate` - 验证物料计量单位类型
- `materialUomTypeBatchValidate` - 批量验证物料计量单位类型
- `propertyLimitMaterialBomRelQuery` - 查询物料BOM关系
- `materialCategoryGet` - 获取物料分类
- `materialCategoryCodeGet` - 根据编码获取物料分类
- `materialCategoryPropertyBatchGet` - 批量获取物料分类属性
- `materialCategorySetBatchGet` - 批量获取物料分类集
- `setLimitMaterialCategoryQuery` - 根据分类集查询物料分类
- `propertyLimitMaterialCategoryPropertyQuery` - 根据属性查询物料分类属性
- `codeListLimitMaterialCategoryQuery` - 根据编码列表查询物料分类
- `codeLimitMaterialCategoryQuery` - 根据编码查询物料分类
- `defaultSetMaterialAssignCategoryGet` - 获取默认分类集的物料分配分类
- `setLimitMaterialAssignCategoryGet` - 根据分类集获取物料分配分类
- `defaultSetMaterialAssignCategoryBatchGet` - 批量获取默认分类集的物料分配分类
- `materialCategoryLimitAssignBatchGet` - 批量获取物料分类分配
- `categoryIdLimitQuery` - 根据分类ID查询物料分类分配
- `materialCategoryEnableValidate` - 验证物料分类是否启用
- `defaultCategorySetValidate` - 验证默认分类集
- `materialLimitSiteBatchQuery` - 批量查询物料的站点
- `materialSiteIdLimitBatchQuery` - 根据物料站点ID批量查询
- `queryMaterialSiteByMaterialId` - 根据物料ID查询物料站点
- `materialSiteListLimitMaterialSiteQuery` - 根据物料ID和站点ID查询物料站点
- `materialSiteListLimitMaterialSiteBatchQuery` - 批量查询物料站点
- `queryByMaterialSiteId` - 根据物料站点ID查询
- `propertyLimitMaterialSitePropertyQuery` - 根据属性查询物料站点属性
- `makeBuyCodeLimitPropertyBatchGet` - 根据Make/Buy编码批量获取属性
- `categorySiteLimitMaterialQuery` - 根据分类站点查询物料
- `categorySiteLimitMaterialBatchQuery` - 批量根据分类站点查询物料
- `materialCategorySiteBatchValidate` - 批量验证物料分类站点
- `materialCategorySiteValidate` - 验证物料分类站点
- `selectByMaterialCategorySiteIds` - 根据物料分类站点ID选择
- `materialCategorySiteLimitMaterialSiteQuery` - 根据物料分类站点查询物料站点
- `selectMaterialIdListByCondition` - 根据条件选择物料ID列表
- `materialGhgBatchGet` - 批量获取物料GHG信息
- `flagLimitBatchGet` - 根据标志批量获取
- `materialRevisionAvailableValidate` - 批量验证物料版本是否可用
- `materialRevisionAvailableValidateSelf` - 验证物料版本是否可用

**用途**：用于查询和管理物料相关信息，支持单个和批量查询，可根据编码查询物料基本信息，还提供物料分类、站点、计量单位、BOM关系等相关操作。

### 2. MtRouterRpcClient

**类路径**：`org.tarzan.boot.method.client.MtRouterRpcClient`

**主要方法**：
- `routerBasicPropertyGet` - 获取单个工艺路线基本信息（已过期）
- `routerBasicPropertyBatchGet` - 批量获取工艺路线基本信息（已过期）
- `codeLimitRouterBasicBatchQuery` - 根据编码批量查询工艺路线基本信息（已过期）
- `routerPropertyGet` - 获取单个工艺路线详细信息（已过期）
- `routerPropertyBatchGet` - 批量获取工艺路线详细信息（已过期）
- `routerLimitRouterQuery` - 查询工艺路线（已过期）
- `routerLimitRouterBatchQuery` - 批量查询工艺路线（已过期）
- `routerAllQuery` - 工艺路线全量查询
- `routerAllBatchQuery` - 批量进行工艺路线全量查询
- `routerStepBatchGet` - 批量获取工艺路线步骤信息
- `routerLimitRouterStepBatchQuery` - 批量查询工艺路线步骤
- `routerGet` - 获取工艺路线信息
- `routerSiteLimitRelBatchQuery` - 批量查询工艺路线站点关联
- `routerBatchGet` - 批量获取工艺路线信息
- `routerAvailableBatchValidate` - 批量验证工艺路线是否可用

**用途**：用于查询工艺路线相关信息，支持单个和批量查询，可根据编码查询工艺路线基本信息。

### 2. MtOperationRpcClient

**类路径**：`org.tarzan.boot.method.client.MtOperationRpcClient`

**主要方法**：
- `operationBasicPropertyGet` - 获取单个工序基本信息（已过期）
- `operationBasicPropertyBatchGet` - 批量获取工序基本信息（已过期）
- `codeLimitOperationBasicBatchQuery` - 根据编码批量查询工序基本信息（已过期）
- `operationPropertyGet` - 获取单个工序详细信息（已过期）
- `operationPropertyBatchGet` - 批量获取工序详细信息（已过期）
- `operationLimitOperationQuery` - 查询工序（已过期）
- `operationLimitOperationBatchQuery` - 批量查询工序（已过期）
- `operationBatchGet` - 批量获取工序信息
- `operationGet` - 获取单个工序信息
- `operationAllVersionQuery` - 查询工序所有版本
- `operationCurrentVersionGet` - 获取工序当前版本
- `operationTypeQuery` - 查询工序类型
- `propertyLimitOperationQuery` - 根据属性查询工序
- `propertyLimitOperationBatchQuery` - 批量根据属性查询工序
- `propertyLimitOperationPropertyQuery` - 根据属性查询工序属性
- `nameLimitOperationBatchQuery` - 根据名称批量查询工序
- `routerOperation` - 获取工艺路线工序
- `routerWorkcell` - 获取工艺路线工作站
- `propertyLimitOperationWkcRelQuery` - 根据属性查询工序工作站关系
- `wkcLimitAvailableOperationQuery` - 根据工作站查询可用工序
- `wkcLimitAvailableOperationBatchQuery` - 批量根据工作站查询可用工序
- `multiOperationAndWkcLimitWkcRelQuery` - 多工序和工作站限制的工作站关系查询
- `operationAvailabilityValidate` - 验证工序是否可用

**用途**：用于查询工序相关信息，支持单个和批量查询，可根据编码查询工序基本信息。

### 3. MtBomRpcClient

**类路径**：`org.tarzan.boot.method.client.MtBomRpcClient`

**主要方法**：
- `bomBasicPropertyGet` - 获取单个BOM基本信息（已过期）
- `bomBasicPropertyBatchGet` - 批量获取BOM基本信息（已过期）
- `codeLimitBomBasicBatchQuery` - 根据编码批量查询BOM基本信息（已过期）
- `bomPropertyGet` - 获取单个BOM详细信息（已过期）
- `bomPropertyBatchGet` - 批量获取BOM详细信息（已过期）
- `bomLimitBomQuery` - 查询BOM（已过期）
- `bomLimitBomBatchQuery` - 批量查询BOM（已过期）
- `bomAllQuery` - BOM全量查询
- `bomAllBatchQuery` - 批量进行BOM全量查询
- `bomBasicGet` - 获取BOM基本信息
- `bomBasicBatchGet` - 批量获取BOM基本信息
- `materialLimitBomComponentBatchQuery` - 根据物料批量查询BOM组件
- `bomComponentQtyBatchCalculate` - 批量计算BOM组件数量
- `bomAvailableValidate` - 验证BOM是否可用
- `bomAvailableBatchValidate` - 批量验证BOM是否可用
- `bomBasicBatchTripleGet` - 批量获取BOM基本信息（三重）
- `bomAllBatchTripleQuery` - 批量进行BOM全量查询（三重）
- `bomAvailableBatchTripleValidate` - 批量验证BOM是否可用（三重）
- `bomComponentQtyBatchTripleCalculate` - 批量计算BOM组件数量（三重）

**用途**：用于查询BOM（物料清单）相关信息，支持单个和批量查询，可根据编码查询BOM基本信息。

### 4. MtProdVersionRpcClient

**类路径**：`org.tarzan.boot.method.client.MtProdVersionRpcClient`

**主要方法**：
- `prodVersionBasicPropertyGet` - 获取单个工艺版本基本信息（已过期）
- `prodVersionBasicPropertyBatchGet` - 批量获取工艺版本基本信息（已过期）
- `codeLimitProdVersionBasicBatchQuery` - 根据编码批量查询工艺版本基本信息（已过期）
- `prodVersionPropertyGet` - 批量获取工艺版本详细信息
- `prodVersionPropertyBatchGet` - 批量获取工艺版本详细信息（已过期）
- `prodVersionLimitProdVersionQuery` - 查询工艺版本（已过期）
- `prodVersionLimitProdVersionBatchQuery` - 批量查询工艺版本（已过期）
- `propertyLimitProdVersionPropertyQuery` - 根据属性查询工艺版本属性
- `productionVersionCodeLimitGet` - 根据编码查询工艺版本
- `materialSiteLimitProdVersionQuery` - 根据物料站点查询工艺版本
- `prodVersionAvailableValidate` - 验证工艺版本是否可用
- `prodVersionCodeAvailableValidate` - 根据编码验证工艺版本是否可用

**用途**：用于查询工艺版本相关信息，支持单个和批量查询，可根据编码查询工艺版本基本信息。

### 5. MtMethodAttrRpcClient

**类路径**：`org.tarzan.boot.method.client.MtMethodAttrRpcClient`

**主要方法**：
- `disRouteAttrPropertyGet` - 获取单个工艺路线属性信息（已过期）
- `disRouteAttrPropertyBatchGet` - 批量获取工艺路线属性信息（已过期）
- `disRouteAttrLimitDisRouteAttrQuery` - 查询工艺路线属性（已过期）
- `disRouteAttrLimitDisRouteAttrBatchQuery` - 批量查询工艺路线属性（已过期）
- `disOperationAttrPropertyGet` - 获取单个工序属性信息（已过期）
- `disOperationAttrPropertyBatchGet` - 批量获取工序属性信息（已过期）
- `disOperationAttrLimitDisOperationAttrQuery` - 查询工序属性（已过期）
- `disOperationAttrLimitDisOperationAttrBatchQuery` - 批量查询工序属性（已过期）
- `attrDataQuery` - 查询属性数据
- `attrPropertyQuery` - 查询属性
- `attrPropertyBatchQuery` - 批量查询属性
- `attrPropertyLimitKeyIdQuery` - 根据属性查询键ID
- `attrPropertyLimitKeyIdBatchQuery` - 批量根据属性查询键ID

**用途**：用于查询工艺方法属性相关信息，支持单个和批量查询，可查询工艺路线和工序的属性信息。

## 使用示例

### 示例1：批量获取物料详细信息（推荐）

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.materialPropertyBatchGet(tenantId, materialIds);
Map<Long, String> materialCodeMap = materials.stream()
    .collect(Collectors.toMap(MtMaterialBaseVO::getMaterialId, MtMaterialBaseVO::getMaterialCode));
```

### 示例2：批量获取工艺路线基本信息

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
5. 物料、工艺路线、工序、BOM等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法
6. 方法属性查询用于获取工艺路线和工序的扩展属性信息
7. 以下物料相关方法已过期，建议使用替代方法：
   - materialBasicPropertyGet → 建议使用 materialPropertyGet
   - materialBasicPropertyBatchGet → 建议使用 materialPropertyBatchGet

8. 以下工艺路线相关方法已过期：
   - routerBasicPropertyGet
   - routerBasicPropertyBatchGet
   - codeLimitRouterBasicBatchQuery
   - routerPropertyGet
   - routerPropertyBatchGet
   - routerLimitRouterQuery
   - routerLimitRouterBatchQuery
   建议使用新的方法如 routerGet、routerBatchGet、routerAllQuery 等。

9. 以下工序相关方法已过期：
   - operationBasicPropertyGet
   - operationBasicPropertyBatchGet
   - codeLimitOperationBasicBatchQuery
   - operationPropertyGet
   - operationPropertyBatchGet
   - operationLimitOperationQuery
   - operationLimitOperationBatchQuery
   建议使用新的方法如 operationGet、operationBatchGet、propertyLimitOperationQuery 等。

10. 以下BOM相关方法已过期：
    - bomBasicPropertyGet
    - bomBasicPropertyBatchGet
    - codeLimitBomBasicBatchQuery
    - bomPropertyGet
    - bomPropertyBatchGet
    - bomLimitBomQuery
    - bomLimitBomBatchQuery
    建议使用新的方法如 bomBasicGet、bomBasicBatchGet、bomAllQuery 等。

11. 以下工艺版本相关方法已过期：
    - prodVersionBasicPropertyGet
    - prodVersionBasicPropertyBatchGet
    - codeLimitProdVersionBasicBatchQuery
    - prodVersionPropertyBatchGet
    - prodVersionLimitProdVersionQuery
    - prodVersionLimitProdVersionBatchQuery
    建议使用新的方法如 prodVersionPropertyGet、productionVersionCodeLimitGet 等。

12. 以下方法属性相关方法已过期：
    - disRouteAttrPropertyGet
    - disRouteAttrPropertyBatchGet
    - disRouteAttrLimitDisRouteAttrQuery
    - disRouteAttrLimitDisRouteAttrBatchQuery
    - disOperationAttrPropertyGet
    - disOperationAttrPropertyBatchGet
    - disOperationAttrLimitDisOperationAttrQuery
    - disOperationAttrLimitDisOperationAttrBatchQuery
    建议使用新的方法如 attrDataQuery、attrPropertyQuery 等。