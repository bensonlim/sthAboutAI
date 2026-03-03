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

### 2. MtAreaRpcClient

**类路径**：`org.tarzan.boot.model.client.MtAreaRpcClient`

**主要方法**：
- `areaBasicPropertyGet` - 获取单个区域基本信息
- `areaBasicPropertyBatchGet` - 批量获取区域基本信息
- `codeLimitAreaPropertyBatchGet` - 根据编码批量获取区域基本信息
- `areaPurchasePropertyGet` - 获取单个区域采购信息
- `areaPurchasePropertyBatchGet` - 批量获取区域采购信息
- `areaSchedulePropertyGet` - 获取单个区域排程信息
- `areaSchedulePropertyBatchGet` - 批量获取区域排程信息
- `propertyLimitAreaQuery` - 根据属性查询区域
- `propertyLimitAreaPropertyQuery` - 根据属性查询区域属性
- `propertyLimitAreaSchedulePropertyQuery` - 根据属性查询区域排程属性
- `propertyListLimitAreaSchedulePropertyQuery` - 根据属性列表查询区域排程属性

**用途**：用于查询区域相关信息，支持单个和批量查询，可根据编码查询区域基本信息。

### 3. MtProdLineRpcClient

**类路径**：`org.tarzan.boot.model.client.MtProdLineRpcClient`

**主要方法**：
- `prodLineBasicPropertyGet` - 获取单个生产线基本信息
- `prodLineBasicPropertyBatchGet` - 批量获取生产线基本信息
- `codeListLimitProdLinePropertyQuery` - 根据编码列表查询生产线属性
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

### 4. MtLocatorRpcClient

**类路径**：`org.tarzan.boot.model.client.MtLocatorRpcClient`

**主要方法**：
- `locatorBasicPropertyGet` - 获取单个库位基本信息
- `locatorBasicPropertyBatchGet` - 批量获取库位基本信息
- `identificationLimitLocatorBatchGet` - 根据标识批量获取库位基本信息
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

### 5. MtWorkCellRpcClient

**类路径**：`org.tarzan.boot.model.client.MtWorkCellRpcClient`

**主要方法**：
- `workcellBasicPropertyGet` - 获取单个工作单元基本信息
- `workcellBasicPropertyBatchGet` - 批量获取工作单元基本信息
- `codeLimitWkcPropertyBatchGet` - 根据编码批量获取工作单元基本信息
- `workcellManufacturingPropertyGet` - 获取单个工作单元制造信息
- `workcellManufacturingPropertyBatchGet` - 批量获取工作单元制造信息
- `propertyLimitWorkcellQuery` - 根据属性查询工作单元
- `propertyLimitWorkcellPropertyQuery` - 根据属性查询工作单元属性
- `propertyLimitWorkcellManufacturingPropertyQuery` - 根据属性查询工作单元制造属性

**用途**：用于查询工作单元相关信息，支持单个和批量查询，可根据编码查询工作单元基本信息。

### 6. MtCalendarRpcClient

**类路径**：`org.tarzan.boot.model.client.MtCalendarRpcClient`

**主要方法**：
- `calendarGet` - 获取日历信息
- `calendarBatchGet` - 批量获取日历信息
- `calendarBasicBatchGetByCode` - 根据编码批量获取日历基本信息
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

### 7. MtOrganizationRpcClient

**类路径**：`org.tarzan.boot.model.client.MtOrganizationRpcClient`

**主要方法**：
- `organizationPropertyGet` - 获取单个组织基本信息
- `organizationPropertyBatchGet` - 批量获取组织基本信息
- `codeListLimitOrganizationPropertyGet` - 根据编码列表获取组织基本信息
- `parentOrganizationRelQuery` - 查询父组织关系
- `subOrganizationRelQuery` - 查询子组织关系
- `organizationLimitSchedulePropertyGet` - 根据组织获取排程属性
- `organizationLimitSchedulePropertyBatchGet` - 批量根据组织获取排程属性
- `organizationLimitSameLevelOrganizationQuery` - 查询组织的同级组织
- `parentOrgLimitSubOrgRelTreeQuery` - 根据父组织查询子组织关系树

**用途**：用于查询组织相关信息，支持单个和批量查询，可根据编码查询组织基本信息。

## 使用示例

### 示例1：获取单个站点基本信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

Long siteId = 1L;
MtModSiteBaseVO site = mtSiteRpcClient.siteBasicPropertyGet(tenantId, siteId);
System.out.println("站点编码：" + site.getSiteCode());
System.out.println("站点名称：" + site.getSiteName());
```

### 示例2：批量获取站点基本信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

List<Long> siteIds = Arrays.asList(1L, 2L, 3L);
List<MtModSiteBaseVO> sites = mtSiteRpcClient.siteBasicPropertyBatchGet(tenantId, siteIds);
Map<Long, String> siteMap = sites.stream()
    .collect(Collectors.toMap(MtModSiteBaseVO::getSiteId, MtModSiteBaseVO::getSiteCode));
```

