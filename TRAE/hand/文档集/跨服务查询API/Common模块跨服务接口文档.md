# Common模块跨服务接口文档

## 概述

Common模块包含了通用功能相关的跨服务接口，用于处理计量单位、编码规则、扩展属性、生成状态和类型、通用属性等通用业务逻辑。

## 接口列表

### 1. MtUomRpcClient

**类路径**：`org.tarzan.boot.common.client.MtUomRpcClient`

**主要方法**：
- `uomBasicPropertyGet` - 获取单个计量单位基本信息（已过期）
- `uomBasicPropertyBatchGet` - 批量获取计量单位基本信息（已过期）
- `codeLimitUomBasicBatchQuery` - 根据编码批量查询计量单位基本信息（已过期）
- `uomPropertyGet` - 获取单个计量单位详细信息
- `uomPropertyBatchGet` - 批量获取计量单位详细信息
- `uomPropertyBatchGetByCodes` - 根据编码批量获取计量单位详细信息
- `uomLimitUomQuery` - 查询计量单位
- `uomLimitUomBatchQuery` - 批量查询计量单位
- `uomTypePropertyGet` - 获取单个计量单位类型信息
- `uomTypePropertyBatchGet` - 批量获取计量单位类型信息
- `uomTypeLimitUomTypeQuery` - 查询计量单位类型
- `uomConversionRateGet` - 获取计量单位转换率
- `uomConversionRateBatchGet` - 批量获取计量单位转换率
- `uomConversionRateQuery` - 查询计量单位转换率
- `uomConversionRateBatchQuery` - 批量查询计量单位转换率
- `uomConversionRateCalculate` - 计算计量单位转换率
- `uomConversionRateBatchCalculate` - 批量计算计量单位转换率
- `uomPrimaryUomGet` - 获取主计量单位
- `uomPrimaryUomBatchGet` - 批量获取主计量单位
- `primaryUomGet` - 获取主计量单位
- `primaryUomBatchGet` - 批量获取主计量单位
- `propertyListLimitUomPropertyQuery` - 根据属性列表查询计量单位属性
- `uomDecimalProcessAlgorithm` - 计量单位小数处理算法
- `uomDecimalProcess` - 计量单位小数处理
- `uomDecimalBatchProcess` - 批量处理计量单位小数
- `uomConversionAlgorithm` - 计量单位转换算法
- `uomConversion` - 计量单位转换
- `uomBatchConversion` - 批量进行计量单位转换

**用途**：用于查询和管理计量单位相关信息，支持计量单位类型、转换率计算、小数处理、主计量单位查询等功能。

### 2. MtNumRangeRpcClient

**类路径**：`org.tarzan.boot.common.client.MtNumRangeRpcClient`

**主要方法**：
- `numrangeGenerate` - 生成编码
- `numrangeBatchGenerate` - 批量生成编码
- `numRangeGenerate` - 生成编码（已过期）
- `numRangeBatchGenerate` - 批量生成编码（已过期）
- `numRangePropertyGet` - 获取单个编码规则信息（已过期）
- `numRangePropertyBatchGet` - 批量获取编码规则信息（已过期）
- `codeLimitNumRangeBasicBatchQuery` - 根据编码批量查询编码规则基本信息（已过期）
- `numRangeLimitNumRangeQuery` - 查询编码规则（已过期）
- `numRangeLimitNumRangeBatchQuery` - 批量查询编码规则（已过期）

**用途**：用于生成和管理编码规则，支持单个和批量生成编码。

### 3. MtExtendRpcClient

**类路径**：`org.tarzan.boot.common.client.MtExtendRpcClient`

