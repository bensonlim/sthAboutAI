# MtUomRpcClient 方法文档

## 概述

MtUomRpcClient 是一个跨服务客户端，用于查询计量单位（UOM - Unit of Measure）相关的信息，包括计量单位基本信息、计量单位转换、计量单位类型等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtUomRpcClient** | `org.tarzan.boot.common.client.MtUomRpcClient` |
| **MtUomBaseVO** | `org.tarzan.common.domain.vo.MtUomBaseVO` |
| **MtUomVO1** | `org.tarzan.common.domain.vo.MtUomVO1` |
| **MtUomVO2** | `org.tarzan.common.domain.vo.MtUomVO2` |
| **MtUomVO3** | `org.tarzan.common.domain.vo.MtUomVO3` |
| **MtUomVO4** | `org.tarzan.common.domain.vo.MtUomVO4` |
| **MtUomVO5** | `org.tarzan.common.domain.vo.MtUomVO5` |
| **MtUomVO6** | `org.tarzan.common.domain.vo.MtUomVO6` |
| **MtUomVO7** | `org.tarzan.common.domain.vo.MtUomVO7` |
| **MtUomVO8** | `org.tarzan.common.domain.vo.MtUomVO8` |
| **MtUomVO9** | `org.tarzan.common.domain.vo.MtUomVO9` |
| **MtUomVO10** | `org.tarzan.common.domain.vo.MtUomVO10` |

## 方法列表

### 1. uomBasicPropertyGet

**用途**：获取单个计量单位基本信息

**状态**：已过期

**参数**：
- tenantId：租户ID
- uomId：计量单位ID

**返回值**：MtUomBaseVO - 计量单位基本信息

**替代方法**：建议使用 uomPropertyGet 方法获取单个计量单位详细信息

### 2. uomBasicPropertyBatchGet

**用途**：批量获取计量单位基本信息

**状态**：已过期

**参数**：
- tenantId：租户ID
- uomIds：计量单位ID列表

**返回值**：List<MtUomBaseVO> - 计量单位基本信息列表

**替代方法**：建议使用 uomPropertyBatchGet 方法批量获取计量单位详细信息

### 3. codeLimitUomBasicBatchQuery

**用途**：根据编码批量查询计量单位基本信息

**状态**：已过期

**参数**：
- tenantId：租户ID
- uomCodes：计量单位编码列表

**返回值**：List<MtUomBaseVO> - 计量单位基本信息列表

**替代方法**：建议使用 uomLimitUomBatchQuery 方法根据编码批量查询计量单位详细信息

### 4. uomPropertyGet

**用途**：获取单个计量单位详细信息

**参数**：
- tenantId：租户ID
- uomId：计量单位ID

**返回值**：MtUomBaseVO - 计量单位详细信息

### 5. uomPropertyBatchGet

**用途**：批量获取计量单位详细信息

**参数**：
- tenantId：租户ID
- uomIds：计量单位ID列表

**返回值**：List<MtUomBaseVO> - 计量单位详细信息列表

### 6. uomLimitUomQuery

**用途**：查询计量单位

**参数**：
- tenantId：租户ID
- queryVO：计量单位查询对象

**返回值**：List<MtUomVO2> - 计量单位列表

### 7. uomLimitUomBatchQuery

**用途**：批量查询计量单位

**参数**：
- tenantId：租户ID
- queryVOs：计量单位查询对象列表

**返回值**：List<MtUomVO3> - 计量单位列表

### 8. uomTypePropertyGet

**用途**：获取单个计量单位类型信息

**参数**：
- tenantId：租户ID
- uomTypeId：计量单位类型ID

**返回值**：MtUomVO4 - 计量单位类型信息

### 9. uomTypePropertyBatchGet

**用途**：批量获取计量单位类型信息

**参数**：
- tenantId：租户ID
- uomTypeIds：计量单位类型ID列表

**返回值**：List<MtUomVO4> - 计量单位类型信息列表

### 10. uomTypeLimitUomTypeQuery

**用途**：查询计量单位类型

**参数**：
- tenantId：租户ID
- queryVO：计量单位类型查询对象

**返回值**：List<MtUomVO5> - 计量单位类型列表

### 11. uomConversionRateGet

**用途**：获取计量单位转换率

**参数**：
- tenantId：租户ID
- queryVO：计量单位转换率查询对象

**返回值**：MtUomVO6 - 计量单位转换率信息

### 12. uomConversionRateBatchGet

**用途**：批量获取计量单位转换率

**参数**：
- tenantId：租户ID
- queryVOs：计量单位转换率查询对象列表

**返回值**：List<MtUomVO6> - 计量单位转换率信息列表

### 13. uomConversionRateQuery

**用途**：查询计量单位转换率

**参数**：
- tenantId：租户ID
- queryVO：计量单位转换率查询对象

**返回值**：List<MtUomVO7> - 计量单位转换率列表

### 14. uomConversionRateBatchQuery

**用途**：批量查询计量单位转换率

**参数**：
- tenantId：租户ID
- queryVOs：计量单位转换率查询对象列表

