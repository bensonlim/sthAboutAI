# MtNumRangeRpcClient 方法文档

## 概述

MtNumRangeRpcClient 是一个跨服务客户端，用于生成和管理编码规则相关的信息，包括编码生成、编码规则查询、编码分配等。该客户端主要用于生成各种业务单据的唯一编码。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtNumRangeRpcClient** | `org.tarzan.boot.common.client.MtNumRangeRpcClient` |
| **MtNumRangeInputVO** | `org.tarzan.common.domain.vo.MtNumRangeInputVO` |
| **MtNumRangeOutputVO** | `org.tarzan.common.domain.vo.MtNumRangeOutputVO` |
| **MtNumRangeBatchInputVO** | `org.tarzan.common.domain.vo.MtNumRangeBatchInputVO` |
| **MtNumRangeBatchOutputVO** | `org.tarzan.common.domain.vo.MtNumRangeBatchOutputVO` |
| **MtNumRangeBatchSpecialVO3** | `org.tarzan.common.domain.vo.MtNumRangeBatchSpecialVO3` |
| **MtNumRangeRuleInfoVO** | `org.tarzan.common.domain.vo.MtNumRangeRuleInfoVO` |
| **MtNumRangeRuleVO** | `org.tarzan.common.domain.vo.MtNumRangeRuleVO` |
| **MtNumRangeSerialRuleInfoVO** | `org.tarzan.common.domain.vo.MtNumRangeSerialRuleInfoVO` |

## 方法列表

### 1. numRangeGenerate

**用途**：生成单个编码

**参数**：
- tenantId：租户ID
- inputVO：编码生成输入对象

**返回值**：MtNumRangeOutputVO - 编码生成结果

### 2. numRangeBatchGenerate

**用途**：批量生成编码

**参数**：
- tenantId：租户ID
- batchInputVO：批量编码生成输入对象

**返回值**：MtNumRangeBatchOutputVO - 批量编码生成结果

### 3. numRangeBatchSpecialGenerate

**用途**：批量生成特殊编码（支持自定义规则）

**参数**：
- tenantId：租户ID
- batchSpecialVO：批量特殊编码生成对象

**返回值**：MtNumRangeBatchOutputVO - 批量编码生成结果

### 4. numRangeRulePropertyGet

**用途**：获取单个编码规则信息

**参数**：
- tenantId：租户ID
- numRangeRuleId：编码规则ID

**返回值**：MtNumRangeRuleInfoVO - 编码规则信息

### 5. numRangeRulePropertyBatchGet

**用途**：批量获取编码规则信息

**参数**：
- tenantId：租户ID
- numRangeRuleIds：编码规则ID列表

**返回值**：List<MtNumRangeRuleInfoVO> - 编码规则信息列表

### 6. numRangeRuleQuery

**用途**：查询编码规则

**参数**：
- tenantId：租户ID
- queryVO：编码规则查询对象

**返回值**：List<MtNumRangeRuleVO> - 编码规则列表

### 7. numRangeRuleBatchQuery

**用途**：批量查询编码规则

**参数**：
- tenantId：租户ID
- queryVOs：编码规则查询对象列表

**返回值**：List<MtNumRangeRuleVO> - 编码规则列表

### 8. numRangeSerialRulePropertyGet

**用途**：获取单个编码序列规则信息

**参数**：
- tenantId：租户ID
- numRangeSerialRuleId：编码序列规则ID

**返回值**：MtNumRangeSerialRuleInfoVO - 编码序列规则信息

### 9. numRangeSerialRulePropertyBatchGet

**用途**：批量获取编码序列规则信息

**参数**：
- tenantId：租户ID
- numRangeSerialRuleIds：编码序列规则ID列表

**返回值**：List<MtNumRangeSerialRuleInfoVO> - 编码序列规则信息列表

### 10. numRangeSerialRuleQuery

**用途**：查询编码序列规则

**参数**：
- tenantId：租户ID
- queryVO：编码序列规则查询对象

**返回值**：List<MtNumRangeSerialRuleInfoVO> - 编码序列规则列表

### 11. numRangeSerialRuleBatchQuery

**用途**：批量查询编码序列规则

**参数**：
- tenantId：租户ID
- queryVOs：编码序列规则查询对象列表

**返回值**：List<MtNumRangeSerialRuleInfoVO> - 编码序列规则列表

### 12. numRangeCurrentValueGet

**用途**：获取编码规则当前值

**参数**：
- tenantId：租户ID
- queryVO：编码规则查询对象

**返回值**：Long - 当前序列值

### 13. numRangeCurrentValueBatchGet

**用途**：批量获取编码规则当前值

**参数**：
- tenantId：租户ID
- queryVOs：编码规则查询对象列表

**返回值**：List<Long> - 当前序列值列表

### 14. numRangeReset

**用途**：重置编码规则序列值

**参数**：
- tenantId：租户ID
- resetVO：编码规则重置对象

**返回值**：Boolean - 重置是否成功

### 15. numRangeValidate

**用途**：验证编码是否符合规则

**参数**：
- tenantId：租户ID
- validateVO：编码验证对象

