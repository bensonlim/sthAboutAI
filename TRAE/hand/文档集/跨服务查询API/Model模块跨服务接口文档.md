# Model模块跨服务接口文档

## 概述

Model模块包含了业务模型相关的跨服务接口，用于查询和管理各种业务实体，如站点、区域、生产线、库位、工作单元和日历等。

## 接口列表

### 1. MtSiteRpcClient

**类路径**：`org.tarzan.boot.model.client.MtSiteRpcClient`

**主要方法**：
- `siteBasicPropertyGet` - 获取单个站点基本信息
- `siteBasicPropertyBatchGet` - 批量获取站点基本信息
- `siteBasicByCodePropertyBatchGet` - 根据编码批量获取站点基本信息
- `codeLimitSiteBasicBatchQuery` - 根据编码批量查询站点基本信息（已过期）
- `sitePropertyGet` - 获取单个站点详细信息（已过期）
- `sitePropertyBatchGet` - 批量获取站点详细信息（已过期）
- `siteLimitSiteQuery` - 查询站点（已过期）
- `siteLimitSiteBatchQuery` - 批量查询站点（已过期）
- `siteSchedulePropertyGet` - 获取单个站点排程信息
- `siteSchedulePropertyBatchGet` - 批量获取站点排程信息
- `siteManufacturingPropertyGet` - 获取单个站点制造信息
- `siteManufacturingPropertyBatchGet` - 批量获取站点制造信息
- `propertyLimitSiteQuery` - 根据属性查询站点
- `propertyLimitSitePropertyQuery` - 根据属性查询站点属性
- `conditionLimitSitePropertyQuery` - 根据条件查询站点属性
- `codeListLimitSitePropertyQuery` - 根据编码列表查询站点属性
- `siteMappingQuery` - 查询站点映射
- `siteLimitAllRelatedSiteQuery` - 查询站点所有相关站点
- `siteMappingBatchQuery` - 批量查询站点映射
- `getRelationByPlantAndSiteType` - 根据工厂和站点类型获取关系
- `siteLimitPlantReleationQuery` - 根据站点查询工厂关系

**用途**：用于查询站点相关信息，支持单个和批量查询，可根据编码查询站点基本信息。

### 3. MtAreaRpcClient

**类路径**：`org.tarzan.boot.model.client.MtAreaRpcClient`

**主要方法**：
- `areaBasicPropertyGet` - 获取单个区域基本信息
- `areaBasicPropertyBatchGet` - 批量获取区域基本信息
- `codeLimitAreaPropertyBatchGet` - 根据编码批量获取区域基本信息
- `codeLimitAreaBasicBatchQuery` - 根据编码批量查询区域基本信息（已过期）
- `areaPropertyGet` - 获取单个区域详细信息（已过期）
- `areaPropertyBatchGet` - 批量获取区域详细信息（已过期）
- `areaLimitAreaQuery` - 查询区域（已过期）
- `areaLimitAreaBatchQuery` - 批量查询区域（已过期）
- `areaPurchasePropertyGet` - 获取单个区域采购信息
- `areaPurchasePropertyBatchGet` - 批量获取区域采购信息
- `areaSchedulePropertyGet` - 获取单个区域排程信息
- `areaSchedulePropertyBatchGet` - 批量获取区域排程信息
- `propertyLimitAreaQuery` - 根据属性查询区域
- `propertyLimitAreaPropertyQuery` - 根据属性查询区域属性
- `propertyLimitAreaSchedulePropertyQuery` - 根据属性查询区域排程属性
- `propertyListLimitAreaSchedulePropertyQuery` - 根据属性列表查询区域排程属性

**用途**：用于查询区域相关信息，支持单个和批量查询，可根据编码查询区域基本信息。

### 4. MtProdLineRpcClient

**类路径**：`org.tarzan.boot.model.client.MtProdLineRpcClient`

