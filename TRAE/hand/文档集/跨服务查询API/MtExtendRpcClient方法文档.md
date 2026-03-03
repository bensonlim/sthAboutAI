# MtExtendRpcClient 方法文档

## 概述

MtExtendRpcClient 是一个跨服务客户端，用于查询和管理扩展属性（Extend Attribute）相关的信息。扩展属性机制允许为业务对象动态添加自定义字段，而无需修改数据库表结构。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtExtendRpcClient** | `org.tarzan.boot.common.client.MtExtendRpcClient` |
| **MtExtendAttrVO** | `org.tarzan.common.domain.vo.MtExtendAttrVO` |
| **MtExtendVO10** | `org.tarzan.common.domain.vo.MtExtendVO10` |
| **MtExtendVO14** | `org.tarzan.common.domain.vo.MtExtendVO14` |
| **MtExtendTableDescVO** | `org.tarzan.common.domain.vo.MtExtendTableDescVO` |
| **MtExtendTableDescRpcVO** | `org.tarzan.common.domain.vo.MtExtendTableDescRpcVO` |
| **MtExtendColumnRpcVO** | `org.tarzan.common.domain.vo.MtExtendColumnRpcVO` |
| **MtExtendRpcVO** | `org.tarzan.common.domain.vo.MtExtendRpcVO` |
| **MtCommonExtendVO5** | `org.tarzan.common.domain.vo.MtCommonExtendVO5` |
| **MtCommonExtendAttrHisVO2** | `org.tarzan.common.domain.vo.MtCommonExtendAttrHisVO2` |

## 方法列表

### 1. extendAttrPropertyGet

**用途**：获取单个扩展属性信息

**参数**：
- tenantId：租户ID
- extendAttrId：扩展属性ID

**返回值**：MtExtendAttrVO - 扩展属性信息

### 2. extendAttrPropertyBatchGet

**用途**：批量获取扩展属性信息

**参数**：
- tenantId：租户ID
- extendAttrIds：扩展属性ID列表

**返回值**：List<MtExtendAttrVO> - 扩展属性信息列表

### 3. extendAttrQuery

**用途**：查询扩展属性

**参数**：
- tenantId：租户ID
- queryVO：扩展属性查询对象

**返回值**：List<MtExtendAttrVO> - 扩展属性列表

### 4. extendAttrBatchQuery

**用途**：批量查询扩展属性

**参数**：
- tenantId：租户ID
- queryVOs：扩展属性查询对象列表

**返回值**：List<MtExtendAttrVO> - 扩展属性列表

### 5. extendTableDescPropertyGet

**用途**：获取单个扩展表描述信息

**参数**：
- tenantId：租户ID
- extendTableDescId：扩展表描述ID

**返回值**：MtExtendTableDescVO - 扩展表描述信息

### 6. extendTableDescPropertyBatchGet

**用途**：批量获取扩展表描述信息

**参数**：
- tenantId：租户ID
- extendTableDescIds：扩展表描述ID列表

**返回值**：List<MtExtendTableDescVO> - 扩展表描述信息列表

### 7. extendTableDescQuery

**用途**：查询扩展表描述

**参数**：
- tenantId：租户ID
- queryVO：扩展表描述查询对象

**返回值**：List<MtExtendTableDescRpcVO> - 扩展表描述列表

### 8. extendTableDescBatchQuery

**用途**：批量查询扩展表描述

**参数**：
- tenantId：租户ID
- queryVOs：扩展表描述查询对象列表

**返回值**：List<MtExtendTableDescRpcVO> - 扩展表描述列表

### 9. extendColumnPropertyGet

**用途**：获取单个扩展列信息

**参数**：
- tenantId：租户ID
- extendColumnId：扩展列ID

**返回值**：MtExtendColumnRpcVO - 扩展列信息

### 10. extendColumnPropertyBatchGet

**用途**：批量获取扩展列信息

**参数**：
- tenantId：租户ID
- extendColumnIds：扩展列ID列表

**返回值**：List<MtExtendColumnRpcVO> - 扩展列信息列表

### 11. extendColumnQuery

**用途**：查询扩展列

**参数**：
- tenantId：租户ID
- queryVO：扩展列查询对象

**返回值**：List<MtExtendColumnRpcVO> - 扩展列列表

### 12. extendColumnBatchQuery

**用途**：批量查询扩展列

**参数**：
- tenantId：租户ID
- queryVOs：扩展列查询对象列表

**返回值**：List<MtExtendColumnRpcVO> - 扩展列列表

### 13. extendAttrValueGet

**用途**：获取扩展属性值

**参数**：
- tenantId：租户ID
- queryVO：扩展属性值查询对象

**返回值**：MtExtendRpcVO - 扩展属性值信息

### 14. extendAttrValueBatchGet

**用途**：批量获取扩展属性值

**参数**：
- tenantId：租户ID
- queryVOs：扩展属性值查询对象列表

**返回值**：List<MtExtendRpcVO> - 扩展属性值信息列表

### 15. extendAttrValueQuery

**用途**：查询扩展属性值

**参数**：
- tenantId：租户ID
- queryVO：扩展属性值查询对象

**返回值**：List<MtCommonExtendVO5> - 扩展属性值列表

### 16. extendAttrValueBatchQuery

**用途**：批量查询扩展属性值

**参数**：
- tenantId：租户ID
- queryVOs：扩展属性值查询对象列表

**返回值**：List<MtCommonExtendVO5> - 扩展属性值列表