**主要方法**：
- `tableLimitAttrNameQuery` - 根据表查询属性名称
- `tableLimitExtendDescQuery` - 根据表查询扩展描述
- `tableLimitExtendDescBatchQuery` - 批量根据表查询扩展描述
- `extendAttrPropertyGet` - 获取单个扩展属性信息（已过期）
- `extendAttrPropertyBatchGet` - 批量获取扩展属性信息（已过期）
- `codeLimitExtendAttrBasicBatchQuery` - 根据编码批量查询扩展属性基本信息（已过期）
- `extendAttrLimitExtendAttrQuery` - 查询扩展属性（已过期）
- `extendAttrLimitExtendAttrBatchQuery` - 批量查询扩展属性（已过期）
- `extendTableDescPropertyGet` - 获取单个扩展表描述信息（已过期）
- `extendTableDescPropertyBatchGet` - 批量获取扩展表描述信息（已过期）
- `codeLimitExtendTableDescBasicBatchQuery` - 根据编码批量查询扩展表描述基本信息（已过期）
- `extendTableDescLimitExtendTableDescQuery` - 查询扩展表描述（已过期）
- `extendTableDescLimitExtendTableDescBatchQuery` - 批量查询扩展表描述（已过期）

**用途**：用于管理扩展属性和扩展表描述信息，支持单个和批量查询。

### 4. MtGenRpcClient

**类路径**：`org.tarzan.boot.common.client.MtGenRpcClient`

**主要方法**：
- `groupLimitTypeQuery` - 根据组查询类型
- `getTypeCodeDescMap` - 获取类型编码描述映射
- `conditionLimitGenTypePropertyQuery` - 根据条件查询生成类型属性
- `groupLimitStatusQuery` - 根据组查询状态
- `getStatusCodeDescMap` - 获取状态编码描述映射
- `genStatusPropertyGet` - 获取单个生成状态信息（已过期）
- `genStatusPropertyBatchGet` - 批量获取生成状态信息（已过期）
- `codeLimitGenStatusBasicBatchQuery` - 根据编码批量查询生成状态基本信息（已过期）
- `genStatusLimitGenStatusQuery` - 查询生成状态（已过期）
- `genStatusLimitGenStatusBatchQuery` - 批量查询生成状态（已过期）
- `genTypePropertyGet` - 获取单个生成类型信息（已过期）
- `genTypePropertyBatchGet` - 批量获取生成类型信息（已过期）
- `codeLimitGenTypeBasicBatchQuery` - 根据编码批量查询生成类型基本信息（已过期）
- `genTypeLimitGenTypeQuery` - 查询生成类型（已过期）
- `genTypeLimitGenTypeBatchQuery` - 批量查询生成类型（已过期）

**用途**：用于管理生成状态和生成类型信息，支持单个和批量查询。

### 5. MtCommonRpcClient

**类路径**：`org.tarzan.boot.common.client.MtCommonRpcClient`

**主要方法**：
- `getErrorMessage` - 获取错误信息
- `getBatchErrorMessage` - 批量获取错误信息
- `attrPropertyGet` - 获取单个属性信息（已过期）
- `attrPropertyBatchGet` - 批量获取属性信息（已过期）
- `codeLimitAttrBasicBatchQuery` - 根据编码批量查询属性基本信息（已过期）
- `attrQuery` - 查询属性（已过期）
- `attrBatchQuery` - 批量查询属性（已过期）
- `attrValueGet` - 获取属性值（已过期）
- `attrValueBatchGet` - 批量获取属性值（已过期）
- `attrValueQuery` - 查询属性值（已过期）
- `attrValueBatchQuery` - 批量查询属性值（已过期）
- `attrUpdate` - 更新属性（已过期）
- `attrBatchUpdate` - 批量更新属性（已过期）
- `attrHisQuery` - 查询属性历史记录（已过期）
- `attrHisBatchQuery` - 批量查询属性历史记录（已过期）
- `conditionValidate` - 验证条件（已过期）
- `errorMessageQuery` - 查询错误信息（已过期）
- `errorMessageBatchQuery` - 批量查询错误信息（已过期）
- `uiTableQuery` - 查询UI表结构（已过期）
- `uiTableBatchQuery` - 批量查询UI表结构（已过期）

**用途**：用于处理通用属性管理、条件验证、错误信息查询和UI表结构查询等通用功能。

## 使用示例

### 示例1：批量获取计量单位详细信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

List<Long> uomIds = Arrays.asList(1L, 2L, 3L);
List<MtUomBaseVO> uoms = mtUomRpcClient.uomPropertyBatchGet(tenantId, uomIds);
Map<Long, String> uomCodeMap = uoms.stream()
    .collect(Collectors.toMap(MtUomBaseVO::getUomId, MtUomBaseVO::getUomCode));
