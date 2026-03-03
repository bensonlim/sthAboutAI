# MtCommonRpcClient 方法文档

## 概述

MtCommonRpcClient 是一个跨服务客户端，用于处理通用的业务逻辑，包括属性管理、错误处理、条件查询等通用功能。该客户端提供了一系列通用的方法，用于支持各种业务场景。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtCommonRpcClient** | `org.tarzan.boot.common.client.MtCommonRpcClient` |
| **MtAttrVO** | `org.tarzan.common.domain.vo.MtAttrVO` |
| **MtAttrQueryVO** | `org.tarzan.common.domain.vo.MtAttrQueryVO` |
| **MtAttrQueryBatchVO** | `org.tarzan.common.domain.vo.MtAttrQueryBatchVO` |
| **MtAttrUpdateVO** | `org.tarzan.common.domain.vo.MtAttrUpdateVO` |
| **MtAttrUpdateBatchVO** | `org.tarzan.common.domain.vo.MtAttrUpdateBatchVO` |
| **MtAttrValueQueryVO** | `org.tarzan.common.domain.vo.MtAttrValueQueryVO` |
| **MtAttrHisQueryVO** | `org.tarzan.common.domain.vo.MtAttrHisQueryVO` |
| **MtAttrHisBatchQueryVO** | `org.tarzan.common.domain.vo.MtAttrHisBatchQueryVO` |
| **MtAttrHisVO** | `org.tarzan.common.domain.vo.MtAttrHisVO` |
| **MtConditionVO** | `org.tarzan.common.domain.vo.MtConditionVO` |
| **MtErrorMessageVO** | `org.tarzan.common.domain.vo.MtErrorMessageVO` |
| **MtUiTableVO** | `org.tarzan.common.domain.vo.MtUiTableVO` |

## 方法列表

### 1. attrPropertyGet

**用途**：获取单个属性信息

**参数**：
- tenantId：租户ID
- attrId：属性ID

**返回值**：MtAttrVO - 属性信息

### 2. attrPropertyBatchGet

**用途**：批量获取属性信息

**参数**：
- tenantId：租户ID
- attrIds：属性ID列表

**返回值**：List<MtAttrVO> - 属性信息列表

### 3. codeLimitAttrBasicBatchQuery

**用途**：根据编码批量查询属性基本信息

**参数**：
- tenantId：租户ID
- attrCodes：属性编码列表

**返回值**：List<MtAttrVO> - 属性基本信息列表

### 4. attrQuery

**用途**：查询属性

**参数**：
- tenantId：租户ID
- queryVO：属性查询对象

**返回值**：List<MtAttrVO> - 属性列表

### 5. attrBatchQuery

**用途**：批量查询属性

**参数**：
- tenantId：租户ID
- queryVOs：属性查询对象列表

**返回值**：List<MtAttrVO> - 属性列表

### 6. attrValueGet

**用途**：获取属性值

**参数**：
- tenantId：租户ID
- queryVO：属性值查询对象

**返回值**：MtAttrVO - 属性值信息

### 7. attrValueBatchGet

**用途**：批量获取属性值

**参数**：
- tenantId：租户ID
- queryVOs：属性值查询对象列表

**返回值**：List<MtAttrVO> - 属性值信息列表

### 8. attrValueQuery

**用途**：查询属性值

**参数**：
- tenantId：租户ID
- queryVO：属性值查询对象

**返回值**：List<MtAttrVO> - 属性值列表

### 9. attrValueBatchQuery

**用途**：批量查询属性值

**参数**：
- tenantId：租户ID
- queryVOs：属性值查询对象列表

**返回值**：List<MtAttrVO> - 属性值列表

### 10. attrUpdate

**用途**：更新属性

**参数**：
- tenantId：租户ID
- updateVO：属性更新对象

**返回值**：MtAttrVO - 更新后的属性信息

### 11. attrBatchUpdate

**用途**：批量更新属性

**参数**：
- tenantId：租户ID
- updateVOs：属性更新对象列表

**返回值**：List<MtAttrVO> - 更新后的属性信息列表

### 12. attrHisQuery

**用途**：查询属性历史记录

**参数**：
- tenantId：租户ID
- queryVO：属性历史查询对象

**返回值**：List<MtAttrHisVO> - 属性历史记录列表

### 13. attrHisBatchQuery

**用途**：批量查询属性历史记录

**参数**：
- tenantId：租户ID
- queryVOs：属性历史查询对象列表

**返回值**：List<MtAttrHisVO> - 属性历史记录列表

### 14. conditionValidate

**用途**：验证条件

**参数**：
- tenantId：租户ID
- conditionVO：条件验证对象