### 17. extendAttrHisQuery

**用途**：查询扩展属性历史记录

**参数**：
- tenantId：租户ID
- queryVO：扩展属性历史查询对象

**返回值**：List<MtCommonExtendAttrHisVO2> - 扩展属性历史记录列表

### 18. extendAttrHisBatchQuery

**用途**：批量查询扩展属性历史记录

**参数**：
- tenantId：租户ID
- queryVOs：扩展属性历史查询对象列表

**返回值**：List<MtCommonExtendAttrHisVO2> - 扩展属性历史记录列表

### 19. extendSettingsQuery

**用途**：查询扩展设置

**参数**：
- tenantId：租户ID
- queryVO：扩展设置查询对象

**返回值**：List<MtExtendVO10> - 扩展设置列表

### 20. extendSettingsBatchQuery

**用途**：批量查询扩展设置

**参数**：
- tenantId：租户ID
- queryVOs：扩展设置查询对象列表

**返回值**：List<MtExtendVO10> - 扩展设置列表

### 21. extendTableDescValidate

**用途**：验证扩展表描述

**参数**：
- tenantId：租户ID
- validateVO：扩展表描述验证对象

**返回值**：Boolean - 验证结果

### 22. extendColumnValidate

**用途**：验证扩展列

**参数**：
- tenantId：租户ID
- validateVO：扩展列验证对象

**返回值**：Boolean - 验证结果

## 使用示例

### 示例1：批量获取扩展属性信息

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendAttrVO;

List<Long> extendAttrIds = Arrays.asList(1L, 2L, 3L);
List<MtExtendAttrVO> extendAttrs = mtExtendRpcClient.extendAttrPropertyBatchGet(tenantId, extendAttrIds);
Map<Long, String> attrNameMap = extendAttrs.stream()
    .collect(Collectors.toMap(MtExtendAttrVO::getExtendAttrId, MtExtendAttrVO::getAttrName));
```

### 示例2：查询扩展属性

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendAttrVO;

MtExtendAttrVO queryVO = new MtExtendAttrVO();
queryVO.setTableId(tableId);
queryVO.setAttrName("CUSTOM_FIELD");
List<MtExtendAttrVO> extendAttrs = mtExtendRpcClient.extendAttrQuery(tenantId, queryVO);
```

### 示例3：查询扩展表描述

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendTableDescRpcVO;

MtExtendTableDescRpcVO queryVO = new MtExtendTableDescRpcVO();
queryVO.setTableName("MT_MATERIAL");
List<MtExtendTableDescRpcVO> tableDescs = mtExtendRpcClient.extendTableDescQuery(tenantId, queryVO);
```

### 示例4：批量获取扩展列信息

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendColumnRpcVO;

List<Long> extendColumnIds = Arrays.asList(1L, 2L, 3L);
List<MtExtendColumnRpcVO> columns = mtExtendRpcClient.extendColumnPropertyBatchGet(tenantId, extendColumnIds);
Map<Long, String> columnNameMap = columns.stream()
    .collect(Collectors.toMap(MtExtendColumnRpcVO::getExtendColumnId, MtExtendColumnRpcVO::getColumnName));
```

### 示例5：获取扩展属性值

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendRpcVO;

MtExtendRpcVO queryVO = new MtExtendRpcVO();
queryVO.setTableName("MT_MATERIAL");
queryVO.setKeyId(materialId);
queryVO.setAttrName("CUSTOM_ATTR");
MtExtendRpcVO attrValue = mtExtendRpcClient.extendAttrValueGet(tenantId, queryVO);
String value = attrValue.getAttrValue();
```

### 示例6：批量获取扩展属性值

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendRpcVO;

List<MtExtendRpcVO> queryVOs = Arrays.asList(
    new MtExtendRpcVO("MT_MATERIAL", materialId1, "ATTR1"),
    new MtExtendRpcVO("MT_MATERIAL", materialId2, "ATTR2")
);
List<MtExtendRpcVO> attrValues = mtExtendRpcClient.extendAttrValueBatchGet(tenantId, queryVOs);
```

### 示例7：查询扩展属性历史记录

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtCommonExtendAttrHisVO2;

MtCommonExtendAttrHisVO2 queryVO = new MtCommonExtendAttrHisVO2();
queryVO.setTableName("MT_MATERIAL");
queryVO.setKeyId(materialId);
queryVO.setAttrName("CUSTOM_ATTR");
List<MtCommonExtendAttrHisVO2> hisList = mtExtendRpcClient.extendAttrHisQuery(tenantId, queryVO);
```

### 示例8：查询扩展设置

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendVO10;

MtExtendVO10 queryVO = new MtExtendVO10();
queryVO.setTableName("MT_MATERIAL");
List<MtExtendVO10> settings = mtExtendRpcClient.extendSettingsQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 扩展属性机制允许为业务对象动态添加自定义字段，无需修改数据库表结构
3. 扩展表描述定义了哪些业务表支持扩展属性
4. 扩展列定义了扩展属性的字段信息，如字段名、数据类型、长度等
5. 扩展属性值存储在独立的扩展属性表中，通过表名和主键ID关联
6. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
7. 扩展属性历史记录用于追踪扩展属性值的变更历史
8. 不同方法返回的对象类型不同，使用时需要注意类型转换
9. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
10. 扩展属性常用于存储业务特定的自定义信息，如物料的额外规格、订单的特殊标记等
11. 使用扩展属性前需要先在扩展表描述和扩展列中配置相关定义