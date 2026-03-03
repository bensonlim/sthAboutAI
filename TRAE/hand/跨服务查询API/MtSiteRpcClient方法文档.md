# MtSiteRpcClient 方法文档

## 概述

MtSiteRpcClient 是一个跨服务客户端，用于查询站点相关的信息，包括站点基本信息、站点调度信息、站点关系等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtSiteRpcClient** | `org.tarzan.boot.model.client.MtSiteRpcClient` |
| **MtModSiteBaseVO** | `org.tarzan.model.domain.vo.MtModSiteBaseVO` |
| **MtModSiteScheduleBaseVO** | `org.tarzan.model.domain.vo.MtModSiteScheduleBaseVO` |
| **MtModSiteVO8** | `org.tarzan.model.domain.vo.MtModSiteVO8` |
| **MtModSiteMappingVO1** | `org.tarzan.model.domain.vo.MtModSiteMappingVO1` |
| **MtModSiteMappingVO2** | `org.tarzan.model.domain.vo.MtModSiteMappingVO2` |

## 方法列表

### 1. siteBasicPropertyGet

**用途**：获取单个站点基本属性

**参数**：
- tenantId：租户ID
- siteId：站点ID

**返回值**：MtModSiteBaseVO - 站点基本信息

### 2. siteBasicPropertyBatchGet

**用途**：批量获取站点基本属性

**参数**：
- tenantId：租户ID
- siteIds：站点ID列表
- fields：可选，要查询的字段

**返回值**：List<MtModSiteBaseVO> - 站点基本信息列表或 Map<Long, String> - 站点ID到站点编码的映射

### 3. siteBasicByCodePropertyBatchGet

**用途**：根据编码批量获取站点基本属性

**参数**：
- tenantId：租户ID
- siteCodes：站点编码列表
- fields：可选，要查询的字段

**返回值**：Map<String, Long> - 站点编码到站点ID的映射

### 4. siteSchedulePropertyGet

**用途**：获取站点调度属性

**参数**：
- tenantId：租户ID
- siteId：站点ID

**返回值**：MtModSiteScheduleBaseVO - 站点调度信息

### 5. siteSchedulePropertyBatchGet

**用途**：批量获取站点调度属性

**参数**：
- tenantId：租户ID
- siteIds：站点ID列表
- fields：可选，要查询的字段

**返回值**：List<MtModSiteScheduleBaseVO> - 站点调度信息列表

### 6. siteManufacturingPropertyBatchGet

**用途**：批量获取站点制造属性

**参数**：
- tenantId：租户ID
- siteIds：站点ID列表
- fields：可选，要查询的字段

**返回值**：未知

### 7. codeListLimitSitePropertyQuery

**用途**：根据编码列表查询站点属性

**参数**：
- tenantId：租户ID
- siteCodes：站点编码列表

**返回值**：List<MtModSiteVO8> - 站点属性列表

### 8. propertyLimitSitePropertyQuery

**用途**：根据属性查询站点属性

**参数**：
- tenantId：租户ID
- condition：查询条件

**返回值**：List<MtModSiteVO8> - 站点属性列表

### 9. siteLimitAllRelatedSiteQuery

**用途**：查询站点所有相关站点

**参数**：
- tenantId：租户ID
- queryVO：查询对象

**返回值**：List<MtModSiteMappingVO2> - 站点映射关系列表

### 10. siteLimitPlantReleationQuery

**用途**：查询站点工厂关系

**参数**：
- tenantId：租户ID
- siteIds：站点ID列表

**返回值**：Map<Long, String> - 站点ID到工厂编码的映射

### 11. getRelationByPlantAndSiteType

**用途**：根据工厂和站点类型获取关系

**参数**：
- tenantId：租户ID
- queryRelVO：查询对象

**返回值**：未知

### 12. siteMappingQuery

**用途**：查询站点映射

**参数**：
- tenantId：租户ID
- siteId：站点ID

**返回值**：List<Long> - 映射站点ID列表

### 13. siteMappingBatchQuery

**用途**：批量查询站点映射

**参数**：
- tenantId：租户ID
- siteIds：站点ID列表

**返回值**：Map<Long, List<Long>> - 站点ID到映射站点ID列表的映射

## 使用示例

### 示例1：获取单个站点基本属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

MtModSiteBaseVO site = mtSiteRpcClient.siteBasicPropertyGet(tenantId, siteId);
String siteCode = site.getSiteCode();
```

### 示例2：批量获取站点基本属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteBaseVO;

List<Long> siteIds = Arrays.asList(1L, 2L, 3L);
List<MtModSiteBaseVO> sites = mtSiteRpcClient.siteBasicPropertyBatchGet(tenantId, siteIds);
Map<Long, String> siteCodeMap = sites.stream()
    .collect(Collectors.toMap(MtModSiteBaseVO::getSiteId, MtModSiteBaseVO::getSiteCode));
```

### 示例3：根据编码批量获取站点基本属性

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;

List<String> siteCodes = Arrays.asList("SITE001", "SITE002", "SITE003");
Map<String, Long> siteIdMap = mtSiteRpcClient.siteBasicByCodePropertyBatchGet(tenantId, siteCodes);
```

### 示例4：查询站点所有相关站点

```java
import org.tarzan.boot.model.client.MtSiteRpcClient;
import org.tarzan.model.domain.vo.MtModSiteMappingVO1;
import org.tarzan.model.domain.vo.MtModSiteMappingVO2;

MtModSiteMappingVO1 queryVO = new MtModSiteMappingVO1();
queryVO.setSiteId(siteId);
queryVO.setSiteType("MANUFACTURING");
List<MtModSiteMappingVO2> relatedSites = mtSiteRpcClient.siteLimitAllRelatedSiteQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
4. 不同方法返回的对象类型不同，使用时需要注意类型转换
5. 部分方法需要传入查询对象，需要根据具体需求构造查询条件