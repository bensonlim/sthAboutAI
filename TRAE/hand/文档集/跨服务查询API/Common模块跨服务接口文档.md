# Common模块跨服务接口文档

## 概述

Common模块包含了通用功能相关的跨服务接口，用于处理计量单位、编码规则、扩展属性、生成状态和类型、通用属性等通用业务逻辑。

## 接口列表

### 1. MtUomRpcClient

**类路径**：`org.tarzan.boot.common.client.MtUomRpcClient`

**主要方法**：
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

**用途**：用于生成和管理编码规则，支持单个和批量生成编码。

### 3. MtExtendRpcClient

**类路径**：`org.tarzan.boot.common.client.MtExtendRpcClient`

**主要方法**：
- `tableLimitAttrNameQuery` - 根据表查询属性名称
- `tableLimitExtendDescQuery` - 根据表查询扩展描述
- `tableLimitExtendDescBatchQuery` - 批量根据表查询扩展描述

**用途**：用于管理扩展属性和扩展表描述信息，支持单个和批量查询。

### 4. MtGenRpcClient

**类路径**：`org.tarzan.boot.common.client.MtGenRpcClient`

**主要方法**：
- `groupLimitTypeQuery` - 根据组查询类型
- `getTypeCodeDescMap` - 获取类型编码描述映射
- `conditionLimitGenTypePropertyQuery` - 根据条件查询生成类型属性
- `groupLimitStatusQuery` - 根据组查询状态
- `getStatusCodeDescMap` - 获取状态编码描述映射

**用途**：用于管理生成状态和生成类型信息，支持单个和批量查询。

### 5. MtCommonRpcClient

**类路径**：`org.tarzan.boot.common.client.MtCommonRpcClient`

**主要方法**：
- `getErrorMessage` - 获取错误信息
- `getBatchErrorMessage` - 批量获取错误信息

**用途**：用于处理通用属性管理、条件验证、错误信息查询和UI表结构查询等通用功能。

## 使用示例

### 示例1：获取单个计量单位详细信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

Long uomId = 1L;
MtUomBaseVO uom = mtUomRpcClient.uomPropertyGet(tenantId, uomId);
System.out.println("计量单位编码：" + uom.getUomCode());
System.out.println("计量单位名称：" + uom.getUomName());
```

### 示例2：批量获取计量单位详细信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

List<Long> uomIds = Arrays.asList(1L, 2L, 3L);
List<MtUomBaseVO> uoms = mtUomRpcClient.uomPropertyBatchGet(tenantId, uomIds);
Map<Long, String> uomCodeMap = uoms.stream()
    .collect(Collectors.toMap(MtUomBaseVO::getUomId, MtUomBaseVO::getUomCode));
```

### 示例3：根据编码批量获取计量单位详细信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

List<String> uomCodes = Arrays.asList("EA", "KG", "M");
List<MtUomBaseVO> uoms = mtUomRpcClient.uomPropertyBatchGetByCodes(tenantId, uomCodes);
Map<String, MtUomBaseVO> uomMap = uoms.stream()
    .collect(Collectors.toMap(MtUomBaseVO::getUomCode, uom -> uom));
```

### 示例4：查询计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;
import org.tarzan.common.domain.vo.MtUomQueryVO;

MtUomQueryVO queryVO = new MtUomQueryVO();
queryVO.setUomType("LENGTH");
List<MtUomBaseVO> uoms = mtUomRpcClient.uomLimitUomQuery(tenantId, queryVO);
```

### 示例5：批量查询计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;
import org.tarzan.common.domain.vo.MtUomQueryVO;

List<MtUomQueryVO> queryVOs = new ArrayList<>();
MtUomQueryVO queryVO1 = new MtUomQueryVO();
queryVO1.setUomType("LENGTH");
queryVOs.add(queryVO1);

MtUomQueryVO queryVO2 = new MtUomQueryVO();
queryVO2.setUomType("WEIGHT");
queryVOs.add(queryVO2);

List<List<MtUomBaseVO>> result = mtUomRpcClient.uomLimitUomBatchQuery(tenantId, queryVOs);
```

### 示例6：获取单个计量单位类型信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomTypeBaseVO;

Long uomTypeId = 1L;
MtUomTypeBaseVO uomType = mtUomRpcClient.uomTypePropertyGet(tenantId, uomTypeId);
System.out.println("计量单位类型编码：" + uomType.getUomTypeCode());
System.out.println("计量单位类型名称：" + uomType.getUomTypeName());
```

### 示例7：批量获取计量单位类型信息

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomTypeBaseVO;

List<Long> uomTypeIds = Arrays.asList(1L, 2L, 3L);
List<MtUomTypeBaseVO> uomTypes = mtUomRpcClient.uomTypePropertyBatchGet(tenantId, uomTypeIds);
Map<Long, String> uomTypeMap = uomTypes.stream()
    .collect(Collectors.toMap(MtUomTypeBaseVO::getUomTypeId, MtUomTypeBaseVO::getUomTypeCode));