### 示例3：根据编码批量获取站点基本信息（推荐）

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

List<String> siteCodes = Arrays.asList("SITE001", "SITE002");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.siteBasicByCodePropertyBatchGet(tenantId, siteCodes);
Map<String, Long> siteIdMap = sites.stream()
    .collect(Collectors.toMap(MtModSiteBaseVO::getSiteCode, MtModSiteBaseVO::getSiteId));
```

### 示例4：获取单个站点排程信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteScheduleVO;

Long siteId = 1L;
MtModSiteScheduleVO schedule = mtSiteRpcClient.siteSchedulePropertyGet(tenantId, siteId);
System.out.println("工作时间：" + schedule.getWorkTime());
```

### 示例5：批量获取站点排程信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteScheduleVO;

List<Long> siteIds = Arrays.asList(1L, 2L, 3L);
List<MtModSiteScheduleVO> schedules = mtSiteRpcClient.siteSchedulePropertyBatchGet(tenantId, siteIds);
Map<Long, MtModSiteScheduleVO> scheduleMap = schedules.stream()
    .collect(Collectors.toMap(MtModSiteScheduleVO::getSiteId, schedule -> schedule));
```

### 示例6：获取单个站点制造信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteManufacturingVO;

Long siteId = 1L;
MtModSiteManufacturingVO manufacturing = mtSiteRpcClient.siteManufacturingPropertyGet(tenantId, siteId);
System.out.println("制造能力：" + manufacturing.getManufacturingCapacity());
```

### 示例7：批量获取站点制造信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteManufacturingVO;

List<Long> siteIds = Arrays.asList(1L, 2L, 3L);
List<MtModSiteManufacturingVO> manufacturings = mtSiteRpcClient.siteManufacturingPropertyBatchGet(tenantId, siteIds);
Map<Long, MtModSiteManufacturingVO> manufacturingMap = manufacturings.stream()
    .collect(Collectors.toMap(MtModSiteManufacturingVO::getSiteId, manufacturing -> manufacturing));
```

### 示例8：根据属性查询站点

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;
import org.tarzan.model.domain.vo.MtModSiteQueryVO;

MtModSiteQueryVO queryVO = new MtModSiteQueryVO();
queryVO.setSiteType("PLANT");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.propertyLimitSiteQuery(tenantId, queryVO);
```

### 示例9：根据属性查询站点属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;
import org.tarzan.model.domain.vo.MtModSitePropertyQueryVO;

MtModSitePropertyQueryVO queryVO = new MtModSitePropertyQueryVO();
queryVO.setSiteType("PLANT");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.propertyLimitSitePropertyQuery(tenantId, queryVO);
```

### 示例10：根据条件查询站点属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;
import org.tarzan.model.domain.vo.MtModSiteConditionQueryVO;

MtModSiteConditionQueryVO queryVO = new MtModSiteConditionQueryVO();
queryVO.setSiteType("PLANT");
queryVO.setEnableFlag("Y");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.conditionLimitSitePropertyQuery(tenantId, queryVO);
```

### 示例11：根据编码列表查询站点属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

List<String> siteCodes = Arrays.asList("SITE001", "SITE002");
List<MtModSiteBaseVO> sites = mtSiteRpcClient.codeListLimitSitePropertyQuery(tenantId, siteCodes);
```

### 示例12：查询站点映射

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteMappingVO;
import org.tarzan.model.domain.vo.MtModSiteMappingQueryVO;

MtModSiteMappingQueryVO queryVO = new MtModSiteMappingQueryVO();
queryVO.setSourceSiteId(1L);
List<MtModSiteMappingVO> mappings = mtSiteRpcClient.siteMappingQuery(tenantId, queryVO);
```

### 示例13：查询站点所有相关站点

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

Long siteId = 1L;
List<MtModSiteBaseVO> relatedSites = mtSiteRpcClient.siteLimitAllRelatedSiteQuery(tenantId, siteId);
```

### 示例14：批量查询站点映射

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteMappingVO;
import org.tarzan.model.domain.vo.MtModSiteMappingQueryVO;

List<MtModSiteMappingQueryVO> queryVOs = new ArrayList<>();
MtModSiteMappingQueryVO queryVO1 = new MtModSiteMappingQueryVO();
queryVO1.setSourceSiteId(1L);
queryVOs.add(queryVO1);

MtModSiteMappingQueryVO queryVO2 = new MtModSiteMappingQueryVO();
queryVO2.setSourceSiteId(2L);
queryVOs.add(queryVO2);

List<List<MtModSiteMappingVO>> results = mtSiteRpcClient.siteMappingBatchQuery(tenantId, queryVOs);
```

### 示例15：根据工厂和站点类型获取关系

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteRelationVO;

Long plantId = 1L;
String siteType = "WAREHOUSE";
List<MtModSiteRelationVO> relations = mtSiteRpcClient.getRelationByPlantAndSiteType(tenantId, plantId, siteType);
```

### 示例16：根据站点查询工厂关系

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteRelationVO;

Long siteId = 1L;
List<MtModSiteRelationVO> relations = mtSiteRpcClient.siteLimitPlantReleationQuery(tenantId, siteId);
```

