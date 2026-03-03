# MtOrganizationRpcClient 方法文档

## 概述

MtOrganizationRpcClient 是一个跨服务客户端，用于查询组织相关的信息，包括组织属性、组织关系等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtOrganizationRpcClient** | `org.tarzan.boot.model.client.MtOrganizationRpcClient` |
| **MtModOrganizationBaseVO** | `org.tarzan.model.domain.vo.MtModOrganizationBaseVO` |
| **MtModOrganizationRelVO8** | `org.tarzan.model.domain.vo.MtModOrganizationRelVO8` |
| **MtModOrganizationRelVO9** | `org.tarzan.model.domain.vo.MtModOrganizationRelVO9` |
| **MtModOrganizationRelVO14** | `org.tarzan.model.domain.vo.MtModOrganizationRelVO14` |

## 方法列表

### 1. codeListLimitOrganizationPropertyGet

**用途**：根据组织编码列表获取组织属性

**参数**：
- tenantId：租户ID
- orgCodeList：组织编码列表

**返回值**：List<MtModOrganizationBaseVO> - 组织属性列表

### 2. organizationPropertyBatchGet

**用途**：批量获取组织属性

**参数**：
- tenantId：租户ID
- organizationIds：组织ID列表

**返回值**：List<MtModOrganizationBaseVO> - 组织属性列表

### 3. organizationLimitSchedulePropertyBatchGet

**用途**：批量获取组织的计划属性

**参数**：
- tenantId：租户ID
- voList：组织计划属性查询对象列表

**返回值**：List<MtModOrganizationBaseVO> - 组织计划属性列表

### 4. parentOrganizationRelQuery

**用途**：查询父组织关系

**参数**：
- tenantId：租户ID
- mtModOrganizationRelVO9：组织关系查询对象

**返回值**：List<MtModOrganizationRelVO8> - 父组织关系列表

### 5. organizationPropertyGet

**用途**：获取单个组织的属性

**参数**：
- tenantId：租户ID
- organizationId：组织ID

**返回值**：MtModOrganizationBaseVO - 组织属性

### 6. subOrganizationRelQuery

**用途**：查询子组织关系

**参数**：
- tenantId：租户ID
- mtModOrganizationRelVO9：组织关系查询对象

**返回值**：List<MtModOrganizationRelVO8> - 子组织关系列表

### 7. organizationLimitSchedulePropertyGet

**用途**：获取单个组织的计划属性

**参数**：
- tenantId：租户ID
- orgVo：组织计划属性查询对象

**返回值**：MtModOrganizationBaseVO - 组织计划属性

### 8. parentOrgLimitSubOrgRelTreeQuery

**用途**：查询父组织限制下的子组织关系树

**参数**：
- tenantId：租户ID
- relVO11List：组织关系查询对象列表

**返回值**：List<MtModOrganizationRelVO14> - 子组织关系树列表

## 使用示例

### 示例1：批量获取组织属性

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationBaseVO;

List<Long> organizationIds = Arrays.asList(1L, 2L, 3L);
List<MtModOrganizationBaseVO> organizations = mtOrganizationRpcClient.organizationPropertyBatchGet(tenantId, organizationIds);
Map<Long, String> orgCodeMap = organizations.stream()
    .collect(Collectors.toMap(MtModOrganizationBaseVO::getOrganizationId, MtModOrganizationBaseVO::getOrganizationCode));
```

### 示例2：查询子组织关系

```java
import org.tarzan.boot.model.client.MtOrganizationRpcClient;
import org.tarzan.model.domain.vo.MtModOrganizationRelVO9;
import org.tarzan.model.domain.vo.MtModOrganizationRelVO8;

MtModOrganizationRelVO9 mtModOrganizationRelVO9 = new MtModOrganizationRelVO9();
mtModOrganizationRelVO9.setOrganizationIds(Arrays.asList(siteId));
mtModOrganizationRelVO9.setTargetOrganizationType("WORKCELL");
mtModOrganizationRelVO9.setQueryType("ALL");
List<MtModOrganizationRelVO8> vo8List = mtOrganizationRpcClient.subOrganizationRelQuery(tenantId, mtModOrganizationRelVO9);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 组织关系查询需要正确设置查询对象的参数，以获取正确的组织关系信息