**主要方法**：
- `prodLineBasicPropertyGet` - 获取单个生产线基本信息
- `prodLineBasicPropertyBatchGet` - 批量获取生产线基本信息
- `codeListLimitProdLinePropertyQuery` - 根据编码列表查询生产线属性
- `codeLimitProdLineBasicBatchQuery` - 根据编码批量查询生产线基本信息（已过期）
- `prodLinePropertyGet` - 获取单个生产线详细信息（已过期）
- `prodLinePropertyBatchGet` - 批量获取生产线详细信息（已过期）
- `prodLineLimitProdLineQuery` - 查询生产线（已过期）
- `prodLineLimitProdLineBatchQuery` - 批量查询生产线（已过期）
- `prodLineSchedulePropertyGet` - 获取单个生产线排程信息
- `prodLineSchedulePropertyBatchGet` - 批量获取生产线排程信息
- `prodLineManufacturingPropertyGet` - 获取单个生产线制造信息
- `prodLineManufacturingPropertyBatchGet` - 批量获取生产线制造信息
- `propertyLimitProdLineQuery` - 根据属性查询生产线
- `propertyLimitProdLinePropertyQuery` - 根据属性查询生产线属性
- `propertyLimitProdLineManufacturingPropertyQuery` - 根据属性查询生产线制造属性
- `prodLineLimitDispatchOperationQuery` - 根据生产线查询调度工序
- `operationLimitProdLineQuery` - 根据工序查询生产线
- `propertyListLimitProdLineDispatchOperationQuery` - 根据属性列表查询生产线调度工序
- `prodLineDispatchOperationValidate` - 验证生产线调度工序

**用途**：用于查询生产线相关信息，支持单个和批量查询，可根据编码查询生产线基本信息。

### 5. MtLocatorRpcClient

**类路径**：`org.tarzan.boot.model.client.MtLocatorRpcClient`

**主要方法**：
- `locatorBasicPropertyGet` - 获取单个库位基本信息
- `locatorBasicPropertyBatchGet` - 批量获取库位基本信息
- `identificationLimitLocatorBatchGet` - 根据标识批量获取库位基本信息
- `codeLimitLocatorBasicBatchQuery` - 根据编码批量查询库位基本信息（已过期）
- `locatorPropertyGet` - 获取单个库位详细信息（已过期）
- `locatorPropertyBatchGet` - 批量获取库位详细信息（已过期）
- `locatorLimitLocatorQuery` - 查询库位（已过期）
- `locatorLimitLocatorBatchQuery` - 批量查询库位（已过期）
- `subLocatorQuery` - 查询子库位
- `parentLocatorQuery` - 查询父库位
- `locatorListLimitSubLocatorQuery` - 根据库位列表查询子库位
- `locatorListLimitParentLocatorQuery` - 根据库位列表查询父库位
- `locatorSiteRelQuery` - 查询库位站点关系
- `propertyLimitLocatorQuery` - 根据属性查询库位
- `propertyLimitLocatorPropertyQuery` - 根据属性查询库位属性
- `codeListLimitLocatorPropertyQuery` - 根据编码列表查询库位属性
- `locatorLimitInventoryCategoryLocatorGet` - 根据库位查询库存分类库位
- `locatorListLimitInvCategoryLocatorGet` - 根据库位列表查询库存分类库位
- `locatorLimitSubLocatorTree` - 查询库位子库位树
- `locatorLimitSubLocatorTreeBatchQuery` - 批量查询库位子库位树
- `properyLimitLocatorSubinvReleationQuery` - 根据属性查询库位子库存关系
- `parentLocatorAndDepthQuery` - 查询父库位和深度
- `locatorPermissionQuery` - 查询库位权限
- `userOperableAreaLocatorQuery` - 查询用户可操作的区域库位
- `siteLimitLocatorInfoQuery` - 根据站点查询库位信息
- `prodLineLimitInvLocatorQuery` - 根据生产线查询库存库位
- `siteLimitTargetLocationQuery` - 根据站点查询目标位置
- `locatorRecordOnhandVerify` - 验证库位记录在手量
- `locatorExecutionValidate` - 验证库位执行
- `locatorExecutionBatchValidate` - 批量验证库位执行
- `userAreaLocatorExecutionValidate` - 验证用户区域库位执行

**用途**：用于查询库位相关信息，支持单个和批量查询，可根据编码查询库位基本信息。

### 6. MtWorkCellRpcClient

**类路径**：`org.tarzan.boot.model.client.MtWorkCellRpcClient`

**主要方法**：
- `workcellBasicPropertyGet` - 获取单个工作单元基本信息
- `workcellBasicPropertyBatchGet` - 批量获取工作单元基本信息
- `codeLimitWkcPropertyBatchGet` - 根据编码批量获取工作单元基本信息
- `workCellBasicPropertyGet` - 获取单个工作单元基本信息（已过期）
- `workCellBasicPropertyBatchGet` - 批量获取工作单元基本信息（已过期）
- `codeLimitWorkCellBasicBatchQuery` - 根据编码批量查询工作单元基本信息（已过期）
- `workCellPropertyGet` - 获取单个工作单元详细信息（已过期）
- `workCellPropertyBatchGet` - 批量获取工作单元详细信息（已过期）
- `workCellLimitWorkCellQuery` - 查询工作单元（已过期）
- `workCellLimitWorkCellBatchQuery` - 批量查询工作单元（已过期）
- `workcellManufacturingPropertyGet` - 获取单个工作单元制造信息
- `workcellManufacturingPropertyBatchGet` - 批量获取工作单元制造信息
- `propertyLimitWorkcellQuery` - 根据属性查询工作单元
- `propertyLimitWorkcellPropertyQuery` - 根据属性查询工作单元属性
- `propertyLimitWorkcellManufacturingPropertyQuery` - 根据属性查询工作单元制造属性

