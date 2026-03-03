# Method模块跨服务接口文档

## 概述

Method模块包含了工艺方法相关的跨服务接口，用于查询和管理物料、工艺路线、工序、BOM、工艺版本和方法属性等。

## 接口列表

### 1. MtMaterialRpcClient

**类路径**：`org.tarzan.boot.method.client.MtMaterialRpcClient`

**主要方法**：
- `codeLimitMaterialBasicBatchQuery` - 根据编码批量查询物料基本信息
- `materialPropertyGet` - 获取单个物料详细信息
- `materialPropertyBatchGet` - 批量获取物料详细信息
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
- `materialCategoryAssignByMaterilSiteIds` - 根据物料站点ID获取物料分类分配
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
- `routerAllQuery` - 工艺路线全量查询
- `routerAllBatchQuery` - 批量进行工艺路线全量查询
- `routerStepBatchGet` - 批量获取工艺路线步骤信息
- `routerLimitRouterStepBatchQuery` - 批量查询工艺路线步骤
- `routerGet` - 获取工艺路线信息
- `routerSiteLimitRelBatchQuery` - 批量查询工艺路线站点关联
- `routerBatchGet` - 批量获取工艺路线信息
- `routerAvailableBatchValidate` - 批量验证工艺路线是否可用

**用途**：用于查询工艺路线相关信息，支持单个和批量查询，可根据编码查询工艺路线基本信息。

### 3. MtOperationRpcClient

**类路径**：`org.tarzan.boot.method.client.MtOperationRpcClient`

**主要方法**：
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

### 4. MtBomRpcClient

**类路径**：`org.tarzan.boot.method.client.MtBomRpcClient`

**主要方法**：
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

### 5. MtProdVersionRpcClient

**类路径**：`org.tarzan.boot.method.client.MtProdVersionRpcClient`

**主要方法**：
- `prodVersionPropertyGet` - 批量获取工艺版本详细信息
- `propertyLimitProdVersionPropertyQuery` - 根据属性查询工艺版本属性
- `productionVersionCodeLimitGet` - 根据编码查询工艺版本
- `materialSiteLimitProdVersionQuery` - 根据物料站点查询工艺版本
- `prodVersionAvailableValidate` - 验证工艺版本是否可用
- `prodVersionCodeAvailableValidate` - 根据编码验证工艺版本是否可用

**用途**：用于查询工艺版本相关信息，支持单个和批量查询，可根据编码查询工艺版本基本信息。

### 6. MtMethodAttrRpcClient

**类路径**：`org.tarzan.boot.method.client.MtMethodAttrRpcClient`

**主要方法**：
- `attrDataQuery` - 查询属性数据
- `attrPropertyQuery` - 查询属性
- `attrPropertyBatchQuery` - 批量查询属性
- `attrPropertyLimitKeyIdQuery` - 根据属性查询键ID
- `attrPropertyLimitKeyIdBatchQuery` - 批量根据属性查询键ID

**用途**：用于查询工艺方法属性相关信息，支持单个和批量查询，可查询工艺路线和工序的属性信息。

## 使用示例

### 示例1：根据编码批量查询物料基本信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

List<String> materialCodes = Arrays.asList("MAT001", "MAT002");
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.codeLimitMaterialBasicBatchQuery(tenantId, materialCodes);
Map<String, Long> materialIdMap = materials.stream()
    .collect(Collectors.toMap(MtMaterialBaseVO::getMaterialCode, MtMaterialBaseVO::getMaterialId));
```

### 示例2：获取单个物料详细信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialVO;

Long materialId = 1L;
MtMaterialVO material = mtMaterialRpcClient.materialPropertyGet(tenantId, materialId);
System.out.println("物料编码：" + material.getMaterialCode());
System.out.println("物料名称：" + material.getMaterialName());
```

### 示例3：批量获取物料详细信息（推荐）

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialVO> materials = mtMaterialRpcClient.materialPropertyBatchGet(tenantId, materialIds);
Map<Long, String> materialCodeMap = materials.stream()
    .collect(Collectors.toMap(MtMaterialVO::getMaterialId, MtMaterialVO::getMaterialCode));
```

### 示例4：根据条件查询物料属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialVO;
import org.tarzan.method.domain.vo.MtMaterialConditionQueryVO;

MtMaterialConditionQueryVO queryVO = new MtMaterialConditionQueryVO();
queryVO.setMaterialType("RAW_MATERIAL");
queryVO.setEnableFlag("Y");
List<MtMaterialVO> materials = mtMaterialRpcClient.conditionLimitMaterialPropertyQuery(tenantId, queryVO);
```

### 示例5：根据属性查询物料属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialVO;
import org.tarzan.method.domain.vo.MtMaterialPropertyQueryVO;