```

### 示例2：批量生成编码

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeBatchInputVO;
import org.tarzan.common.domain.vo.MtNumRangeBatchOutputVO;

List<MtNumRangeBatchInputVO> inputVOs = Arrays.asList(
    new MtNumRangeBatchInputVO("ORDER", "SO"),
    new MtNumRangeBatchInputVO("ORDER", "PO")
);
List<MtNumRangeBatchOutputVO> outputVOs = mtNumRangeRpcClient.numRangeBatchGenerate(tenantId, inputVOs);
Map<String, String> codeMap = outputVOs.stream()
    .collect(Collectors.toMap(MtNumRangeBatchOutputVO::getObjectCode, MtNumRangeBatchOutputVO::getGeneratedCode));
```

### 示例3：批量获取属性信息

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtAttrVO;

List<Long> attrIds = Arrays.asList(1L, 2L, 3L);
List<MtAttrVO> attrs = mtCommonRpcClient.attrPropertyBatchGet(tenantId, attrIds);
Map<Long, String> attrCodeMap = attrs.stream()
    .collect(Collectors.toMap(MtAttrVO::getAttrId, MtAttrVO::getAttrCode));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 以下方法已过期，建议使用替代方法：
   - uomBasicPropertyGet → 建议使用 uomPropertyGet
   - uomBasicPropertyBatchGet → 建议使用 uomPropertyBatchGet
   - codeLimitUomBasicBatchQuery → 建议使用 uomLimitUomBatchQuery

6. 以下编码规则相关方法已过期：
   - numRangeGenerate → 建议使用 numrangeGenerate
   - numRangeBatchGenerate → 建议使用 numrangeBatchGenerate
   - numRangePropertyGet
   - numRangePropertyBatchGet
   - codeLimitNumRangeBasicBatchQuery
   - numRangeLimitNumRangeQuery
   - numRangeLimitNumRangeBatchQuery

7. 以下扩展属性相关方法已过期：
   - extendAttrPropertyGet
   - extendAttrPropertyBatchGet
   - codeLimitExtendAttrBasicBatchQuery
   - extendAttrLimitExtendAttrQuery
   - extendAttrLimitExtendAttrBatchQuery
   - extendTableDescPropertyGet
   - extendTableDescPropertyBatchGet
   - codeLimitExtendTableDescBasicBatchQuery
   - extendTableDescLimitExtendTableDescQuery
   - extendTableDescLimitExtendTableDescBatchQuery
   建议使用新的方法如 tableLimitAttrNameQuery、tableLimitExtendDescQuery 等。

8. 以下生成状态和类型相关方法已过期：
   - genStatusPropertyGet
   - genStatusPropertyBatchGet
   - codeLimitGenStatusBasicBatchQuery
   - genStatusLimitGenStatusQuery
   - genStatusLimitGenStatusBatchQuery
   - genTypePropertyGet
   - genTypePropertyBatchGet
   - codeLimitGenTypeBasicBatchQuery
   - genTypeLimitGenTypeQuery
   - genTypeLimitGenTypeBatchQuery
   建议使用新的方法如 groupLimitTypeQuery、getTypeCodeDescMap、groupLimitStatusQuery 等。

9. 以下通用属性相关方法已过期：
   - attrPropertyGet
   - attrPropertyBatchGet
   - codeLimitAttrBasicBatchQuery
   - attrQuery
   - attrBatchQuery
   - attrValueGet
   - attrValueBatchGet
   - attrValueQuery
   - attrValueBatchQuery
   - attrUpdate
   - attrBatchUpdate
   - attrHisQuery
   - attrHisBatchQuery
   - conditionValidate
   - errorMessageQuery
   - errorMessageBatchQuery
   - uiTableQuery
   - uiTableBatchQuery
   建议使用新的方法如 getErrorMessage、getBatchErrorMessage 等。
10. 计量单位转换率计算需要提供源计量单位ID和目标计量单位ID
11. 编码规则生成用于生成各种业务对象的唯一编码
12. 扩展属性用于存储业务对象的自定义属性信息
13. 生成状态和类型用于管理系统中各种生成对象的状态和类型
14. 通用属性管理是系统的基础功能，被多个业务模块使用