### 示例17：获取单个区域基本信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;

Long areaId = 1L;
MtModAreaBaseVO area = mtAreaRpcClient.areaBasicPropertyGet(tenantId, areaId);
System.out.println("区域编码：" + area.getAreaCode());
System.out.println("区域名称：" + area.getAreaName());
```

### 示例18：批量获取区域基本信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;

List<Long> areaIds = Arrays.asList(1L, 2L, 3L);
List<MtModAreaBaseVO> areas = mtAreaRpcClient.areaBasicPropertyBatchGet(tenantId, areaIds);
Map<Long, String> areaMap = areas.stream()
    .collect(Collectors.toMap(MtModAreaBaseVO::getAreaId, MtModAreaBaseVO::getAreaCode));
```

### 示例19：根据编码批量获取区域基本信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;

List<String> areaCodes = Arrays.asList("AREA001", "AREA002");
List<MtModAreaBaseVO> areas = mtAreaRpcClient.codeLimitAreaPropertyBatchGet(tenantId, areaCodes);
Map<String, Long> areaIdMap = areas.stream()
    .collect(Collectors.toMap(MtModAreaBaseVO::getAreaCode, MtModAreaBaseVO::getAreaId));
```

### 示例20：获取单个区域采购信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaPurchaseVO;

Long areaId = 1L;
MtModAreaPurchaseVO purchase = mtAreaRpcClient.areaPurchasePropertyGet(tenantId, areaId);
System.out.println("采购负责人：" + purchase.getPurchaseManager());
```

### 示例21：批量获取区域采购信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaPurchaseVO;

List<Long> areaIds = Arrays.asList(1L, 2L, 3L);
List<MtModAreaPurchaseVO> purchases = mtAreaRpcClient.areaPurchasePropertyBatchGet(tenantId, areaIds);
Map<Long, MtModAreaPurchaseVO> purchaseMap = purchases.stream()
    .collect(Collectors.toMap(MtModAreaPurchaseVO::getAreaId, purchase -> purchase));
```

### 示例22：获取单个区域排程信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaScheduleVO;

Long areaId = 1L;
MtModAreaScheduleVO schedule = mtAreaRpcClient.areaSchedulePropertyGet(tenantId, areaId);
System.out.println("排程负责人：" + schedule.getScheduleManager());
```

### 示例23：批量获取区域排程信息

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaScheduleVO;

List<Long> areaIds = Arrays.asList(1L, 2L, 3L);
List<MtModAreaScheduleVO> schedules = mtAreaRpcClient.areaSchedulePropertyBatchGet(tenantId, areaIds);
Map<Long, MtModAreaScheduleVO> scheduleMap = schedules.stream()
    .collect(Collectors.toMap(MtModAreaScheduleVO::getAreaId, schedule -> schedule));
```

### 示例24：根据属性查询区域

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;
import org.tarzan.model.domain.vo.MtModAreaQueryVO;

MtModAreaQueryVO queryVO = new MtModAreaQueryVO();
queryVO.setAreaType("PRODUCTION");
List<MtModAreaBaseVO> areas = mtAreaRpcClient.propertyLimitAreaQuery(tenantId, queryVO);
```

### 示例25：根据属性查询区域属性

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaBaseVO;
import org.tarzan.model.domain.vo.MtModAreaPropertyQueryVO;

MtModAreaPropertyQueryVO queryVO = new MtModAreaPropertyQueryVO();
queryVO.setAreaType("PRODUCTION");
List<MtModAreaBaseVO> areas = mtAreaRpcClient.propertyLimitAreaPropertyQuery(tenantId, queryVO);
```

### 示例26：根据属性查询区域排程属性

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaScheduleVO;
import org.tarzan.model.domain.vo.MtModAreaSchedulePropertyQueryVO;

MtModAreaSchedulePropertyQueryVO queryVO = new MtModAreaSchedulePropertyQueryVO();
queryVO.setAreaType("PRODUCTION");
List<MtModAreaScheduleVO> schedules = mtAreaRpcClient.propertyLimitAreaSchedulePropertyQuery(tenantId, queryVO);
```

### 示例27：根据属性列表查询区域排程属性

```java
import org.tarzan.boot.model.client.MtAreaRpcClient;
import org.tarzan.model.domain.vo.MtModAreaScheduleVO;
import org.tarzan.model.domain.vo.MtModAreaSchedulePropertyListQueryVO;

MtModAreaSchedulePropertyListQueryVO queryVO = new MtModAreaSchedulePropertyListQueryVO();
List<String> areaTypes = Arrays.asList("PRODUCTION", "WAREHOUSE");
queryVO.setAreaTypes(areaTypes);
List<MtModAreaScheduleVO> schedules = mtAreaRpcClient.propertyListLimitAreaSchedulePropertyQuery(tenantId, queryVO);
```

### 示例28：获取单个生产线基本信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;