MtMaterialPropertyQueryVO queryVO = new MtMaterialPropertyQueryVO();
queryVO.setMaterialType("RAW_MATERIAL");
List<MtMaterialVO> materials = mtMaterialRpcClient.propertyLimitMaterialPropertyQuery(tenantId, queryVO);
```

### 示例6：根据编码列表查询物料属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialVO;

List<String> materialCodes = Arrays.asList("MAT001", "MAT002");
List<MtMaterialVO> materials = mtMaterialRpcClient.codeListLimitMaterialPropertyQuery(tenantId, materialCodes);
```

### 示例7：根据计量单位查询物料

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

Long uomId = 1L;
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.uomLimitMaterialQuery(tenantId, uomId);
```

### 示例8：根据名称查询物料

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

String materialName = "测试物料";
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.nameLimitMaterialQuery(tenantId, materialName);
```

### 示例9：根据属性查询物料ID

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;

Long materialId = mtMaterialRpcClient.propertyLimitMaterialGet(tenantId, "MAT001");
System.out.println("物料ID：" + materialId);
```

### 示例10：获取单个物料的计量单位

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialUomVO;

Long materialId = 1L;
MtMaterialUomVO materialUom = mtMaterialRpcClient.materialUomGet(tenantId, materialId);
System.out.println("主计量单位：" + materialUom.getPrimaryUomCode());
```

### 示例11：批量获取物料的计量单位

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialUomVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialUomVO> materialUoms = mtMaterialRpcClient.materialUomBatchGet(tenantId, materialIds);
Map<Long, String> primaryUomMap = materialUoms.stream()
    .collect(Collectors.toMap(MtMaterialUomVO::getMaterialId, MtMaterialUomVO::getPrimaryUomCode));
```

### 示例12：物料计量单位转换

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialUomConvertVO;

MtMaterialUomConvertVO convertVO = new MtMaterialUomConvertVO();
convertVO.setMaterialId(1L);
convertVO.setFromUomId(2L);
convertVO.setToUomId(3L);
convertVO.setQuantity(new BigDecimal(10));
BigDecimal convertedQuantity = mtMaterialRpcClient.materialUomConversion(tenantId, convertVO);
System.out.println("转换后的数量：" + convertedQuantity);
```

### 示例13：验证物料双重计量单位

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialDualUomValidateVO;

MtMaterialDualUomValidateVO validateVO = new MtMaterialDualUomValidateVO();
validateVO.setMaterialId(1L);
validateVO.setPrimaryUomId(2L);
validateVO.setSecondaryUomId(3L);
boolean isValid = mtMaterialRpcClient.materialDualUomValidate(tenantId, validateVO);
System.out.println("双重计量单位是否有效：" + isValid);
```

### 示例14：批量验证物料双重计量单位

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialDualUomValidateVO;

List<MtMaterialDualUomValidateVO> validateVOs = new ArrayList<>();
MtMaterialDualUomValidateVO validateVO1 = new MtMaterialDualUomValidateVO();
validateVO1.setMaterialId(1L);
validateVO1.setPrimaryUomId(2L);
validateVO1.setSecondaryUomId(3L);
validateVOs.add(validateVO1);

MtMaterialDualUomValidateVO validateVO2 = new MtMaterialDualUomValidateVO();
validateVO2.setMaterialId(4L);
validateVO2.setPrimaryUomId(5L);
validateVO2.setSecondaryUomId(6L);
validateVOs.add(validateVO2);

List<Boolean> results = mtMaterialRpcClient.materialDualUomBatchValidate(tenantId, validateVOs);
```

### 示例15：验证物料计量单位类型

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialUomTypeValidateVO;

MtMaterialUomTypeValidateVO validateVO = new MtMaterialUomTypeValidateVO();
validateVO.setMaterialId(1L);
validateVO.setUomId(2L);
boolean isValid = mtMaterialRpcClient.materialUomTypeValidate(tenantId, validateVO);
System.out.println("计量单位类型是否有效：" + isValid);
```

### 示例16：批量验证物料计量单位类型

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialUomTypeValidateVO;

List<MtMaterialUomTypeValidateVO> validateVOs = new ArrayList<>();
MtMaterialUomTypeValidateVO validateVO1 = new MtMaterialUomTypeValidateVO();
validateVO1.setMaterialId(1L);
validateVO1.setUomId(2L);
validateVOs.add(validateVO1);

MtMaterialUomTypeValidateVO validateVO2 = new MtMaterialUomTypeValidateVO();
validateVO2.setMaterialId(3L);
validateVO2.setUomId(4L);
validateVOs.add(validateVO2);

List<Boolean> results = mtMaterialRpcClient.materialUomTypeBatchValidate(tenantId, validateVOs);
```

### 示例17：查询物料BOM关系

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBomRelVO;
import org.tarzan.method.domain.vo.MtMaterialBomRelQueryVO;

