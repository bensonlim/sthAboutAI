# MtMethodAttrRpcClient 方法文档

## 概述

MtMethodAttrRpcClient 是一个跨服务客户端，用于查询方法模块属性相关的信息，包括分发路线属性、分发路线位置属性等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtMethodAttrRpcClient** | `org.tarzan.boot.method.client.MtMethodAttrRpcClient` |
| **MtDisRouteAttrQueryVO** | `org.tarzan.method.domain.vo.MtDisRouteAttrQueryVO` |
| **MtDisRouteAttrQueryVO1** | `org.tarzan.method.domain.vo.MtDisRouteAttrQueryVO1` |
| **MtDisRouteAttrUpdateVO** | `org.tarzan.method.domain.vo.MtDisRouteAttrUpdateVO` |
| **MtDisRouteLocationAttrVO1** | `org.tarzan.method.domain.vo.MtDisRouteLocationAttrVO1` |
| **MtDisRouteLocationAttrVO3** | `org.tarzan.method.domain.vo.MtDisRouteLocationAttrVO3` |

## 方法列表

### 1. disRouteAttrPropertyGet

**用途**：获取单个分发路线属性信息

**参数**：
- tenantId：租户ID
- disRouteAttrId：分发路线属性ID

**返回值**：MtDisRouteAttrQueryVO - 分发路线属性信息

### 2. disRouteAttrPropertyBatchGet

**用途**：批量获取分发路线属性信息

**参数**：
- tenantId：租户ID
- disRouteAttrIds：分发路线属性ID列表

**返回值**：List<MtDisRouteAttrQueryVO> - 分发路线属性信息列表

### 3. disRouteAttrQuery

**用途**：查询分发路线属性

**参数**：
- tenantId：租户ID
- queryVO：分发路线属性查询对象

**返回值**：List<MtDisRouteAttrQueryVO1> - 分发路线属性列表

### 4. disRouteAttrBatchQuery

**用途**：批量查询分发路线属性

**参数**：
- tenantId：租户ID
- queryVOs：分发路线属性查询对象列表

**返回值**：List<MtDisRouteAttrQueryVO1> - 分发路线属性列表

### 5. disRouteAttrUpdate

**用途**：更新分发路线属性

**参数**：
- tenantId：租户ID
- updateVO：分发路线属性更新对象

**返回值**：MtDisRouteAttrUpdateVO - 更新结果

### 6. disRouteAttrBatchUpdate

**用途**：批量更新分发路线属性

**参数**：
- tenantId：租户ID
- updateVOs：分发路线属性更新对象列表

**返回值**：List<MtDisRouteAttrUpdateVO> - 更新结果列表

### 7. disRouteLocationAttrPropertyGet

**用途**：获取单个分发路线位置属性信息

**参数**：
- tenantId：租户ID
- disRouteLocationAttrId：分发路线位置属性ID

**返回值**：MtDisRouteLocationAttrVO1 - 分发路线位置属性信息

### 8. disRouteLocationAttrPropertyBatchGet

**用途**：批量获取分发路线位置属性信息

**参数**：
- tenantId：租户ID
- disRouteLocationAttrIds：分发路线位置属性ID列表

**返回值**：List<MtDisRouteLocationAttrVO1> - 分发路线位置属性信息列表

### 9. disRouteLocationAttrQuery

**用途**：查询分发路线位置属性

**参数**：
- tenantId：租户ID
- queryVO：分发路线位置属性查询对象

**返回值**：List<MtDisRouteLocationAttrVO3> - 分发路线位置属性列表

### 10. disRouteLocationAttrBatchQuery

**用途**：批量查询分发路线位置属性

**参数**：
- tenantId：租户ID
- queryVOs：分发路线位置属性查询对象列表

**返回值**：List<MtDisRouteLocationAttrVO3> - 分发路线位置属性列表

## 使用示例

### 示例1：批量获取分发路线属性信息

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteAttrQueryVO;

List<Long> disRouteAttrIds = Arrays.asList(1L, 2L, 3L);
List<MtDisRouteAttrQueryVO> disRouteAttrs = mtMethodAttrRpcClient.disRouteAttrPropertyBatchGet(tenantId, disRouteAttrIds);
Map<Long, String> attrNameMap = disRouteAttrs.stream()
    .collect(Collectors.toMap(MtDisRouteAttrQueryVO::getDisRouteAttrId, MtDisRouteAttrQueryVO::getAttrName));
```

### 示例2：查询分发路线属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteAttrQueryVO1;

MtDisRouteAttrQueryVO1 queryVO = new MtDisRouteAttrQueryVO1();
queryVO.setDisRouteId(disRouteId);
queryVO.setAttrName("PRIORITY");
List<MtDisRouteAttrQueryVO1> disRouteAttrs = mtMethodAttrRpcClient.disRouteAttrQuery(tenantId, queryVO);
```

### 示例3：更新分发路线属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteAttrUpdateVO;

MtDisRouteAttrUpdateVO updateVO = new MtDisRouteAttrUpdateVO();
updateVO.setDisRouteAttrId(disRouteAttrId);
updateVO.setAttrValue("HIGH");
MtDisRouteAttrUpdateVO result = mtMethodAttrRpcClient.disRouteAttrUpdate(tenantId, updateVO);
```

### 示例4：批量更新分发路线属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteAttrUpdateVO;

List<MtDisRouteAttrUpdateVO> updateVOs = Arrays.asList(
    new MtDisRouteAttrUpdateVO(disRouteAttrId1, "VALUE1"),
    new MtDisRouteAttrUpdateVO(disRouteAttrId2, "VALUE2")
);
List<MtDisRouteAttrUpdateVO> results = mtMethodAttrRpcClient.disRouteAttrBatchUpdate(tenantId, updateVOs);
```

### 示例5：批量获取分发路线位置属性信息

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteLocationAttrVO1;

List<Long> disRouteLocationAttrIds = Arrays.asList(1L, 2L, 3L);
List<MtDisRouteLocationAttrVO1> disRouteLocationAttrs = mtMethodAttrRpcClient.disRouteLocationAttrPropertyBatchGet(tenantId, disRouteLocationAttrIds);
Map<Long, String> locationAttrNameMap = disRouteLocationAttrs.stream()
    .collect(Collectors.toMap(MtDisRouteLocationAttrVO1::getDisRouteLocationAttrId, MtDisRouteLocationAttrVO1::getAttrName));
```

### 示例6：查询分发路线位置属性

```java
import org.tarzan.boot.method.client.MtMethodAttrRpcClient;
import org.tarzan.method.domain.vo.MtDisRouteLocationAttrVO3;

MtDisRouteLocationAttrVO3 queryVO = new MtDisRouteLocationAttrVO3();
queryVO.setDisRouteId(disRouteId);
queryVO.setLocationId(locationId);
List<MtDisRouteLocationAttrVO3> disRouteLocationAttrs = mtMethodAttrRpcClient.disRouteLocationAttrQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 分发路线属性查询需要提供分发路线ID和/或属性名称
4. 分发路线位置属性查询需要提供分发路线ID和/或位置ID
5. 属性更新操作会修改数据库中的属性值，请谨慎操作
6. 不同方法返回的对象类型不同，使用时需要注意类型转换
7. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
8. 分发路线属性用于配置分发路线的各种参数，如优先级、规则等
9. 分发路线位置属性用于配置分发路线在特定位置的属性