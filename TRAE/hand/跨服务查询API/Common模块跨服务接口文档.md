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

**用途**：用于查询和管理计量单位相关信息，支持计量单位类型、转换率计算等功能。

### 2. MtNumRangeRpcClient

**类路径**：`org.tarzan.boot.common.client.MtNumRangeRpcClient`

**主要方法**：
- `numRangeGenerate` - 生成编码
- `numRangeBatchGenerate` - 批量生成编码
- `numRangePropertyGet` - 获取单个编码规则信息
- `numRangePropertyBatchGet` - 批量获取编码规则信息
- `codeLimitNumRangeBasicBatchQuery` - 根据编码批量查询编码规则基本信息
- `numRangeLimitNumRangeQuery` - 查询编码规则
- `numRangeLimitNumRangeBatchQuery` - 批量查询编码规则

**用途**：用于生成和管理编码规则，支持单个和批量生成编码。

### 3. MtExtendRpcClient

**类路径**：`org.tarzan.boot.common.client.MtExtendRpcClient`

**主要方法**：
- `extendAttrPropertyGet` - 获取单个扩展属性信息
- `extendAttrPropertyBatchGet` - 批量获取扩展属性信息
- `codeLimitExtendAttrBasicBatchQuery` - 根据编码批量查询扩展属性基本信息
- `extendAttrLimitExtendAttrQuery` - 查询扩展属性
- `extendAttrLimitExtendAttrBatchQuery` - 批量查询扩展属性
- `extendTableDescPropertyGet` - 获取单个扩展表描述信息
- `extendTableDescPropertyBatchGet` - 批量获取扩展表描述信息
- `codeLimitExtendTableDescBasicBatchQuery` - 根据编码批量查询扩展表描述基本信息
- `extendTableDescLimitExtendTableDescQuery` - 查询扩展表描述
- `extendTableDescLimitExtendTableDescBatchQuery` - 批量查询扩展表描述

**用途**：用于管理扩展属性和扩展表描述信息，支持单个和批量查询。

### 4. MtGenRpcClient

**类路径**：`org.tarzan.boot.common.client.MtGenRpcClient`

**主要方法**：
- `genStatusPropertyGet` - 获取单个生成状态信息
- `genStatusPropertyBatchGet` - 批量获取生成状态信息
- `codeLimitGenStatusBasicBatchQuery` - 根据编码批量查询生成状态基本信息
- `genStatusPropertyGet` - 获取单个生成状态详细信息
- `genStatusPropertyBatchGet` - 批量获取生成状态详细信息
- `genStatusLimitGenStatusQuery` - 查询生成状态
- `genStatusLimitGenStatusBatchQuery` - 批量查询生成状态
- `genTypePropertyGet` - 获取单个生成类型信息
- `genTypePropertyBatchGet` - 批量获取生成类型信息
- `codeLimitGenTypeBasicBatchQuery` - 根据编码批量查询生成类型基本信息
- `genTypePropertyGet` - 获取单个生成类型详细信息
- `genTypePropertyBatchGet` - 批量获取生成类型详细信息
- `genTypeLimitGenTypeQuery` - 查询生成类型
- `genTypeLimitGenTypeBatchQuery` - 批量查询生成类型

**用途**：用于管理生成状态和生成类型信息，支持单个和批量查询。

### 5. MtCommonRpcClient

**类路径**：`org.tarzan.boot.common.client.MtCommonRpcClient`

**主要方法**：
- `attrPropertyGet` - 获取单个属性信息
- `attrPropertyBatchGet` - 批量获取属性信息
- `codeLimitAttrBasicBatchQuery` - 根据编码批量查询属性基本信息
- `attrQuery` - 查询属性
- `attrBatchQuery` - 批量查询属性
- `attrValueGet` - 获取属性值
- `attrValueBatchGet` - 批量获取属性值
- `attrValueQuery` - 查询属性值
- `attrValueBatchQuery` - 批量查询属性值
- `attrUpdate` - 更新属性
- `attrBatchUpdate` - 批量更新属性
- `attrHisQuery` - 查询属性历史记录
- `attrHisBatchQuery` - 批量查询属性历史记录
- `conditionValidate` - 验证条件
- `errorMessageQuery` - 查询错误信息
- `errorMessageBatchQuery` - 批量查询错误信息
- `uiTableQuery` - 查询UI表结构
- `uiTableBatchQuery` - 批量查询UI表结构

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
6. 计量单位转换率计算需要提供源计量单位ID和目标计量单位ID
7. 编码规则生成用于生成各种业务对象的唯一编码
8. 扩展属性用于存储业务对象的自定义属性信息
9. 生成状态和类型用于管理系统中各种生成对象的状态和类型
10. 通用属性管理是系统的基础功能，被多个业务模块使用