Long prodLineId = 1L;
MtModProdLineBaseVO prodLine = mtProdLineRpcClient.prodLineBasicPropertyGet(tenantId, prodLineId);
System.out.println("生产线编码：" + prodLine.getProdLineCode());
System.out.println("生产线名称：" + prodLine.getProdLineName());
```

### 示例29：批量获取生产线基本信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;

List<Long> prodLineIds = Arrays.asList(1L, 2L, 3L);
List<MtModProdLineBaseVO> prodLines = mtProdLineRpcClient.prodLineBasicPropertyBatchGet(tenantId, prodLineIds);
Map<Long, String> prodLineMap = prodLines.stream()
    .collect(Collectors.toMap(MtModProdLineBaseVO::getProdLineId, MtModProdLineBaseVO::getProdLineCode));
```

### 示例30：根据编码列表查询生产线属性

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;

List<String> prodLineCodes = Arrays.asList("LINE001", "LINE002");
List<MtModProdLineBaseVO> prodLines = mtProdLineRpcClient.codeListLimitProdLinePropertyQuery(tenantId, prodLineCodes);
Map<String, Long> prodLineIdMap = prodLines.stream()
    .collect(Collectors.toMap(MtModProdLineBaseVO::getProdLineCode, MtModProdLineBaseVO::getProdLineId));
```

### 示例31：获取单个生产线排程信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineScheduleVO;

Long prodLineId = 1L;
MtModProdLineScheduleVO schedule = mtProdLineRpcClient.prodLineSchedulePropertyGet(tenantId, prodLineId);
System.out.println("排程效率：" + schedule.getScheduleEfficiency());
```

### 示例32：批量获取生产线排程信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineScheduleVO;

List<Long> prodLineIds = Arrays.asList(1L, 2L, 3L);
List<MtModProdLineScheduleVO> schedules = mtProdLineRpcClient.prodLineSchedulePropertyBatchGet(tenantId, prodLineIds);
Map<Long, MtModProdLineScheduleVO> scheduleMap = schedules.stream()
    .collect(Collectors.toMap(MtModProdLineScheduleVO::getProdLineId, schedule -> schedule));
```

### 示例33：获取单个生产线制造信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingVO;

Long prodLineId = 1L;
MtModProdLineManufacturingVO manufacturing = mtProdLineRpcClient.prodLineManufacturingPropertyGet(tenantId, prodLineId);
System.out.println("制造能力：" + manufacturing.getManufacturingCapacity());
```

### 示例34：批量获取生产线制造信息

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingVO;

List<Long> prodLineIds = Arrays.asList(1L, 2L, 3L);
List<MtModProdLineManufacturingVO> manufacturings = mtProdLineRpcClient.prodLineManufacturingPropertyBatchGet(tenantId, prodLineIds);
Map<Long, MtModProdLineManufacturingVO> manufacturingMap = manufacturings.stream()
    .collect(Collectors.toMap(MtModProdLineManufacturingVO::getProdLineId, manufacturing -> manufacturing));
```

### 示例35：根据属性查询生产线

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;
import org.tarzan.model.domain.vo.MtModProdLineQueryVO;

MtModProdLineQueryVO queryVO = new MtModProdLineQueryVO();
queryVO.setProdLineType("ASSEMBLY");
List<MtModProdLineBaseVO> prodLines = mtProdLineRpcClient.propertyLimitProdLineQuery(tenantId, queryVO);
```

### 示例36：根据属性查询生产线属性

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;
import org.tarzan.model.domain.vo.MtModProdLinePropertyQueryVO;

MtModProdLinePropertyQueryVO queryVO = new MtModProdLinePropertyQueryVO();
queryVO.setProdLineType("ASSEMBLY");
List<MtModProdLineBaseVO> prodLines = mtProdLineRpcClient.propertyLimitProdLinePropertyQuery(tenantId, queryVO);
```

### 示例37：根据属性查询生产线制造属性

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingVO;
import org.tarzan.model.domain.vo.MtModProdLineManufacturingPropertyQueryVO;

MtModProdLineManufacturingPropertyQueryVO queryVO = new MtModProdLineManufacturingPropertyQueryVO();
queryVO.setProdLineType("ASSEMBLY");
List<MtModProdLineManufacturingVO> manufacturings = mtProdLineRpcClient.propertyLimitProdLineManufacturingPropertyQuery(tenantId, queryVO);
```

### 示例38：根据生产线查询调度工序

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineDispatchOperationVO;

Long prodLineId = 1L;
List<MtModProdLineDispatchOperationVO> operations = mtProdLineRpcClient.prodLineLimitDispatchOperationQuery(tenantId, prodLineId);
```

### 示例39：根据工序查询生产线

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineBaseVO;

Long operationId = 1L;
List<MtModProdLineBaseVO> prodLines = mtProdLineRpcClient.operationLimitProdLineQuery(tenantId, operationId);
```

### 示例40：根据属性列表查询生产线调度工序

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineDispatchOperationVO;
import org.tarzan.model.domain.vo.MtModProdLineDispatchOperationPropertyListQueryVO;

