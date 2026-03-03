# MtBomRpcClient 方法文档

## 概述

MtBomRpcClient 是一个跨服务客户端，用于查询BOM（物料清单）相关的信息，包括BOM基本信息、BOM组件、BOM替代组、BOM站点分配等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtBomRpcClient** | `org.tarzan.boot.method.client.MtBomRpcClient` |
| **MtBomBaseVO** | `org.tarzan.method.domain.vo.MtBomBaseVO` |
| **MtBomVO** | `org.tarzan.method.domain.vo.MtBomVO` |
| **MtBomVO1** | `org.tarzan.method.domain.vo.MtBomVO1` |
| **MtBomComponentVO** | `org.tarzan.method.domain.vo.MtBomComponentVO` |
| **MtBomComponentVO1** | `org.tarzan.method.domain.vo.MtBomComponentVO1` |
| **MtBomComponentVO5** | `org.tarzan.method.domain.vo.MtBomComponentVO5` |
| **MtBomComponentVO6** | `org.tarzan.method.domain.vo.MtBomComponentVO6` |
| **MtBomComponentVO9** | `org.tarzan.method.domain.vo.MtBomComponentVO9` |
| **MtBomSiteAssignVO** | `org.tarzan.method.domain.vo.MtBomSiteAssignVO` |
| **MtBomSiteAssignVO1** | `org.tarzan.method.domain.vo.MtBomSiteAssignVO1` |
| **MtBomSubstituteGroupVO** | `org.tarzan.method.domain.vo.MtBomSubstituteGroupVO` |
| **MtBomSubstituteVO** | `org.tarzan.method.domain.vo.MtBomSubstituteVO` |
| **MtBomSubstituteVO1** | `org.tarzan.method.domain.vo.MtBomSubstituteVO1` |
| **MtBomReferencePointVO** | `org.tarzan.method.domain.vo.MtBomReferencePointVO` |
| **MtMaterialBomRelVO** | `org.tarzan.method.domain.vo.MtMaterialBomRelVO` |

## 方法列表

### 1. bomBasicPropertyGet

**用途**：获取单个BOM基本信息

**参数**：
- tenantId：租户ID
- bomId：BOM ID

**返回值**：MtBomBaseVO - BOM基本信息

### 2. bomBasicPropertyBatchGet

**用途**：批量获取BOM基本信息

**参数**：
- tenantId：租户ID
- bomIds：BOM ID列表

**返回值**：List<MtBomBaseVO> - BOM基本信息列表

### 3. codeLimitBomBasicBatchQuery

**用途**：根据编码批量查询BOM基本信息

**参数**：
- tenantId：租户ID
- bomCodes：BOM编码列表

**返回值**：List<MtBomBaseVO> - BOM基本信息列表

### 4. bomComponentPropertyGet

**用途**：获取单个BOM组件信息

**参数**：
- tenantId：租户ID
- bomComponentId：BOM组件ID

**返回值**：MtBomComponentVO - BOM组件信息

### 5. bomComponentPropertyBatchGet

**用途**：批量获取BOM组件信息

**参数**：
- tenantId：租户ID
- bomComponentIds：BOM组件ID列表

**返回值**：List<MtBomComponentVO> - BOM组件信息列表

### 6. bomLimitBomComponentQuery

**用途**：查询BOM组件

**参数**：
- tenantId：租户ID
- queryVO：BOM组件查询对象

**返回值**：List<MtBomComponentVO1> - BOM组件列表

### 7. bomLimitBomComponentBatchQuery

**用途**：批量查询BOM组件

**参数**：
- tenantId：租户ID
- queryVOs：BOM组件查询对象列表

**返回值**：List<MtBomComponentVO5> - BOM组件列表

### 8. bomSiteAssignPropertyGet

**用途**：获取单个BOM站点分配信息

**参数**：
- tenantId：租户ID
- bomSiteAssignId：BOM站点分配ID

**返回值**：MtBomSiteAssignVO - BOM站点分配信息

### 9. bomSiteAssignPropertyBatchGet

**用途**：批量获取BOM站点分配信息

**参数**：
- tenantId：租户ID
- bomSiteAssignIds：BOM站点分配ID列表

**返回值**：List<MtBomSiteAssignVO> - BOM站点分配信息列表

### 10. bomLimitBomSiteAssignQuery

**用途**：查询BOM站点分配

**参数**：
- tenantId：租户ID
- queryVO：BOM站点分配查询对象

**返回值**：List<MtBomSiteAssignVO1> - BOM站点分配列表

### 11. bomSubstituteGroupPropertyGet

**用途**：获取单个BOM替代组信息

**参数**：
- tenantId：租户ID
- substituteGroupId：替代组ID

**返回值**：MtBomSubstituteGroupVO - BOM替代组信息

### 12. bomSubstituteGroupPropertyBatchGet

**用途**：批量获取BOM替代组信息

**参数**：
- tenantId：租户ID
- substituteGroupIds：替代组ID列表

**返回值**：List<MtBomSubstituteGroupVO> - BOM替代组信息列表

### 13. bomLimitBomSubstituteQuery

**用途**：查询BOM替代

**参数**：
- tenantId：租户ID
- queryVO：BOM替代查询对象

**返回值**：List<MtBomSubstituteVO> - BOM替代列表

