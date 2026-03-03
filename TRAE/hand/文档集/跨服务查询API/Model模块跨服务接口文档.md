# Model模块跨服务接口文档

## 概述

Model模块包含了业务模型相关的跨服务接口，用于查询和管理各种业务实体，如站点、区域、生产线、库位、工作单元和日历等。

## 接口列表

### 1. MtSiteRpcClient

**类路径**：`org.tarzan.boot.model.client.MtSiteRpcClient`

**主要方法**：
- `siteBasicPropertyGet` - 获取单个站点基本信息
- `siteBasicPropertyBatchGet` - 批量获取站点基本信息
- `codeLimitSiteBasicBatchQuery` - 根据编码批量查询站点基本信息
- `sitePropertyGet` - 获取单个站点详细信息
- `sitePropertyBatchGet` - 批量获取站点详细信息
- `siteLimitSiteQuery` - 查询站点
- `siteLimitSiteBatchQuery` - 批量查询站点

**用途**：用于查询站点相关信息，支持单个和批量查询，可根据编码查询站点基本信息。

### 3. MtAreaRpcClient

**类路径**：`org.tarzan.boot.model.client.MtAreaRpcClient`

**主要方法**：
- `areaBasicPropertyGet` - 获取单个区域基本信息
- `areaBasicPropertyBatchGet` - 批量获取区域基本信息
- `codeLimitAreaBasicBatchQuery` - 根据编码批量查询区域基本信息
- `areaPropertyGet` - 获取单个区域详细信息
- `areaPropertyBatchGet` - 批量获取区域详细信息
- `areaLimitAreaQuery` - 查询区域
- `areaLimitAreaBatchQuery` - 批量查询区域

**用途**：用于查询区域相关信息，支持单个和批量查询，可根据编码查询区域基本信息。

### 4. MtProdLineRpcClient

**类路径**：`org.tarzan.boot.model.client.MtProdLineRpcClient`

**主要方法**：
- `prodLineBasicPropertyGet` - 获取单个生产线基本信息
- `prodLineBasicPropertyBatchGet` - 批量获取生产线基本信息
- `codeLimitProdLineBasicBatchQuery` - 根据编码批量查询生产线基本信息
- `prodLinePropertyGet` - 获取单个生产线详细信息
- `prodLinePropertyBatchGet` - 批量获取生产线详细信息
- `prodLineLimitProdLineQuery` - 查询生产线
- `prodLineLimitProdLineBatchQuery` - 批量查询生产线

**用途**：用于查询生产线相关信息，支持单个和批量查询，可根据编码查询生产线基本信息。

### 5. MtLocatorRpcClient

**类路径**：`org.tarzan.boot.model.client.MtLocatorRpcClient`

**主要方法**：
- `locatorBasicPropertyGet` - 获取单个库位基本信息
- `locatorBasicPropertyBatchGet` - 批量获取库位基本信息
- `codeLimitLocatorBasicBatchQuery` - 根据编码批量查询库位基本信息
- `locatorPropertyGet` - 获取单个库位详细信息
- `locatorPropertyBatchGet` - 批量获取库位详细信息
- `locatorLimitLocatorQuery` - 查询库位
- `locatorLimitLocatorBatchQuery` - 批量查询库位

**用途**：用于查询库位相关信息，支持单个和批量查询，可根据编码查询库位基本信息。

### 6. MtWorkCellRpcClient

**类路径**：`org.tarzan.boot.model.client.MtWorkCellRpcClient`

**主要方法**：
- `workCellBasicPropertyGet` - 获取单个工作单元基本信息
- `workCellBasicPropertyBatchGet` - 批量获取工作单元基本信息
- `codeLimitWorkCellBasicBatchQuery` - 根据编码批量查询工作单元基本信息
- `workCellPropertyGet` - 获取单个工作单元详细信息
- `workCellPropertyBatchGet` - 批量获取工作单元详细信息
- `workCellLimitWorkCellQuery` - 查询工作单元
- `workCellLimitWorkCellBatchQuery` - 批量查询工作单元

**用途**：用于查询工作单元相关信息，支持单个和批量查询，可根据编码查询工作单元基本信息。

### 7. MtCalendarRpcClient

**类路径**：`org.tarzan.boot.model.client.MtCalendarRpcClient`

**主要方法**：
- `calendarBasicPropertyGet` - 获取单个日历基本信息
- `calendarBasicPropertyBatchGet` - 批量获取日历基本信息
- `codeLimitCalendarBasicBatchQuery` - 根据编码批量查询日历基本信息
- `calendarPropertyGet` - 获取单个日历详细信息
- `calendarPropertyBatchGet` - 批量获取日历详细信息
- `calendarLimitCalendarQuery` - 查询日历
- `calendarLimitCalendarBatchQuery` - 批量查询日历

**用途**：用于查询日历相关信息，支持单个和批量查询，可根据编码查询日历基本信息。

### 8. MtOrganizationRpcClient

**类路径**：`org.tarzan.boot.model.client.MtOrganizationRpcClient`

**主要方法**：
- `organizationBasicPropertyGet` - 获取单个组织基本信息
- `organizationBasicPropertyBatchGet` - 批量获取组织基本信息
- `codeLimitOrganizationBasicBatchQuery` - 根据编码批量查询组织基本信息
- `organizationPropertyGet` - 获取单个组织详细信息
- `organizationPropertyBatchGet` - 批量获取组织详细信息
- `organizationLimitOrganizationQuery` - 查询组织
- `organizationLimitOrganizationBatchQuery` - 批量查询组织

**用途**：用于查询组织相关信息，支持单个和批量查询，可根据编码查询组织基本信息。

## 使用示例

### 示例1：根据编码批量查询站点基本信息

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtSiteBaseVO;

List<String> siteCodes = Arrays.asList("SITE001", "SITE002");
List<MtSiteBaseVO> sites = mtSiteRpcClient.codeLimitSiteBasicBatchQuery(tenantId, siteCodes);
Map<String, Long> siteIdMap = sites.stream()
    .collect(Collectors.toMap(MtSiteBaseVO::getSiteCode, MtSiteBaseVO::getSiteId));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 物料、站点、区域等实体的基本信息和详细信息查询方法有所不同，根据业务需求选择合适的方法