```

### 示例8：查询计量单位类型

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomTypeBaseVO;
import org.tarzan.common.domain.vo.MtUomTypeQueryVO;

MtUomTypeQueryVO queryVO = new MtUomTypeQueryVO();
queryVO.setEnableFlag("Y");
List<MtUomTypeBaseVO> uomTypes = mtUomRpcClient.uomTypeLimitUomTypeQuery(tenantId, queryVO);
```

### 示例9：获取计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomConversionRateVO;

Long fromUomId = 1L; // 源计量单位ID
Long toUomId = 2L;   // 目标计量单位ID
MtUomConversionRateVO conversionRate = mtUomRpcClient.uomConversionRateGet(tenantId, fromUomId, toUomId);
System.out.println("转换率：" + conversionRate.getConversionRate());
```

### 示例10：批量获取计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomConversionRateVO;
import org.tarzan.common.domain.vo.MtUomConversionRateQueryVO;

List<MtUomConversionRateQueryVO> queryVOs = new ArrayList<>();
MtUomConversionRateQueryVO queryVO1 = new MtUomConversionRateQueryVO();
queryVO1.setFromUomId(1L);
queryVO1.setToUomId(2L);
queryVOs.add(queryVO1);

MtUomConversionRateQueryVO queryVO2 = new MtUomConversionRateQueryVO();
queryVO2.setFromUomId(2L);
queryVO2.setToUomId(3L);
queryVOs.add(queryVO2);

List<MtUomConversionRateVO> conversionRates = mtUomRpcClient.uomConversionRateBatchGet(tenantId, queryVOs);
```

### 示例11：计算计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import java.math.BigDecimal;

Long fromUomId = 1L; // 源计量单位ID
Long toUomId = 2L;   // 目标计量单位ID
BigDecimal quantity = new BigDecimal(100); // 数量
BigDecimal convertedQuantity = mtUomRpcClient.uomConversionRateCalculate(tenantId, fromUomId, toUomId, quantity);
System.out.println("转换后的数量：" + convertedQuantity);
```

### 示例12：批量计算计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomConversionCalculateVO;
import java.math.BigDecimal;

List<MtUomConversionCalculateVO> calculateVOs = new ArrayList<>();
MtUomConversionCalculateVO calculateVO1 = new MtUomConversionCalculateVO();
calculateVO1.setFromUomId(1L);
calculateVO1.setToUomId(2L);
calculateVO1.setQuantity(new BigDecimal(100));
calculateVOs.add(calculateVO1);

MtUomConversionCalculateVO calculateVO2 = new MtUomConversionCalculateVO();
calculateVO2.setFromUomId(2L);
calculateVO2.setToUomId(3L);
calculateVO2.setQuantity(new BigDecimal(50));
calculateVOs.add(calculateVO2);

List<BigDecimal> results = mtUomRpcClient.uomConversionRateBatchCalculate(tenantId, calculateVOs);
```

### 示例13：获取主计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

Long materialId = 1L; // 物料ID
MtUomBaseVO primaryUom = mtUomRpcClient.uomPrimaryUomGet(tenantId, materialId);
System.out.println("主计量单位：" + primaryUom.getUomCode());
```

### 示例14：批量获取主计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

List<Long> materialIds = Arrays.asList(1L, 2L, 3L);
List<MtUomBaseVO> primaryUoms = mtUomRpcClient.uomPrimaryUomBatchGet(tenantId, materialIds);
Map<Long, String> materialUomMap = primaryUoms.stream()
    .collect(Collectors.toMap(MtUomBaseVO::getMaterialId, MtUomBaseVO::getUomCode));
```

### 示例15：计量单位转换

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import java.math.BigDecimal;

Long fromUomId = 1L; // 源计量单位ID
Long toUomId = 2L;   // 目标计量单位ID
BigDecimal quantity = new BigDecimal(100); // 数量
BigDecimal convertedQuantity = mtUomRpcClient.uomConversion(tenantId, fromUomId, toUomId, quantity);
System.out.println("转换后的数量：" + convertedQuantity);
```

### 示例16：批量进行计量单位转换

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomConversionVO;
import java.math.BigDecimal;

List<MtUomConversionVO> conversionVOs = new ArrayList<>();
MtUomConversionVO conversionVO1 = new MtUomConversionVO();
conversionVO1.setFromUomId(1L);
conversionVO1.setToUomId(2L);
conversionVO1.setQuantity(new BigDecimal(100));
conversionVOs.add(conversionVO1);

MtUomConversionVO conversionVO2 = new MtUomConversionVO();
conversionVO2.setFromUomId(2L);
conversionVO2.setToUomId(3L);
conversionVO2.setQuantity(new BigDecimal(50));
conversionVOs.add(conversionVO2);

List<BigDecimal> results = mtUomRpcClient.uomBatchConversion(tenantId, conversionVOs);
```

### 示例17：生成编码

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeOutputVO;