**用途**：用于查询工作单元相关信息，支持单个和批量查询，可根据编码查询工作单元基本信息。

### 7. MtCalendarRpcClient

**类路径**：`org.tarzan.boot.model.client.MtCalendarRpcClient`

**主要方法**：
- `calendarGet` - 获取日历信息
- `calendarBatchGet` - 批量获取日历信息
- `calendarBasicBatchGetByCode` - 根据编码批量获取日历基本信息
- `calendarBasicPropertyGet` - 获取单个日历基本信息（已过期）
- `calendarBasicPropertyBatchGet` - 批量获取日历基本信息（已过期）
- `codeLimitCalendarBasicBatchQuery` - 根据编码批量查询日历基本信息（已过期）
- `calendarPropertyGet` - 获取单个日历详细信息（已过期）
- `calendarPropertyBatchGet` - 批量获取日历详细信息（已过期）
- `calendarLimitCalendarQuery` - 查询日历（已过期）
- `calendarLimitCalendarBatchQuery` - 批量查询日历（已过期）
- `calendarShiftGet` - 获取日历班次信息
- `calendarShiftBatchGet` - 批量获取日历班次信息
- `calendarLimitCalendarShiftBatchGet` - 根据日历批量获取班次信息
- `orgAndPeriodLimitCalendarShiftQuery` - 根据组织和周期查询日历班次
- `orgAndPeriodLimitCalendarShiftBatchQuery` - 批量根据组织和周期查询日历班次
- `orgAndTimeLimitCalendarShiftGet` - 根据组织和时间获取日历班次
- `orgAndTimeLimitCalendarShiftBatchGet` - 批量根据组织和时间获取日历班次
- `timeLimitWorkDayShiftQuery` - 根据时间查询工作日班次
- `organizationShiftBatchQuery` - 批量查询组织班次
- `organizationLimitOnlyCalendarGet` - 根据组织获取唯一日历
- `organizationLimitOnlyCalendarBatchGet` - 批量根据组织获取唯一日历
- `timeLimitCalendarShiftQuery` - 根据时间查询日历班次
- `timeLimitAvailableCalendarShiftQuery` - 根据时间查询可用日历班次
- `propertyLimitCalendarShiftPropertyQuery` - 根据属性查询日历班次属性
- `calendarLimitShiftQuery` - 根据日历查询班次
- `calendarLimitShiftBatchQuery` - 批量根据日历查询班次
- `calendarLimitOrganizationRelationQuery` - 根据日历查询组织关系
- `dateLimitCalendarShiftGet` - 根据日期获取日历班次
- `organizationLimitCalendarQuery` - 根据组织查询日历
- `propertyLimitCalendarOrganizationRelationQuery` - 根据属性查询日历组织关系
- `propertyLimitCalendarOrganizationRelationBatchQuery` - 批量根据属性查询日历组织关系
- `typeLimitCalendarQuery` - 根据类型查询日历
- `calendarPreviousShiftGet` - 获取日历前一个班次
- `calendarNextShiftGet` - 获取日历下一个班次
- `propertyLimitCalendarPropertyQuery` - 根据属性查询日历属性
- `availableShiftTempletQuery` - 查询可用班次模板
- `calendarShiftLimitNearShiftQuery` - 根据日历班次查询附近班次
- `typeLimitShiftTemplateQuery` - 根据类型查询班次模板
- `shiftTemplateGet` - 获取班次模板
- `propertyLimitShiftTemplatePropertyQuery` - 根据属性查询班次模板属性
- `codeListLimitShiftPropertyQuery` - 根据编码列表查询班次属性
- `supplierLimitCalendarQuery` - 根据供应商查询日历
- `calendarAvailableValidate` - 验证日历是否可用
- `calendarShiftAvailableValidate` - 验证日历班次是否可用

**用途**：用于查询日历相关信息，支持单个和批量查询，可根据编码查询日历基本信息。

### 8. MtOrganizationRpcClient

**类路径**：`org.tarzan.boot.model.client.MtOrganizationRpcClient`