**返回值**：Boolean - 验证结果

### 15. errorMessageQuery

**用途**：查询错误信息

**参数**：
- tenantId：租户ID
- errorCode：错误编码

**返回值**：MtErrorMessageVO - 错误信息

### 16. errorMessageBatchQuery

**用途**：批量查询错误信息

**参数**：
- tenantId：租户ID
- errorCodes：错误编码列表

**返回值**：List<MtErrorMessageVO> - 错误信息列表

### 17. uiTableQuery

**用途**：查询UI表结构

**参数**：
- tenantId：租户ID
- tableName：表名

**返回值**：MtUiTableVO - UI表结构信息

### 18. uiTableBatchQuery

**用途**：批量查询UI表结构

**参数**：
- tenantId：租户ID
- tableNames：表名列表

**返回值**：List<MtUiTableVO> - UI表结构信息列表

## 使用示例

### 示例1：批量获取属性信息

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrVO;

List<Long> attrIds = Arrays.asList(1L, 2L, 3L);
List<MtAttrVO> attrs = mtCommonRpcClient.attrPropertyBatchGet(tenantId, attrIds);
Map<Long, String> attrCodeMap = attrs.stream()
    .collect(Collectors.toMap(MtAttrVO::getAttrId, MtAttrVO::getAttrCode));
```

### 示例2：根据编码批量查询属性基本信息

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrVO;

List<String> attrCodes = Arrays.asList("COLOR", "SIZE", "WEIGHT");
List<MtAttrVO> attrs = mtCommonRpcClient.codeLimitAttrBasicBatchQuery(tenantId, attrCodes);
Map<String, Long> attrIdMap = attrs.stream()
    .collect(Collectors.toMap(MtAttrVO::getAttrCode, MtAttrVO::getAttrId));
```

### 示例3：查询属性值

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrValueQueryVO;
import org.tarzan.common.domain.vo.MtAttrVO;

MtAttrValueQueryVO queryVO = new MtAttrValueQueryVO();
queryVO.setAttrId(attrId);
queryVO.setObjectId(objectId);
List<MtAttrVO> attrValues = mtCommonRpcClient.attrValueQuery(tenantId, queryVO);
```

### 示例4：更新属性

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrUpdateVO;
import org.tarzan.common.domain.vo.MtAttrVO;

MtAttrUpdateVO updateVO = new MtAttrUpdateVO();
updateVO.setAttrId(attrId);
updateVO.setObjectId(objectId);
updateVO.setAttrValue("RED");
MtAttrVO updatedAttr = mtCommonRpcClient.attrUpdate(tenantId, updateVO);
```

### 示例5：批量更新属性

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrUpdateBatchVO;
import org.tarzan.common.domain.vo.MtAttrVO;

List<MtAttrUpdateBatchVO> updateVOs = Arrays.asList(
    new MtAttrUpdateBatchVO(attrId1, objectId1, "VALUE1"),
    new MtAttrUpdateBatchVO(attrId2, objectId2, "VALUE2")
);
List<MtAttrVO> updatedAttrs = mtCommonRpcClient.attrBatchUpdate(tenantId, updateVOs);
```

### 示例6：查询属性历史记录

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrHisQueryVO;
import org.tarzan.common.domain.vo.MtAttrHisVO;

MtAttrHisQueryVO queryVO = new MtAttrHisQueryVO();
queryVO.setAttrId(attrId);
queryVO.setObjectId(objectId);
List<MtAttrHisVO> hisList = mtCommonRpcClient.attrHisQuery(tenantId, queryVO);
```

### 示例7：验证条件

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtConditionVO;

MtConditionVO conditionVO = new MtConditionVO();
conditionVO.setConditionExpression("AGE > 18");
conditionVO.setParams(Collections.singletonMap("AGE", 20));
Boolean isValid = mtCommonRpcClient.conditionValidate(tenantId, conditionVO);
```

### 8. 查询错误信息

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtErrorMessageVO;

MtErrorMessageVO errorMessage = mtCommonRpcClient.errorMessageQuery(tenantId, "ERROR_CODE_001");
String errorDesc = errorMessage.getErrorMessage();
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 属性管理是通用功能，用于存储和管理业务对象的各种属性
4. 属性值存储在独立的属性值表中，通过属性ID和对象ID关联
5. 属性历史记录用于追踪属性值的变更历史
6. 条件验证用于验证业务规则和条件表达式
7. 错误信息查询用于获取系统预定义的错误消息
8. UI表结构查询用于获取表的元数据信息，支持前端UI展示
9. 不同方法返回的对象类型不同，使用时需要注意类型转换
10. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
11. 属性管理是系统的基础功能，被多个业务模块使用