MtModProdLineDispatchOperationPropertyListQueryVO queryVO = new MtModProdLineDispatchOperationPropertyListQueryVO();
queryVO.setProdLineId(1L);
List<MtModProdLineDispatchOperationVO> operations = mtProdLineRpcClient.propertyListLimitProdLineDispatchOperationQuery(tenantId, queryVO);
```

### 示例41：验证生产线调度工序

```java
import org.tarzan.boot.model.client.MtProdLineRpcClient;
import org.tarzan.model.domain.vo.MtModProdLineDispatchOperationValidateVO;

MtModProdLineDispatchOperationValidateVO validateVO = new MtModProdLineDispatchOperationValidateVO();
validateVO.setProdLineId(1L);
validateVO.setOperationId(2L);
boolean isValid = mtProdLineRpcClient.prodLineDispatchOperationValidate(tenantId, validateVO);
System.out.println("调度工序是否有效：" + isValid);
```

### 示例42：获取单个库位基本信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long locatorId = 1L;
MtModLocatorBaseVO locator = mtLocatorRpcClient.locatorBasicPropertyGet(tenantId, locatorId);
System.out.println("库位编码：" + locator.getLocatorCode());
System.out.println("库位名称：" + locator.getLocatorName());
```

### 示例43：批量获取库位基本信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<Long> locatorIds = Arrays.asList(1L, 2L, 3L);
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.locatorBasicPropertyBatchGet(tenantId, locatorIds);
Map<Long, String> locatorMap = locators.stream()
    .collect(Collectors.toMap(MtModLocatorBaseVO::getLocatorId, MtModLocatorBaseVO::getLocatorCode));
```

### 示例44：根据标识批量获取库位基本信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<String> identifications = Arrays.asList("LOC001", "LOC002");
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.identificationLimitLocatorBatchGet(tenantId, identifications);
Map<String, Long> locatorIdMap = locators.stream()
    .collect(Collectors.toMap(MtModLocatorBaseVO::getLocatorCode, MtModLocatorBaseVO::getLocatorId));
```

### 示例45：查询子库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long locatorId = 1L;
List<MtModLocatorBaseVO> subLocators = mtLocatorRpcClient.subLocatorQuery(tenantId, locatorId);
```

### 示例46：查询父库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long locatorId = 1L;
MtModLocatorBaseVO parentLocator = mtLocatorRpcClient.parentLocatorQuery(tenantId, locatorId);
System.out.println("父库位编码：" + parentLocator.getLocatorCode());
```

### 示例47：根据库位列表查询子库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<Long> locatorIds = Arrays.asList(1L, 2L);
List<List<MtModLocatorBaseVO>> subLocatorsList = mtLocatorRpcClient.locatorListLimitSubLocatorQuery(tenantId, locatorIds);
```

### 示例48：根据库位列表查询父库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<Long> locatorIds = Arrays.asList(1L, 2L);
List<MtModLocatorBaseVO> parentLocators = mtLocatorRpcClient.locatorListLimitParentLocatorQuery(tenantId, locatorIds);
```

### 示例49：查询库位站点关系

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorSiteRelVO;
import org.tarzan.model.domain.vo.MtModLocatorSiteRelQueryVO;

MtModLocatorSiteRelQueryVO queryVO = new MtModLocatorSiteRelQueryVO();
queryVO.setLocatorId(1L);
List<MtModLocatorSiteRelVO> relations = mtLocatorRpcClient.locatorSiteRelQuery(tenantId, queryVO);
```

### 示例50：根据属性查询库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;
import org.tarzan.model.domain.vo.MtModLocatorQueryVO;

MtModLocatorQueryVO queryVO = new MtModLocatorQueryVO();
queryVO.setLocatorType("STORAGE");
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.propertyLimitLocatorQuery(tenantId, queryVO);
```

### 示例51：根据属性查询库位属性

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;
import org.tarzan.model.domain.vo.MtModLocatorPropertyQueryVO;

MtModLocatorPropertyQueryVO queryVO = new MtModLocatorPropertyQueryVO();
queryVO.setLocatorType("STORAGE");
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.propertyLimitLocatorPropertyQuery(tenantId, queryVO);
```

### 示例52：根据编码列表查询库位属性

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

List<String> locatorCodes = Arrays.asList("LOC001", "LOC002");
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.codeListLimitLocatorPropertyQuery(tenantId, locatorCodes);
```

### 示例53：根据库位查询库存分类库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorInventoryCategoryVO;

Long locatorId = 1L;
List<MtModLocatorInventoryCategoryVO> inventoryCategories = mtLocatorRpcClient.locatorLimitInventoryCategoryLocatorGet(tenantId, locatorId);
```

### 示例54：根据库位列表查询库存分类库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorInventoryCategoryVO;

List<Long> locatorIds = Arrays.asList(1L, 2L);
List<MtModLocatorInventoryCategoryVO> inventoryCategories = mtLocatorRpcClient.locatorListLimitInvCategoryLocatorGet(tenantId, locatorIds);
```