MtMaterialBomRelQueryVO queryVO = new MtMaterialBomRelQueryVO();
queryVO.setMaterialId(1L);
List<MtMaterialBomRelVO> bomRels = mtMaterialRpcClient.propertyLimitMaterialBomRelQuery(tenantId, queryVO);
```

### 示例18：获取物料分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

Long categoryId = 1L;
MtMaterialCategoryVO category = mtMaterialRpcClient.materialCategoryGet(tenantId, categoryId);
System.out.println("分类编码：" + category.getCategoryCode());
System.out.println("分类名称：" + category.getCategoryName());
```

### 示例19：根据编码获取物料分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

String categoryCode = "CAT001";
MtMaterialCategoryVO category = mtMaterialRpcClient.materialCategoryCodeGet(tenantId, categoryCode);
System.out.println("分类ID：" + category.getCategoryId());
```

### 示例20：批量获取物料分类属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

List<Long> categoryIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategoryVO> categories = mtMaterialRpcClient.materialCategoryPropertyBatchGet(tenantId, categoryIds);
Map<Long, String> categoryNameMap = categories.stream()
    .collect(Collectors.toMap(MtMaterialCategoryVO::getCategoryId, MtMaterialCategoryVO::getCategoryName));
```

### 示例21：批量获取物料分类集

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategorySetVO;

List<Long> setIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategorySetVO> categorySets = mtMaterialRpcClient.materialCategorySetBatchGet(tenantId, setIds);
Map<Long, String> setNameMap = categorySets.stream()
    .collect(Collectors.toMap(MtMaterialCategorySetVO::getSetId, MtMaterialCategorySetVO::getSetName));
```

### 示例22：根据分类集查询物料分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

Long setId = 1L;
List<MtMaterialCategoryVO> categories = mtMaterialRpcClient.setLimitMaterialCategoryQuery(tenantId, setId);
```

### 示例23：根据属性查询物料分类属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;
import org.tarzan.method.domain.vo.MtMaterialCategoryPropertyQueryVO;

MtMaterialCategoryPropertyQueryVO queryVO = new MtMaterialCategoryPropertyQueryVO();
queryVO.setSetId(1L);
List<MtMaterialCategoryVO> categories = mtMaterialRpcClient.propertyLimitMaterialCategoryPropertyQuery(tenantId, queryVO);
```

### 示例24：根据编码列表查询物料分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

List<String> categoryCodes = Arrays.asList("CAT001", "CAT002");
List<MtMaterialCategoryVO> categories = mtMaterialRpcClient.codeListLimitMaterialCategoryQuery(tenantId, categoryCodes);
```

### 示例25：根据编码查询物料分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryVO;

String categoryCode = "CAT001";
MtMaterialCategoryVO category = mtMaterialRpcClient.codeLimitMaterialCategoryQuery(tenantId, categoryCode);
```

### 示例26：获取默认分类集的物料分配分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

Long materialId = 1L;
MtMaterialCategoryAssignVO assignCategory = mtMaterialRpcClient.defaultSetMaterialAssignCategoryGet(tenantId, materialId);
System.out.println("分配分类ID：" + assignCategory.getCategoryId());
```

### 示例27：根据分类集获取物料分配分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

Long materialId = 1L;
Long setId = 2L;
MtMaterialCategoryAssignVO assignCategory = mtMaterialRpcClient.setLimitMaterialAssignCategoryGet(tenantId, materialId, setId);
System.out.println("分配分类ID：" + assignCategory.getCategoryId());
```

### 示例28：批量获取默认分类集的物料分配分类

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategoryAssignVO> assignCategories = mtMaterialRpcClient.defaultSetMaterialAssignCategoryBatchGet(tenantId, materialIds);
Map<Long, Long> materialCategoryMap = assignCategories.stream()
    .collect(Collectors.toMap(MtMaterialCategoryAssignVO::getMaterialId, MtMaterialCategoryAssignVO::getCategoryId));
```

### 示例29：批量获取物料分类分配

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

List<Long> categoryIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategoryAssignVO> assignCategories = mtMaterialRpcClient.materialCategoryLimitAssignBatchGet(tenantId, categoryIds);
```

### 示例30：根据物料站点ID获取物料分类分配

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

List<Long> materialSiteIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategoryAssignVO> assignCategories = mtMaterialRpcClient.materialCategoryAssignByMaterilSiteIds(tenantId, materialSiteIds);
```

### 示例31：根据分类ID查询物料分类分配

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategoryAssignVO;

Long categoryId = 1L;
List<MtMaterialCategoryAssignVO> assignCategories = mtMaterialRpcClient.categoryIdLimitQuery(tenantId, categoryId);
```

### 示例32：验证物料分类是否启用

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;

Long categoryId = 1L;
boolean isEnabled = mtMaterialRpcClient.materialCategoryEnableValidate(tenantId, categoryId);
System.out.println("物料分类是否启用：" + isEnabled);
```

### 示例33：验证默认分类集

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;