### 14. bomLimitBomSubstituteBatchQuery

**用途**：批量查询BOM替代

**参数**：
- tenantId：租户ID
- queryVOs：BOM替代查询对象列表

**返回值**：List<MtBomSubstituteVO1> - BOM替代列表

### 15. bomReferencePointPropertyGet

**用途**：获取单个BOM参考点信息

**参数**：
- tenantId：租户ID
- referencePointId：参考点ID

**返回值**：MtBomReferencePointVO - BOM参考点信息

### 16. bomLimitBomReferencePointQuery

**用途**：查询BOM参考点

**参数**：
- tenantId：租户ID
- queryVO：BOM参考点查询对象

**返回值**：List<MtBomReferencePointVO> - BOM参考点列表

### 17. materialLimitBomRelQuery

**用途**：查询物料BOM关系

**参数**：
- tenantId：租户ID
- queryVO：物料BOM关系查询对象

**返回值**：List<MtMaterialBomRelVO> - 物料BOM关系列表

### 18. bomLimitBomQuery

**用途**：查询BOM

**参数**：
- tenantId：租户ID
- queryVO：BOM查询对象

**返回值**：List<MtBomVO> - BOM列表

### 19. bomLimitBomBatchQuery

**用途**：批量查询BOM

**参数**：
- tenantId：租户ID
- queryVOs：BOM查询对象列表

**返回值**：List<MtBomVO1> - BOM列表

### 20. bomAllQuery

**用途**：查询BOM完整信息（包括组件、替代等）

**参数**：
- tenantId：租户ID
- queryVO：BOM完整信息查询对象

**返回值**：MtBomVO - BOM完整信息

## 使用示例

### 示例1：批量获取BOM基本信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomBaseVO;

List<Long> bomIds = Arrays.asList(1L, 2L, 3L);
List<MtBomBaseVO> boms = mtBomRpcClient.bomBasicPropertyBatchGet(tenantId, bomIds);
Map<Long, String> bomCodeMap = boms.stream()
    .collect(Collectors.toMap(MtBomBaseVO::getBomId, MtBomBaseVO::getBomCode));
```

### 示例2：根据编码批量查询BOM基本信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomBaseVO;

List<String> bomCodes = Arrays.asList("BOM001", "BOM002", "BOM003");
List<MtBomBaseVO> boms = mtBomRpcClient.codeLimitBomBasicBatchQuery(tenantId, bomCodes);
Map<String, Long> bomIdMap = boms.stream()
    .collect(Collectors.toMap(MtBomBaseVO::getBomCode, MtBomBaseVO::getBomId));
```

### 示例3：查询BOM组件

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomComponentVO1;

MtBomComponentVO1 queryVO = new MtBomComponentVO1();
queryVO.setBomId(bomId);
queryVO.setMaterialId(materialId);
List<MtBomComponentVO1> components = mtBomRpcClient.bomLimitBomComponentQuery(tenantId, queryVO);
```

### 示例4：批量获取BOM组件信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomComponentVO;

List<Long> bomComponentIds = Arrays.asList(1L, 2L, 3L);
List<MtBomComponentVO> components = mtBomRpcClient.bomComponentPropertyBatchGet(tenantId, bomComponentIds);
Map<Long, String> componentMaterialMap = components.stream()
    .collect(Collectors.toMap(MtBomComponentVO::getBomComponentId, MtBomComponentVO::getMaterialId));
```

### 示例5：查询BOM站点分配

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomSiteAssignVO1;

MtBomSiteAssignVO1 queryVO = new MtBomSiteAssignVO1();
queryVO.setBomId(bomId);
queryVO.setSiteId(siteId);
List<MtBomSiteAssignVO1> siteAssigns = mtBomRpcClient.bomLimitBomSiteAssignQuery(tenantId, queryVO);
```

### 示例6：查询BOM替代

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomSubstituteVO;

MtBomSubstituteVO queryVO = new MtBomSubstituteVO();
queryVO.setBomComponentId(bomComponentId);
List<MtBomSubstituteVO> substitutes = mtBomRpcClient.bomLimitBomSubstituteQuery(tenantId, queryVO);
```

### 示例7：查询物料BOM关系

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtMaterialBomRelVO;

MtMaterialBomRelVO queryVO = new MtMaterialBomRelVO();
queryVO.setMaterialId(materialId);
queryVO.setSiteId(siteId);
List<MtMaterialBomRelVO> bomRels = mtBomRpcClient.materialLimitBomRelQuery(tenantId, queryVO);
```

### 示例8：查询BOM完整信息

```java
import org.tarzan.boot.method.client.MtBomRpcClient;
import org.tarzan.method.domain.vo.MtBomVO;

MtBomVO queryVO = new MtBomVO();
queryVO.setBomId(bomId);
queryVO.setBomVersion(bomVersion);
MtBomVO bomAll = mtBomRpcClient.bomAllQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. BOM组件查询需要提供BOM ID和/或物料ID
4. BOM站点分配查询需要提供BOM ID和站点ID
5. BOM替代查询需要提供BOM组件ID
6. 物料BOM关系查询支持按物料和站点查询
7. BOM完整信息查询会返回BOM的所有相关信息，包括组件、替代等
8. 不同方法返回的对象类型不同，使用时需要注意类型转换
9. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量