### 示例55：查询库位子库位树

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorTreeVO;

Long locatorId = 1L;
MtModLocatorTreeVO locatorTree = mtLocatorRpcClient.locatorLimitSubLocatorTree(tenantId, locatorId);
```

### 示例56：批量查询库位子库位树

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorTreeVO;

List<Long> locatorIds = Arrays.asList(1L, 2L);
List<MtModLocatorTreeVO> locatorTrees = mtLocatorRpcClient.locatorLimitSubLocatorTreeBatchQuery(tenantId, locatorIds);
```

### 示例57：根据属性查询库位子库存关系

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorSubinvRelVO;
import org.tarzan.model.domain.vo.MtModLocatorSubinvRelQueryVO;

MtModLocatorSubinvRelQueryVO queryVO = new MtModLocatorSubinvRelQueryVO();
queryVO.setLocatorId(1L);
List<MtModLocatorSubinvRelVO> relations = mtLocatorRpcClient.properyLimitLocatorSubinvReleationQuery(tenantId, queryVO);
```

### 示例58：查询父库位和深度

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorParentDepthVO;

Long locatorId = 1L;
MtModLocatorParentDepthVO parentDepth = mtLocatorRpcClient.parentLocatorAndDepthQuery(tenantId, locatorId);
System.out.println("父库位ID：" + parentDepth.getParentLocatorId());
System.out.println("深度：" + parentDepth.getDepth());
```

### 示例59：查询库位权限

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorPermissionVO;
import org.tarzan.model.domain.vo.MtModLocatorPermissionQueryVO;

MtModLocatorPermissionQueryVO queryVO = new MtModLocatorPermissionQueryVO();
queryVO.setUserId(1L);
List<MtModLocatorPermissionVO> permissions = mtLocatorRpcClient.locatorPermissionQuery(tenantId, queryVO);
```

### 示例60：查询用户可操作的区域库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long userId = 1L;
Long areaId = 2L;
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.userOperableAreaLocatorQuery(tenantId, userId, areaId);
```

### 示例61：根据站点查询库位信息

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long siteId = 1L;
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.siteLimitLocatorInfoQuery(tenantId, siteId);
```

### 示例62：根据生产线查询库存库位

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long prodLineId = 1L;
List<MtModLocatorBaseVO> locators = mtLocatorRpcClient.prodLineLimitInvLocatorQuery(tenantId, prodLineId);
```

### 示例63：根据站点查询目标位置

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorBaseVO;

Long siteId = 1L;
List<MtModLocatorBaseVO> targetLocations = mtLocatorRpcClient.siteLimitTargetLocationQuery(tenantId, siteId);
```

### 示例64：验证库位记录在手量

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorOnhandVerifyVO;

MtModLocatorOnhandVerifyVO verifyVO = new MtModLocatorOnhandVerifyVO();
verifyVO.setLocatorId(1L);
verifyVO.setMaterialId(2L);
boolean isValid = mtLocatorRpcClient.locatorRecordOnhandVerify(tenantId, verifyVO);
System.out.println("库位记录在手量是否有效：" + isValid);
```

### 示例65：验证库位执行

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorExecutionValidateVO;

MtModLocatorExecutionValidateVO validateVO = new MtModLocatorExecutionValidateVO();
validateVO.setLocatorId(1L);
boolean isValid = mtLocatorRpcClient.locatorExecutionValidate(tenantId, validateVO);
System.out.println("库位执行是否有效：" + isValid);
```

### 示例66：批量验证库位执行

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModLocatorExecutionValidateVO;

List<MtModLocatorExecutionValidateVO> validateVOs = new ArrayList<>();
MtModLocatorExecutionValidateVO validateVO1 = new MtModLocatorExecutionValidateVO();
validateVO1.setLocatorId(1L);
validateVOs.add(validateVO1);

MtModLocatorExecutionValidateVO validateVO2 = new MtModLocatorExecutionValidateVO();
validateVO2.setLocatorId(2L);
validateVOs.add(validateVO2);

List<Boolean> results = mtLocatorRpcClient.locatorExecutionBatchValidate(tenantId, validateVOs);
```

### 示例67：验证用户区域库位执行

```java
import org.tarzan.boot.model.client.MtLocatorRpcClient;
import org.tarzan.model.domain.vo.MtModUserAreaLocatorExecutionValidateVO;

MtModUserAreaLocatorExecutionValidateVO validateVO = new MtModUserAreaLocatorExecutionValidateVO();
validateVO.setUserId(1L);
validateVO.setAreaId(2L);
validateVO.setLocatorId(3L);
boolean isValid = mtLocatorRpcClient.userAreaLocatorExecutionValidate(tenantId, validateVO);
System.out.println("用户区域库位执行是否有效：" + isValid);
```

### 示例68：获取单个工作单元基本信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;