boolean isDefault = mtMaterialRpcClient.defaultCategorySetValidate(tenantId, 1L);
System.out.println("是否为默认分类集：" + isDefault);
```

### 示例34：批量查询物料的站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.materialLimitSiteBatchQuery(tenantId, materialIds);
```

### 示例35：根据物料站点ID批量查询

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

List<Long> materialSiteIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.materialSiteIdLimitBatchQuery(tenantId, materialSiteIds);
```

### 示例36：根据物料ID查询物料站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.queryMaterialSiteByMaterialId(tenantId, materialIds);
```

### 示例37：根据物料ID和站点ID查询物料站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;
import org.tarzan.method.domain.vo.MtMaterialSiteQueryVO;

MtMaterialSiteQueryVO queryVO = new MtMaterialSiteQueryVO();
queryVO.setMaterialId(1L);
queryVO.setSiteId(2L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.materialSiteListLimitMaterialSiteQuery(tenantId, queryVO);
```

### 示例38：批量查询物料站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;
import org.tarzan.method.domain.vo.MtMaterialSiteQueryVO;

List<MtMaterialSiteQueryVO> queryVOs = new ArrayList<>();
MtMaterialSiteQueryVO queryVO1 = new MtMaterialSiteQueryVO();
queryVO1.setMaterialId(1L);
queryVO1.setSiteId(2L);
queryVOs.add(queryVO1);

MtMaterialSiteQueryVO queryVO2 = new MtMaterialSiteQueryVO();
queryVO2.setMaterialId(3L);
queryVO2.setSiteId(4L);
queryVOs.add(queryVO2);

List<List<MtMaterialSiteBaseVO>> results = mtMaterialRpcClient.materialSiteListLimitMaterialSiteBatchQuery(tenantId, queryVOs);
```

### 示例39：根据物料站点ID查询

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

Long materialSiteId = 1L;
MtMaterialSiteBaseVO materialSite = mtMaterialRpcClient.queryByMaterialSiteId(tenantId, materialSiteId);
System.out.println("物料ID：" + materialSite.getMaterialId());
System.out.println("站点ID：" + materialSite.getSiteId());
```

### 示例40：根据属性查询物料站点属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;
import org.tarzan.method.domain.vo.MtMaterialSitePropertyQueryVO;

MtMaterialSitePropertyQueryVO queryVO = new MtMaterialSitePropertyQueryVO();
queryVO.setMaterialId(1L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.propertyLimitMaterialSitePropertyQuery(tenantId, queryVO);
```

### 示例41：根据Make/Buy编码批量获取属性

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMakeBuyVO;

List<String> makeBuyCodes = Arrays.asList("MAKE", "BUY");
List<MtMakeBuyVO> makeBuys = mtMaterialRpcClient.makeBuyCodeLimitPropertyBatchGet(tenantId, makeBuyCodes);
Map<String, String> makeBuyDescMap = makeBuys.stream()
    .collect(Collectors.toMap(MtMakeBuyVO::getMakeBuyCode, MtMakeBuyVO::getMakeBuyDesc));
```

### 示例42：根据分类站点查询物料

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

Long categorySiteId = 1L;
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.categorySiteLimitMaterialQuery(tenantId, categorySiteId);
```

### 示例43：批量根据分类站点查询物料

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

List<Long> categorySiteIds = Arrays.asList(1L, 2L, 3L);
List<List<MtMaterialBaseVO>> results = mtMaterialRpcClient.categorySiteLimitMaterialBatchQuery(tenantId, categorySiteIds);
```

### 示例44：批量验证物料分类站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategorySiteValidateVO;

List<MtMaterialCategorySiteValidateVO> validateVOs = new ArrayList<>();
MtMaterialCategorySiteValidateVO validateVO1 = new MtMaterialCategorySiteValidateVO();
validateVO1.setCategoryId(1L);
validateVO1.setSiteId(2L);
validateVOs.add(validateVO1);

MtMaterialCategorySiteValidateVO validateVO2 = new MtMaterialCategorySiteValidateVO();
validateVO2.setCategoryId(3L);
validateVO2.setSiteId(4L);
validateVOs.add(validateVO2);

List<Boolean> results = mtMaterialRpcClient.materialCategorySiteBatchValidate(tenantId, validateVOs);
```

### 示例45：验证物料分类站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategorySiteValidateVO;

MtMaterialCategorySiteValidateVO validateVO = new MtMaterialCategorySiteValidateVO();
validateVO.setCategoryId(1L);
validateVO.setSiteId(2L);
boolean isValid = mtMaterialRpcClient.materialCategorySiteValidate(tenantId, validateVO);
System.out.println("物料分类站点是否有效：" + isValid);
```

### 示例46：根据物料分类站点ID选择

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialCategorySiteVO;

List<Long> categorySiteIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialCategorySiteVO> categorySites = mtMaterialRpcClient.selectByMaterialCategorySiteIds(tenantId, categorySiteIds);
```

### 示例47：根据物料分类站点查询物料站点

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

Long categorySiteId = 1L;
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.materialCategorySiteLimitMaterialSiteQuery(tenantId, categorySiteId);
```

### 示例48：根据条件选择物料ID列表

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialConditionQueryVO;

MtMaterialConditionQueryVO queryVO = new MtMaterialConditionQueryVO();
queryVO.setMaterialType("RAW_MATERIAL");
List<Long> materialIds = mtMaterialRpcClient.selectMaterialIdListByCondition(tenantId, queryVO);
```

### 示例49：批量获取物料GHG信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialGhgVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialGhgVO> ghgInfos = mtMaterialRpcClient.materialGhgBatchGet(tenantId, materialIds);
Map<Long, MtMaterialGhgVO> ghgInfoMap = ghgInfos.stream()
    .collect(Collectors.toMap(MtMaterialGhgVO::getMaterialId, ghg -> ghg));
```

### 示例50：根据标志批量获取

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

String flag = "ACTIVE";
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.flagLimitBatchGet(tenantId, flag);
```

### 示例51：批量验证物料版本是否可用

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialRevisionValidateVO;

List<MtMaterialRevisionValidateVO> validateVOs = new ArrayList<>();
MtMaterialRevisionValidateVO validateVO1 = new MtMaterialRevisionValidateVO();
validateVO1.setMaterialId(1L);
validateVO1.setRevision("A");
validateVOs.add(validateVO1);

MtMaterialRevisionValidateVO validateVO2 = new MtMaterialRevisionValidateVO();
validateVO2.setMaterialId(2L);
validateVO2.setRevision("B");
validateVOs.add(validateVO2);

List<Boolean> results = mtMaterialRpcClient.materialRevisionAvailableValidate(tenantId, validateVOs);
```

### 示例52：验证物料版本是否可用

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;

Long materialId = 1L;
String revision = "A";
boolean isAvailable = mtMaterialRpcClient.materialRevisionAvailableValidateSelf(tenantId, materialId, revision);
System.out.println("物料版本是否可用：" + isAvailable);
```

### 示例53：工艺路线全量查询

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterTotalVO;

MtRouterTotalVO router = mtRouterRpcClient.routerAllQuery(tenantId, 1L);
System.out.println("工艺路线编码：" + router.getRouterCode());
System.out.println("工艺路线名称：" + router.getRouterName());
```

### 示例54：批量进行工艺路线全量查询

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterTotalVO;

List<Long> routerIds = Arrays.asList(1L, 2L, 3L);
List<MtRouterTotalVO> routers = mtRouterRpcClient.routerAllBatchQuery(tenantId, routerIds);
Map<Long, String> routerNameMap = routers.stream()
    .collect(Collectors.toMap(MtRouterTotalVO::getRouterId, MtRouterTotalVO::getRouterName));
```

### 示例55：批量获取工艺路线步骤信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterStepVO;

List<Long> routerIds = Arrays.asList(1L, 2L, 3L);
List<List<MtRouterStepVO>> stepsList = mtRouterRpcClient.routerStepBatchGet(tenantId, routerIds);
```

### 示例56：批量查询工艺路线步骤

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterStepVO;
import org.tarzan.method.domain.vo.MtRouterStepQueryVO;

List<MtRouterStepQueryVO> queryVOs = new ArrayList<>();
MtRouterStepQueryVO queryVO1 = new MtRouterStepQueryVO();
queryVO1.setRouterId(1L);
queryVOs.add(queryVO1);

MtRouterStepQueryVO queryVO2 = new MtRouterStepQueryVO();
queryVO2.setRouterId(2L);
queryVOs.add(queryVO2);

List<List<MtRouterStepVO>> results = mtRouterRpcClient.routerLimitRouterStepBatchQuery(tenantId, queryVOs);
```

### 示例57：获取工艺路线信息

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterTotalVO;

Long routerId = 1L;
MtRouterTotalVO router = mtRouterRpcClient.routerGet(tenantId, routerId);
System.out.println("工艺路线编码：" + router.getRouterCode());
```

### 示例58：批量查询工艺路线站点关联

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterSiteRelVO;
import org.tarzan.method.domain.vo.MtRouterSiteRelQueryVO;

List<MtRouterSiteRelQueryVO> queryVOs = new ArrayList<>();
MtRouterSiteRelQueryVO queryVO1 = new MtRouterSiteRelQueryVO();
queryVO1.setRouterId(1L);
queryVOs.add(queryVO1);

MtRouterSiteRelQueryVO queryVO2 = new MtRouterSiteRelQueryVO();
queryVO2.setRouterId(2L);
queryVOs.add(queryVO2);

List<List<MtRouterSiteRelVO>> results = mtRouterRpcClient.routerSiteLimitRelBatchQuery(tenantId, queryVOs);
```

### 示例59：批量获取工艺路线详细信息（推荐）

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;
import org.tarzan.method.domain.vo.MtRouterTotalVO;

List<Long> routerIds = Arrays.asList(1L, 2L, 3L);
List<MtRouterTotalVO> routers = mtRouterRpcClient.routerBatchGet(tenantId, routerIds);
Map<Long, String> routerCodeMap = routers.stream()
    .collect(Collectors.toMap(MtRouterTotalVO::getRouterId, MtRouterTotalVO::getRouterCode));
```

### 示例60：批量验证工艺路线是否可用

```java
import org.tarzan.boot.method.client.MtRouterRpcClient;

List<Long> routerIds = Arrays.asList(1L, 2L, 3L);
List<Boolean> results = mtRouterRpcClient.routerAvailableBatchValidate(tenantId, routerIds);
```

### 示例61：批量获取工序信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;

List<Long> operationIds = Arrays.asList(1L, 2L, 3L);
List<MtOperationVO> operations = mtOperationRpcClient.operationBatchGet(tenantId, operationIds);
Map<Long, String> operationCodeMap = operations.stream()
    .collect(Collectors.toMap(MtOperationVO::getOperationId, MtOperationVO::getOperationCode));
```

### 示例62：获取单个工序信息

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;

Long operationId = 1L;
MtOperationVO operation = mtOperationRpcClient.operationGet(tenantId, operationId);
System.out.println("工序编码：" + operation.getOperationCode());
System.out.println("工序名称：" + operation.getOperationName());
```

### 示例63：查询工序所有版本

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;

Long operationId = 1L;
List<MtOperationVO> versions = mtOperationRpcClient.operationAllVersionQuery(tenantId, operationId);
```

### 示例64：获取工序当前版本

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;

Long operationId = 1L;
MtOperationVO currentVersion = mtOperationRpcClient.operationCurrentVersionGet(tenantId, operationId);
System.out.println("当前版本：" + currentVersion.getRevision());
```

### 示例65：查询工序类型

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationTypeVO;

List<MtOperationTypeVO> operationTypes = mtOperationRpcClient.operationTypeQuery(tenantId);
```

### 示例66：根据属性查询工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;
import org.tarzan.method.domain.vo.MtOperationQueryVO;

MtOperationQueryVO queryVO = new MtOperationQueryVO();
queryVO.setOperationType("ASSEMBLY");
List<MtOperationBaseVO> operations = mtOperationRpcClient.propertyLimitOperationQuery(tenantId, queryVO);
```

### 示例67：批量根据属性查询工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;
import org.tarzan.method.domain.vo.MtOperationQueryVO;

List<MtOperationQueryVO> queryVOs = new ArrayList<>();
MtOperationQueryVO queryVO1 = new MtOperationQueryVO();
queryVO1.setOperationType("ASSEMBLY");
queryVOs.add(queryVO1);

MtOperationQueryVO queryVO2 = new MtOperationQueryVO();
queryVO2.setOperationType("TEST");
queryVOs.add(queryVO2);

List<List<MtOperationBaseVO>> results = mtOperationRpcClient.propertyLimitOperationBatchQuery(tenantId, queryVOs);
```

### 示例68：根据属性查询工序属性

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationVO;
import org.tarzan.method.domain.vo.MtOperationPropertyQueryVO;

MtOperationPropertyQueryVO queryVO = new MtOperationPropertyQueryVO();
queryVO.setOperationType("ASSEMBLY");
List<MtOperationVO> operations = mtOperationRpcClient.propertyLimitOperationPropertyQuery(tenantId, queryVO);
```

### 示例69：根据编码批量查询工序基本信息（推荐）

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

List<String> operationCodes = Arrays.asList("OP001", "OP002");
List<MtOperationBaseVO> operations = mtOperationRpcClient.nameLimitOperationBatchQuery(tenantId, operationCodes);
Map<String, Long> operationIdMap = operations.stream()
    .collect(Collectors.toMap(MtOperationBaseVO::getOperationCode, MtOperationBaseVO::getOperationId));
```

### 示例70：获取工艺路线工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

Long routerId = 1L;
List<MtOperationBaseVO> operations = mtOperationRpcClient.routerOperation(tenantId, routerId);
```

### 示例71：获取工艺路线工作站

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtWorkcellBaseVO;

Long routerId = 1L;
List<MtWorkcellBaseVO> workcells = mtOperationRpcClient.routerWorkcell(tenantId, routerId);
```

### 示例72：根据属性查询工序工作站关系

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationWkcRelVO;
import org.tarzan.method.domain.vo.MtOperationWkcRelQueryVO;

MtOperationWkcRelQueryVO queryVO = new MtOperationWkcRelQueryVO();
queryVO.setOperationId(1L);
List<MtOperationWkcRelVO> relations = mtOperationRpcClient.propertyLimitOperationWkcRelQuery(tenantId, queryVO);
```

### 示例73：根据工作站查询可用工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

Long workcellId = 1L;
List<MtOperationBaseVO> operations = mtOperationRpcClient.wkcLimitAvailableOperationQuery(tenantId, workcellId);
```

### 示例74：批量根据工作站查询可用工序

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationBaseVO;

List<Long> workcellIds = Arrays.asList(1L, 2L, 3L);
List<List<MtOperationBaseVO>> results = mtOperationRpcClient.wkcLimitAvailableOperationBatchQuery(tenantId, workcellIds);
```

### 示例75：多工序和工作站限制的工作站关系查询

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;
import org.tarzan.method.domain.vo.MtOperationWkcRelVO;
import org.tarzan.method.domain.vo.MtMultiOperationWkcRelQueryVO;

MtMultiOperationWkcRelQueryVO queryVO = new MtMultiOperationWkcRelQueryVO();
queryVO.setOperationIds(Arrays.asList(1L, 2L));
queryVO.setWorkcellIds(Arrays.asList(3L, 4L));
List<MtOperationWkcRelVO> relations = mtOperationRpcClient.multiOperationAndWkcLimitWkcRelQuery(tenantId, queryVO);
```

### 示例76：验证工序是否可用

```java
import org.tarzan.boot.method.client.MtOperationRpcClient;

Long operationId = 1L;
boolean isAvailable = mtOperationRpcClient.operationAvailabilityValidate(tenantId, operationId);
System.out.println("工序是否可用：" + isAvailable);
```

### 示例77：BOM全量查询

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomTotalVO;

MtBomTotalVO bom = mtBomRpcClient.bomAllQuery(tenantId, 1L);
System.out.println("BOM编码：" + bom.getBomCode());
System.out.println("BOM名称：" + bom.getBomName());
```

### 示例78：批量进行BOM全量查询

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomTotalVO;

List<Long> bomIds = Arrays.asList(1L, 2L, 3L);
List<MtBomTotalVO> boms = mtBomRpcClient.bomAllBatchQuery(tenantId, bomIds);
Map<Long, String> bomNameMap = boms.stream()
    .collect(Collectors.toMap(MtBomTotalVO::getBomId, MtBomTotalVO::getBomName));
```

### 示例79：获取BOM基本信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomBaseVO;

Long bomId = 1L;
MtBomBaseVO bom = mtBomRpcClient.bomBasicGet(tenantId, bomId);
System.out.println("BOM编码：" + bom.getBomCode());
```

### 示例80：批量获取BOM详细信息（推荐）

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomTotalVO;

List<Long> bomIds = Arrays.asList(1L, 2L, 3L);
List<MtBomTotalVO> boms = mtBomRpcClient.bomBasicBatchGet(tenantId, bomIds);
Map<Long, String> bomNameMap = boms.stream()
    .collect(Collectors.toMap(MtBomTotalVO::getBomId, MtBomTotalVO::getBomName));
```

### 示例81：根据物料批量查询BOM组件

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomComponentVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<List<MtBomComponentVO>> componentsList = mtBomRpcClient.materialLimitBomComponentBatchQuery(tenantId, materialIds);
```

### 示例82：批量计算BOM组件数量

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomComponentQtyCalculateVO;

List<MtBomComponentQtyCalculateVO> calculateVOs = new ArrayList<>();
MtBomComponentQtyCalculateVO calculateVO1 = new MtBomComponentQtyCalculateVO();
calculateVO1.setBomId(1L);
calculateVO1.setQuantity(new BigDecimal(10));
calculateVOs.add(calculateVO1);

MtBomComponentQtyCalculateVO calculateVO2 = new MtBomComponentQtyCalculateVO();
calculateVO2.setBomId(2L);
calculateVO2.setQuantity(new BigDecimal(20));
calculateVOs.add(calculateVO2);

List<List<MtBomComponentQtyCalculateVO>> results = mtBomRpcClient.bomComponentQtyBatchCalculate(tenantId, calculateVOs);
```

### 示例83：验证BOM是否可用

```java
import org.tarzan.boot.method.client.MtBomRpcClient;

Long bomId = 1L;
boolean isAvailable = mtBomRpcClient.bomAvailableValidate(tenantId, bomId);
System.out.println("BOM是否可用：" + isAvailable);
```

### 示例84：批量验证BOM是否可用

```java
import org.tarzan.boot.method.client.MtBomRpcClient;

List<Long> bomIds = Arrays.asList(1L, 2L, 3L);
List<Boolean> results = mtBomRpcClient.bomAvailableBatchValidate(tenantId, bomIds);
```

### 示例85：批量获取工艺版本详细信息

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionVO;

List<Long> prodVersionIds = Arrays.asList(1L, 2L, 3L);
List<MtProdVersionVO> prodVersions = mtProdVersionRpcClient.prodVersionPropertyGet(tenantId, prodVersionIds);
Map<Long, String> prodVersionCodeMap = prodVersions.stream()
    .collect(Collectors.toMap(MtProdVersionVO::getProdVersionId, MtProdVersionVO::getProdVersionCode));
```

### 示例86：根据属性查询工艺版本属性

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionVO;
import org.tarzan.method.domain.vo.MtProdVersionPropertyQueryVO;

MtProdVersionPropertyQueryVO queryVO = new MtProdVersionPropertyQueryVO();
queryVO.setMaterialId(1L);
List<MtProdVersionVO> prodVersions = mtProdVersionRpcClient.propertyLimitProdVersionPropertyQuery(tenantId, queryVO);
```

### 示例87：根据编码查询工艺版本

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionVO;

String prodVersionCode = "PV001";
MtProdVersionVO prodVersion = mtProdVersionRpcClient.productionVersionCodeLimitGet(tenantId, prodVersionCode);
System.out.println("工艺版本ID：" + prodVersion.getProdVersionId());
```

### 示例88：根据物料站点查询工艺版本

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;
import org.tarzan.method.domain.vo.MtProdVersionVO;

Long materialSiteId = 1L;
List<MtProdVersionVO> prodVersions = mtProdVersionRpcClient.materialSiteLimitProdVersionQuery(tenantId, materialSiteId);
```

### 示例89：验证工艺版本是否可用

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;

Long prodVersionId = 1L;
boolean isAvailable = mtProdVersionRpcClient.prodVersionAvailableValidate(tenantId, prodVersionId);
System.out.println("工艺版本是否可用：" + isAvailable);
```

### 示例90：根据编码验证工艺版本是否可用

```java
import org.tarzan.boot.method.client.MtProdVersionRpcClient;

String prodVersionCode = "PV001";
boolean isAvailable = mtProdVersionRpcClient.prodVersionCodeAvailableValidate(tenantId, prodVersionCode);
System.out.println("工艺版本是否可用：" + isAvailable);
```

### 示例91：查询属性数据

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtMethodAttrDataVO;
import org.tarzan.method.domain.vo.MtMethodAttrDataQueryVO;

MtMethodAttrDataQueryVO queryVO = new MtMethodAttrDataQueryVO();
queryVO.setKeyId(1L);
queryVO.setAttrId(2L);
MtMethodAttrDataVO attrData = mtMethodAttrRpcClient.attrDataQuery(tenantId, queryVO);
System.out.println("属性值：" + attrData.getAttrValue());
```

### 示例92：查询属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtMethodAttrVO;

Long attrId = 1L;
MtMethodAttrVO attr = mtMethodAttrRpcClient.attrPropertyQuery(tenantId, attrId);
System.out.println("属性编码：" + attr.getAttrCode());
System.out.println("属性名称：" + attr.getAttrName());
```

### 示例93：批量查询属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtMethodAttrVO;

List<Long> attrIds = Arrays.asList(1L, 2L, 3L);
List<MtMethodAttrVO> attrs = mtMethodAttrRpcClient.attrPropertyBatchQuery(tenantId, attrIds);
Map<Long, String> attrNameMap = attrs.stream()
    .collect(Collectors.toMap(MtMethodAttrVO::getAttrId, MtMethodAttrVO::getAttrName));
```

### 示例94：根据属性查询键ID

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtMethodAttrKeyIdVO;
import org.tarzan.method.domain.vo.MtMethodAttrKeyIdQueryVO;

MtMethodAttrKeyIdQueryVO queryVO = new MtMethodAttrKeyIdQueryVO();
queryVO.setAttrId(1L);
queryVO.setAttrValue("TEST");
List<MtMethodAttrKeyIdVO> keyIds = mtMethodAttrRpcClient.attrPropertyLimitKeyIdQuery(tenantId, queryVO);
```

### 示例95：批量根据属性查询键ID

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtMethodAttrKeyIdVO;
import org.tarzan.method.domain.vo.MtMethodAttrKeyIdQueryVO;

List<MtMethodAttrKeyIdQueryVO> queryVOs = new ArrayList<>();
MtMethodAttrKeyIdQueryVO queryVO1 = new MtMethodAttrKeyIdQueryVO();
queryVO1.setAttrId(1L);
queryVO1.setAttrValue("TEST1");
queryVOs.add(queryVO1);

MtMethodAttrKeyIdQueryVO queryVO2 = new MtMethodAttrKeyIdQueryVO();
queryVO2.setAttrId(2L);
queryVO2.setAttrValue("TEST2");
queryVOs.add(queryVO2);

List<List<MtMethodAttrKeyIdVO>> results = mtMethodAttrRpcClient.attrPropertyLimitKeyIdBatchQuery(tenantId, queryVOs);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 物料、工艺路线、工序、BOM等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法
6. 方法属性查询用于获取工艺路线和工序的扩展属性信息