String objectCode = "ORDER";
String numRangeCode = "SO";
MtNumRangeOutputVO outputVO = mtNumRangeRpcClient.numrangeGenerate(tenantId, objectCode, numRangeCode);
System.out.println("生成的编码：" + outputVO.getGeneratedCode());
```

### 示例18：批量生成编码（推荐）

```java
import org.tarzan.boot.common.client.MtNumRangeRpcClient;
import org.tarzan.common.domain.vo.MtNumRangeBatchInputVO;
import org.tarzan.common.domain.vo.MtNumRangeBatchOutputVO;

MtNumRangeBatchInputVO inputVO = new MtNumRangeBatchInputVO("ORDER", "SO");
List<MtNumRangeBatchOutputVO> outputVOs = mtNumRangeRpcClient.numrangeBatchGenerate(tenantId, inputVO);
Map<String, String> codeMap = outputVOs.stream()
    .collect(Collectors.toMap(MtNumRangeBatchOutputVO::getObjectCode, MtNumRangeBatchOutputVO::getGeneratedCode));
```

### 示例19：根据表查询属性名称

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendAttrNameVO;

String tableName = "MT_SAMPLE_TABLE";
List<MtExtendAttrNameVO> attrNames = mtExtendRpcClient.tableLimitAttrNameQuery(tenantId, tableName);
```

### 示例20：根据表查询扩展描述

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendTableDescVO;

String tableName = "MT_SAMPLE_TABLE";
MtExtendTableDescVO tableDesc = mtExtendRpcClient.tableLimitExtendDescQuery(tenantId, tableName);
System.out.println("表描述：" + tableDesc.getTableDesc());
```

### 示例21：批量根据表查询扩展描述

```java
import org.tarzan.boot.common.client.MtExtendRpcClient;
import org.tarzan.common.domain.vo.MtExtendTableDescVO;

List<String> tableNames = Arrays.asList("MT_SAMPLE_TABLE1", "MT_SAMPLE_TABLE2");
List<MtExtendTableDescVO> tableDescs = mtExtendRpcClient.tableLimitExtendDescBatchQuery(tenantId, tableNames);
Map<String, MtExtendTableDescVO> tableDescMap = tableDescs.stream()
    .collect(Collectors.toMap(MtExtendTableDescVO::getTableName, desc -> desc));
```

### 示例22：根据组查询类型

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeVO;

String groupCode = "ORDER_TYPE";
List<MtGenTypeVO> types = mtGenRpcClient.groupLimitTypeQuery(tenantId, groupCode);
```

### 示例23：获取类型编码描述映射

```java
import org.tarzan.boot.common.client.MtGenRpcClient;

String groupCode = "ORDER_TYPE";
Map<String, String> typeCodeDescMap = mtGenRpcClient.getTypeCodeDescMap(tenantId, groupCode);
```

### 示例24：根据条件查询生成类型属性

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeVO;
import org.tarzan.common.domain.vo.MtGenTypeQueryVO;

MtGenTypeQueryVO queryVO = new MtGenTypeQueryVO();
queryVO.setGroupCode("ORDER_TYPE");
queryVO.setEnableFlag("Y");
List<MtGenTypeVO> types = mtGenRpcClient.conditionLimitGenTypePropertyQuery(tenantId, queryVO);
```

### 示例25：根据组查询状态

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenStatusVO;

String groupCode = "ORDER_STATUS";
List<MtGenStatusVO> statuses = mtGenRpcClient.groupLimitStatusQuery(tenantId, groupCode);
```

### 示例26：获取状态编码描述映射

```java
import org.tarzan.boot.common.client.MtGenRpcClient;

String groupCode = "ORDER_STATUS";
Map<String, String> statusCodeDescMap = mtGenRpcClient.getStatusCodeDescMap(tenantId, groupCode);
```

### 示例27：获取错误信息（推荐）

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;

String errorMessage = mtCommonRpcClient.getErrorMessage(tenantId, "ERROR_CODE", "param1", "param2");
System.out.println("错误信息：" + errorMessage);
```

### 示例28：批量获取错误信息

```java
import org.tarzan.boot.common.client.MtCommonRpcClient;
import org.tarzan.common.domain.vo.MtErrorMessageVO;

List<String> errorCodes = Arrays.asList("ERROR_CODE1", "ERROR_CODE2");
List<MtErrorMessageVO> errorMessages = mtCommonRpcClient.getBatchErrorMessage(tenantId, errorCodes);
Map<String, String> errorMessageMap = errorMessages.stream()
    .collect(Collectors.toMap(MtErrorMessageVO::getErrorCode, MtErrorMessageVO::getErrorMessage));
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 不同方法返回的对象类型不同，使用时需要注意类型转换
4. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
5. 计量单位转换率计算需要提供源计量单位ID和目标计量单位ID
6. 编码规则生成用于生成各种业务对象的唯一编码
7. 扩展属性用于存储业务对象的自定义属性信息
8. 生成状态和类型用于管理系统中各种生成对象的状态和类型
9. 通用属性管理是系统的基础功能，被多个业务模块使用