**主要方法**：
- `organizationPropertyGet` - 获取单个组织基本信息
- `organizationPropertyBatchGet` - 批量获取组织基本信息
- `codeListLimitOrganizationPropertyGet` - 根据编码列表获取组织基本信息
- `organizationBasicPropertyGet` - 获取单个组织基本信息（已过期）
- `organizationBasicPropertyBatchGet` - 批量获取组织基本信息（已过期）
- `codeLimitOrganizationBasicBatchQuery` - 根据编码批量查询组织基本信息（已过期）
- `organizationLimitOrganizationQuery` - 查询组织（已过期）
- `organizationLimitOrganizationBatchQuery` - 批量查询组织（已过期）
- `parentOrganizationRelQuery` - 查询父组织关系
- `subOrganizationRelQuery` - 查询子组织关系
- `organizationLimitSchedulePropertyGet` - 根据组织获取排程属性
- `organizationLimitSchedulePropertyBatchGet` - 批量根据组织获取排程属性
- `organizationLimitSameLevelOrganizationQuery` - 查询组织的同级组织
- `parentOrgLimitSubOrgRelTreeQuery` - 根据父组织查询子组织关系树

**用途**：用于查询组织相关信息，支持单个和批量查询，可根据编码查询组织基本信息。

## 使用示例

### 示例1：根据编码批量查询站点基本信息（推荐）

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

List<String> siteCodes = Arrays.asList("SITE001", "SITE002");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.siteBasicByCodePropertyBatchGet(tenantId, siteCodes);
Map<String, Long> siteIdMap = sites.stream()
    .collect(Collectors.toMap(MtModSiteBaseVO::getSiteCode, MtModSiteBaseVO::getSiteId));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 物料、站点、区域等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法

6. 以下站点相关方法已过期：
   - codeLimitSiteBasicBatchQuery
   - sitePropertyGet
   - sitePropertyBatchGet
   - siteLimitSiteQuery
   - siteLimitSiteBatchQuery
   建议使用新的方法如 siteBasicByCodePropertyBatchGet、propertyLimitSitePropertyQuery 等。

7. 以下区域相关方法已过期：
   - codeLimitAreaBasicBatchQuery
   - areaPropertyGet
   - areaPropertyBatchGet
   - areaLimitAreaQuery
   - areaLimitAreaBatchQuery
   建议使用新的方法如 codeLimitAreaPropertyBatchGet、propertyLimitAreaPropertyQuery 等。

8. 以下生产线相关方法已过期：
   - codeLimitProdLineBasicBatchQuery
   - prodLinePropertyGet
   - prodLinePropertyBatchGet
   - prodLineLimitProdLineQuery
   - prodLineLimitProdLineBatchQuery
   建议使用新的方法如 codeListLimitProdLinePropertyQuery、propertyLimitProdLinePropertyQuery 等。

9. 以下库位相关方法已过期：
   - codeLimitLocatorBasicBatchQuery
   - locatorPropertyGet
   - locatorPropertyBatchGet
   - locatorLimitLocatorQuery
   - locatorLimitLocatorBatchQuery
   建议使用新的方法如 identificationLimitLocatorBatchGet、codeListLimitLocatorPropertyQuery 等。

10. 以下工作单元相关方法已过期：
    - workCellBasicPropertyGet
    - workCellBasicPropertyBatchGet
    - codeLimitWorkCellBasicBatchQuery
    - workCellPropertyGet
    - workCellPropertyBatchGet
    - workCellLimitWorkCellQuery
    - workCellLimitWorkCellBatchQuery
    建议使用新的方法如 workcellBasicPropertyGet、workcellBasicPropertyBatchGet、codeLimitWkcPropertyBatchGet 等。

11. 以下日历相关方法已过期：
    - calendarBasicPropertyGet
    - calendarBasicPropertyBatchGet
    - codeLimitCalendarBasicBatchQuery
    - calendarPropertyGet
    - calendarPropertyBatchGet
    - calendarLimitCalendarQuery
    - calendarLimitCalendarBatchQuery
    建议使用新的方法如 calendarGet、calendarBatchGet、calendarBasicBatchGetByCode 等。

12. 以下组织相关方法已过期：
    - organizationBasicPropertyGet
    - organizationBasicPropertyBatchGet
    - codeLimitOrganizationBasicBatchQuery
    - organizationLimitOrganizationQuery
    - organizationLimitOrganizationBatchQuery
    建议使用新的方法如 organizationPropertyGet、organizationPropertyBatchGet、codeListLimitOrganizationPropertyGet 等。