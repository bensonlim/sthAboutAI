# MtMaterialRpcClient 方法文档

## 概述

MtMaterialRpcClient 是一个跨服务客户端，用于查询物料相关的信息，包括物料基本信息、物料站点信息、物料属性等。

## 类路径

| 类名                       | 包路径                                                 |
|--------------------------|-----------------------------------------------------|
| **MtMaterialRpcClient**  | `org.tarzan.boot.method.client.MtMaterialRpcClient` |
| **MtMaterialBaseVO**     | `org.tarzan.method.domain.vo.MtMaterialBaseVO`       |
| **MtMaterialVO**         | `org.tarzan.method.domain.vo.MtMaterialVO`           |
| **MtMaterialSiteVO4**    | `org.tarzan.method.domain.vo.MtMaterialSiteVO4`      |
| **MtMaterialSiteBaseVO** | `org.tarzan.method.domain.vo.MtMaterialSiteBaseVO`       |

## 方法列表

### 1. materialBasicInfoBatchGet

**用途**：批量获取物料基本信息

**参数**：
- tenantId：租户ID
- materialIds：物料ID列表
- fields：可选，要查询的字段

**返回值**：List<MtMaterialBaseVO> - 物料基本信息列表

### 2. codeLimitMaterialBasicBatchQuery

**用途**：根据编码批量查询物料基本信息

**参数**：
- tenantId：租户ID
- materialCodes：物料编码列表
- fields：可选，要查询的字段

**返回值**：List<MtMaterialBaseVO> - 物料基本信息列表

### 3. materialSiteListLimitMaterialSiteQuery

**用途**：查询物料站点信息

**参数**：
- tenantId：租户ID
- materialIds：物料ID列表
- siteIds：站点ID列表

**返回值**：List<MtMaterialSiteBaseVO> - 物料站点信息列表

### 4. materialSiteLimitRelationBatchGet

**用途**：批量获取物料站点关系

**参数**：
- tenantId：租户ID
- 查询对象列表

**返回值**：List<MtMaterialSiteVO4> - 物料站点关系列表

### 5. materialPropertyBatchGet

**用途**：批量获取物料属性

**参数**：
- tenantId：租户ID
- materialIds：物料ID列表
- fields：可选，要查询的字段

**返回值**：List<MtMaterialVO> 或 Map<Long, String> - 物料属性列表或映射

### 6. queryMaterialSiteByMaterialId

**用途**：根据物料ID查询物料站点信息

**参数**：
- tenantId：租户ID
- materialIds：物料ID列表

**返回值**：List<MtMaterialSiteBaseVO> - 物料站点信息列表

### 7. setLimitMaterialAssignCategoryBatchGet

**用途**：批量获取物料分配类别

**参数**：
- tenantId：租户ID
- 查询对象

**返回值**：未知

## 使用示例

### 示例1：批量获取物料基本信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.materialBasicInfoBatchGet(tenantId, materialIds);
Map<Long, String> materialCodeMap = materials.stream()
    .collect(Collectors.toMap(MtMaterialBaseVO::getMaterialId, MtMaterialBaseVO::getMaterialCode));
```

### 示例2：根据编码批量查询物料基本信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBaseVO;

List<String> materialCodes = Arrays.asList("MAT001", "MAT002", "MAT003");
List<MtMaterialBaseVO> materials = mtMaterialRpcClient.codeLimitMaterialBasicBatchQuery(tenantId, materialCodes);
Map<String, Long> materialIdMap = materials.stream()
    .collect(Collectors.toMap(MtMaterialBaseVO::getMaterialCode, MtMaterialBaseVO::getMaterialId));
```

### 示例3：查询物料站点信息

```java
import org.tarzan.boot.method.client.MtMaterialRpcClient;
import org.tarzan.method.domain.vo.MtMaterialSiteBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<Long> siteIds = Arrays.asList(101L, 102L);
List<MtMaterialSiteBaseVO> materialSites = mtMaterialRpcClient.materialSiteListLimitMaterialSiteQuery(tenantId, materialIds, siteIds);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
4. 不同方法返回的对象类型不同，使用时需要注意类型转换