Long workcellId = 1L;
MtModWorkcellBaseVO workcell = mtWorkCellRpcClient.workcellBasicPropertyGet(tenantId, workcellId);
System.out.println("工作单元编码：" + workcell.getWorkcellCode());
System.out.println("工作单元名称：" + workcell.getWorkcellName());
```

### 示例69：批量获取工作单元基本信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;

List<Long> workcellIds = Arrays.asList(1L, 2L, 3L);
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.workcellBasicPropertyBatchGet(tenantId, workcellIds);
Map<Long, String> workcellMap = workcells.stream()
    .collect(Collectors.toMap(MtModWorkcellBaseVO::getWorkcellId, MtModWorkcellBaseVO::getWorkcellCode));
```

### 示例70：根据编码批量获取工作单元基本信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;

List<String> workcellCodes = Arrays.asList("WC001", "WC002");
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.codeLimitWkcPropertyBatchGet(tenantId, workcellCodes);
Map<String, Long> workcellIdMap = workcells.stream()
    .collect(Collectors.toMap(MtModWorkcellBaseVO::getWorkcellCode, MtModWorkcellBaseVO::getWorkcellId));
```

### 示例71：获取单个工作单元制造信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO;

Long workcellId = 1L;
MtModWorkcellManufacturingVO manufacturing = mtWorkCellRpcClient.workcellManufacturingPropertyGet(tenantId, workcellId);
System.out.println("制造能力：" + manufacturing.getManufacturingCapacity());
```

### 示例72：批量获取工作单元制造信息

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO;

List<Long> workcellIds = Arrays.asList(1L, 2L, 3L);
List<MtModWorkcellManufacturingVO> manufacturings = mtWorkCellRpcClient.workcellManufacturingPropertyBatchGet(tenantId, workcellIds);
Map<Long, MtModWorkcellManufacturingVO> manufacturingMap = manufacturings.stream()
    .collect(Collectors.toMap(MtModWorkcellManufacturingVO::getWorkcellId, manufacturing -> manufacturing));
```

### 示例73：根据属性查询工作单元

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;
import org.tarzan.model.domain.vo.MtModWorkcellQueryVO;

MtModWorkcellQueryVO queryVO = new MtModWorkcellQueryVO();
queryVO.setWorkcellType("ASSEMBLY");
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.propertyLimitWorkcellQuery(tenantId, queryVO);
```

### 示例74：根据属性查询工作单元属性

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellBaseVO;
import org.tarzan.model.domain.vo.MtModWorkcellPropertyQueryVO;

MtModWorkcellPropertyQueryVO queryVO = new MtModWorkcellPropertyQueryVO();
queryVO.setWorkcellType("ASSEMBLY");
List<MtModWorkcellBaseVO> workcells = mtWorkCellRpcClient.propertyLimitWorkcellPropertyQuery(tenantId, queryVO);
```

### 示例75：根据属性查询工作单元制造属性

```java
import org.tarzan.boot.model.client.MtWorkCellRpcClient;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingVO;
import org.tarzan.model.domain.vo.MtModWorkcellManufacturingPropertyQueryVO;

MtModWorkcellManufacturingPropertyQueryVO queryVO = new MtModWorkcellManufacturingPropertyQueryVO();
queryVO.setWorkcellType("ASSEMBLY");
List<MtModWorkcellManufacturingVO> manufacturings = mtWorkCellRpcClient.propertyLimitWorkcellManufacturingPropertyQuery(tenantId, queryVO);
```

### 示例76：获取日历信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarVO;

Long calendarId = 1L;
MtModCalendarVO calendar = mtCalendarRpcClient.calendarGet(tenantId, calendarId);
System.out.println("日历编码：" + calendar.getCalendarCode());
System.out.println("日历名称：" + calendar.getCalendarName());
```

### 示例77：批量获取日历信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarVO;

List<Long> calendarIds = Arrays.asList(1L, 2L, 3L);
List<MtModCalendarVO> calendars = mtCalendarRpcClient.calendarBatchGet(tenantId, calendarIds);
Map<Long, String> calendarMap = calendars.stream()
    .collect(Collectors.toMap(MtModCalendarVO::getCalendarId, MtModCalendarVO::getCalendarCode));
```

### 示例78：根据编码批量获取日历基本信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarBaseVO;

List<String> calendarCodes = Arrays.asList("CAL001", "CAL002");
List<MtModCalendarBaseVO> calendars = mtCalendarRpcClient.calendarBasicBatchGetByCode(tenantId, calendarCodes);
Map<String, Long> calendarIdMap = calendars.stream()
    .collect(Collectors.toMap(MtModCalendarBaseVO::getCalendarCode, MtModCalendarBaseVO::getCalendarId));
```

### 示例79：获取日历班次信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarShiftVO;