**返回值**：Boolean - 验证结果

### 16. numRangeBatchValidate

**用途**：批量验证编码是否符合规则

**参数**：
- tenantId：租户ID
- validateVOs：编码验证对象列表

**返回值**：List<Boolean> - 验证结果列表

## 使用示例

### 示例1：生成单个编码

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeInputVO;
import org.tarzan.common.domain.vo.MtNumRangeOutputVO;

MtNumRangeInputVO inputVO = new MtNumRangeInputVO();
inputVO.setObjectCode("MO");  // 对象编码，如生产订单
inputVO.setObjectTypeCode("MO_CODE");  // 对象类型编码
inputVO.setSiteId(siteId);  // 站点ID
MtNumRangeOutputVO outputVO = mtNumRangeRpcClient.numRangeGenerate(tenantId, inputVO);
String moCode = outputVO.getNumber();  // 生成的编码
```

### 示例2：批量生成编码

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeBatchInputVO;
import org.tarzan.common.domain.vo.MtNumRangeBatchOutputVO;

MtNumRangeBatchInputVO batchInputVO = new MtNumRangeBatchInputVO();
batchInputVO.setObjectCode("MO");
batchInputVO.setObjectTypeCode("MO_CODE");
batchInputVO.setSiteId(siteId);
batchInputVO.setBatchCount(10);  // 生成10个编码
MtNumRangeBatchOutputVO batchOutputVO = mtNumRangeRpcClient.numRangeBatchGenerate(tenantId, batchInputVO);
List<String> moCodes = batchOutputVO.getNumberList();  // 生成的编码列表
```

### 示例3：批量生成特殊编码

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeBatchSpecialVO3;
import org.tarzan.common.domain.vo.MtNumRangeBatchOutputVO;

MtNumRangeBatchSpecialVO3 batchSpecialVO = new MtNumRangeBatchSpecialVO3();
batchSpecialVO.setObjectCode("MO");
batchSpecialVO.setObjectTypeCode("MO_CODE");
batchSpecialVO.setSiteId(siteId);
batchSpecialVO.setBatchCount(5);
batchSpecialVO.setCallObjectCodeList(Arrays.asList("CALL1", "CALL2"));  // 自定义调用对象
MtNumRangeBatchOutputVO batchOutputVO = mtNumRangeRpcClient.numRangeBatchSpecialGenerate(tenantId, batchSpecialVO);
List<String> moCodes = batchOutputVO.getNumberList();
```

### 示例4：查询编码规则

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeRuleVO;

MtNumRangeRuleVO queryVO = new MtNumRangeRuleVO();
queryVO.setObjectCode("MO");
queryVO.setSiteId(siteId);
List<MtNumRangeRuleVO> rules = mtNumRangeRpcClient.numRangeRuleQuery(tenantId, queryVO);
```

### 示例5：批量获取编码规则信息

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeRuleInfoVO;

List<Long> numRangeRuleIds = Arrays.asList(1L, 2L, 3L);
List<MtNumRangeRuleInfoVO> rules = mtNumRangeRpcClient.numRangeRulePropertyBatchGet(tenantId, numRangeRuleIds);
Map<Long, String> ruleNameMap = rules.stream()
    .collect(Collectors.toMap(MtNumRangeRuleInfoVO::getNumRangeRuleId, MtNumRangeRuleInfoVO::getNumRangeRuleName));
```

### 示例6：获取编码规则当前值

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeRuleVO;

MtNumRangeRuleVO queryVO = new MtNumRangeRuleVO();
queryVO.setNumRangeRuleId(numRangeRuleId);
Long currentValue = mtNumRangeRpcClient.numRangeCurrentValueGet(tenantId, queryVO);
```

### 示例7：重置编码规则序列值

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeRuleVO;

MtNumRangeRuleVO resetVO = new MtNumRangeRuleVO();
resetVO.setNumRangeRuleId(numRangeRuleId);
resetVO.setResetValue(1L);  // 重置为1
Boolean success = mtNumRangeRpcClient.numRangeReset(tenantId, resetVO);
```

### 示例8：验证编码是否符合规则

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeInputVO;

MtNumRangeInputVO validateVO = new MtNumRangeInputVO();
validateVO.setObjectCode("MO");
validateVO.setNumber("MO20240001");
Boolean isValid = mtNumRangeRpcClient.numRangeValidate(tenantId, validateVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 编码生成前需要确保编码规则已配置，包括对象编码、对象类型编码等
3. 批量生成编码时，建议控制批量数量，避免一次性生成过多编码导致性能问题
4. 编码规则通常与站点（Site）关联，生成编码时需要提供站点ID
5. 编码重置操作需谨慎，重置后可能导致编码重复
6. 编码验证用于检查编码是否符合预定义的规则格式
7. 编码序列规则定义了编码的生成方式，如前缀、日期格式、序列号长度等
8. 不同对象类型（如生产订单、工单、物料等）通常有不同的编码规则
9. 编码生成是原子操作，确保生成的编码唯一性
10. 建议在事务中调用编码生成方法，确保业务数据与编码的一致性