**返回值**：List<MtUomVO7> - 计量单位转换率列表

### 15. uomConversionRateCalculate

**用途**：计算计量单位转换率

**参数**：
- tenantId：租户ID
- calculateVO：计量单位转换率计算对象

**返回值**：MtUomVO8 - 计量单位转换率计算结果

### 16. uomConversionRateBatchCalculate

**用途**：批量计算计量单位转换率

**参数**：
- tenantId：租户ID
- calculateVOs：计量单位转换率计算对象列表

**返回值**：List<MtUomVO8> - 计量单位转换率计算结果列表

### 17. uomPrimaryUomGet

**用途**：获取主计量单位

**参数**：
- tenantId：租户ID
- queryVO：主计量单位查询对象

**返回值**：MtUomVO9 - 主计量单位信息

### 18. uomPrimaryUomBatchGet

**用途**：批量获取主计量单位

**参数**：
- tenantId：租户ID
- queryVOs：主计量单位查询对象列表

**返回值**：List<MtUomVO9> - 主计量单位信息列表

### 19. uomLimitUomTypeQuery

**用途**：查询计量单位类型下的计量单位

**参数**：
- tenantId：租户ID
- queryVO：计量单位类型查询对象

**返回值**：List<MtUomVO10> - 计量单位列表

### 20. uomTypeLimitUomQuery

**用途**：根据计量单位类型查询计量单位

**参数**：
- tenantId：租户ID
- queryVO：计量单位查询对象

**返回值**：List<MtUomVO2> - 计量单位列表

## 使用示例

### 示例1：批量获取计量单位详细信息（推荐）

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomBaseVO;

List<Long> uomIds = Arrays.asList(1L, 2L, 3L);
List<MtUomBaseVO> uoms = mtUomRpcClient.uomPropertyBatchGet(tenantId, uomIds);
Map<Long, String> uomCodeMap = uoms.stream()
    .collect(Collectors.toMap(MtUomBaseVO::getUomId, MtUomBaseVO::getUomCode));
```

### 示例2：根据编码批量查询计量单位详细信息（推荐）

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO2;
import org.tarzan.common.domain.vo.MtUomVO3;

List<MtUomVO2> queryVOs = Arrays.asList(
    new MtUomVO2("PCS"),
    new MtUomVO2("KG"),
    new MtUomVO2("M")
);
List<MtUomVO3> uoms = mtUomRpcClient.uomLimitUomBatchQuery(tenantId, queryVOs);
Map<String, Long> uomIdMap = uoms.stream()
    .collect(Collectors.toMap(MtUomVO3::getUomCode, MtUomVO3::getUomId));
```

### 示例3：查询计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO2;

MtUomVO2 queryVO = new MtUomVO2();
queryVO.setUomTypeId(uomTypeId);
queryVO.setUomCode("PCS");
List<MtUomVO2> uoms = mtUomRpcClient.uomLimitUomQuery(tenantId, queryVO);
```

### 示例4：获取计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO6;

MtUomVO6 queryVO = new MtUomVO6();
queryVO.setFromUomId(fromUomId);
queryVO.setToUomId(toUomId);
MtUomVO6 conversionRate = mtUomRpcClient.uomConversionRateGet(tenantId, queryVO);
```

### 示例5：计算计量单位转换率

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO8;

MtUomVO8 calculateVO = new MtUomVO8();
calculateVO.setFromUomId(fromUomId);
calculateVO.setToUomId(toUomId);
calculateVO.setPrimaryValue(new BigDecimal("100"));
MtUomVO8 result = mtUomRpcClient.uomConversionRateCalculate(tenantId, calculateVO);
```

### 示例6：获取主计量单位

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO9;

MtUomVO9 queryVO = new MtUomVO9();
queryVO.setUomId(uomId);
MtUomVO9 primaryUom = mtUomRpcClient.uomPrimaryUomGet(tenantId, queryVO);
```

### 示例7：查询计量单位类型

```java
import org.tarzan.boot.common.client.MtUomRpcClient;
import org.tarzan.common.domain.vo.MtUomVO5;

MtUomVO5 queryVO = new MtUomVO5();
queryVO.setUomTypeCode("WEIGHT");
List<MtUomVO5> uomTypes = mtUomRpcClient.uomTypeLimitUomTypeQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 计量单位转换率计算需要提供源计量单位ID和目标计量单位ID
4. 计量单位查询支持按计量单位类型和编码查询
5. 主计量单位是计量单位类型下的默认计量单位
6. 不同方法返回的对象类型不同，使用时需要注意类型转换
7. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
8. 计量单位转换率用于在不同计量单位之间进行数值转换
9. 常用的计量单位类型包括：数量（QTY）、重量（WEIGHT）、长度（LENGTH）、体积（VOLUME）等
10. 以下方法已过期，建议使用替代方法：
    - uomBasicPropertyGet → 建议使用 uomPropertyGet
    - uomBasicPropertyBatchGet → 建议使用 uomPropertyBatchGet
    - codeLimitUomBasicBatchQuery → 建议使用 uomLimitUomBatchQuery