Long calendarShiftId = 1L;
MtModCalendarShiftVO calendarShift = mtCalendarRpcClient.calendarShiftGet(tenantId, calendarShiftId);
System.out.println("班次编码：" + calendarShift.getShiftCode());
System.out.println("班次名称：" + calendarShift.getShiftName());
```

### 示例80：批量获取日历班次信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarShiftVO;

List<Long> calendarShiftIds = Arrays.asList(1L, 2L, 3L);
List<MtModCalendarShiftVO> calendarShifts = mtCalendarRpcClient.calendarShiftBatchGet(tenantId, calendarShiftIds);
Map<Long, String> calendarShiftMap = calendarShifts.stream()
    .collect(Collectors.toMap(MtModCalendarShiftVO::getCalendarShiftId, MtModCalendarShiftVO::getShiftCode));
```

### 示例81：根据组织和时间获取日历班次

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarShiftVO;
import java.util.Date;

Long organizationId = 1L;
Date date = new Date();
MtModCalendarShiftVO calendarShift = mtCalendarRpcClient.orgAndTimeLimitCalendarShiftGet(tenantId, organizationId, date);
```

### 示例82：批量根据组织和时间获取日历班次

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtModCalendarShiftVO;
import org.tarzan.model.domain.vo.MtModCalendarShiftTimeQueryVO;
import java.util.Date;

List<MtModCalendarShiftTimeQueryVO> queryVOs = new ArrayList<>();
MtModCalendarShiftTimeQueryVO queryVO1 = new MtModCalendarShiftTimeQueryVO();
queryVO1.setOrganizationId(1L);
queryVO1.setDate(new Date());
queryVOs.add(queryVO1);

MtModCalendarShiftTimeQueryVO queryVO2 = new MtModCalendarShiftTimeQueryVO();
queryVO2.setOrganizationId(2L);
queryVO2.setDate(new Date());
queryVOs.add(queryVO2);

List<MtModCalendarShiftVO> calendarShifts = mtCalendarRpcClient.orgAndTimeLimitCalendarShiftBatchGet(tenantId, queryVOs);
```

### 示例83：获取单个组织基本信息

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationBaseVO;

Long organizationId = 1L;
MtModOrganizationBaseVO organization = mtOrganizationRpcClient.organizationPropertyGet(tenantId, organizationId);
System.out.println("组织编码：" + organization.getOrganizationCode());
System.out.println("组织名称：" + organization.getOrganizationName());
```

### 示例84：批量获取组织基本信息

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationBaseVO;

List<Long> organizationIds = Arrays.asList(1L, 2L, 3L);
List<MtModOrganizationBaseVO> organizations = mtOrganizationRpcClient.organizationPropertyBatchGet(tenantId, organizationIds);
Map<Long, String> organizationMap = organizations.stream()
    .collect(Collectors.toMap(MtModOrganizationBaseVO::getOrganizationId, MtModOrganizationBaseVO::getOrganizationCode));
```

### 示例85：根据编码列表获取组织基本信息

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationBaseVO;

List<String> organizationCodes = Arrays.asList("ORG001", "ORG002");
List<MtModOrganizationBaseVO> organizations = mtOrganizationRpcClient.codeListLimitOrganizationPropertyGet(tenantId, organizationCodes);
Map<String, Long> organizationIdMap = organizations.stream()
    .collect(Collectors.toMap(MtModOrganizationBaseVO::getOrganizationCode, MtModOrganizationBaseVO::getOrganizationId));
```

### 示例86：查询父组织关系

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationRelationVO;

Long organizationId = 1L;
List<MtModOrganizationRelationVO> parentRelations = mtOrganizationRpcClient.parentOrganizationRelQuery(tenantId, organizationId);
```

### 示例87：查询子组织关系

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationRelationVO;

Long organizationId = 1L;
List<MtModOrganizationRelationVO> subRelations = mtOrganizationRpcClient.subOrganizationRelQuery(tenantId, organizationId);
```

### 示例88：根据组织获取排程属性

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationScheduleVO;

Long organizationId = 1L;
MtModOrganizationScheduleVO schedule = mtOrganizationRpcClient.organizationLimitSchedulePropertyGet(tenantId, organizationId);
System.out.println("排程负责人：" + schedule.getScheduleManager());
```

### 示例89：批量根据组织获取排程属性

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationScheduleVO;

List<Long> organizationIds = Arrays.asList(1L, 2L, 3L);
List<MtModOrganizationScheduleVO> schedules = mtOrganizationRpcClient.organizationLimitSchedulePropertyBatchGet(tenantId, organizationIds);
Map<Long, MtModOrganizationScheduleVO> scheduleMap = schedules.stream()
    .collect(Collectors.toMap(MtModOrganizationScheduleVO::getOrganizationId, schedule -> schedule));
```

### 示例90：查询组织的同级组织

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationBaseVO;

Long organizationId = 1L;
List<MtModOrganizationBaseVO> sameLevelOrganizations = mtOrganizationRpcClient.organizationLimitSameLevelOrganizationQuery(tenantId, organizationId);
```

### 示例91：根据父组织查询子组织关系树

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationTreeVO;

Long parentOrganizationId = 1L;
MtModOrganizationTreeVO organizationTree = mtOrganizationRpcClient.parentOrgLimitSubOrgRelTreeQuery(tenantId, parentOrganizationId);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 物料、站点、区域等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法

