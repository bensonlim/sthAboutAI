# MtGenRpcClient 方法文档

## 概述

MtGenRpcClient 是一个跨服务客户端，用于查询和管理生成状态（Gen Status）和生成类型（Gen Type）相关的信息。生成状态和生成类型主要用于管理各种业务对象的生成过程和类型定义。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtGenRpcClient** | `org.tarzan.boot.common.client.MtGenRpcClient` |
| **MtGenStatusBaseVO** | `org.tarzan.common.domain.vo.MtGenStatusBaseVO` |
| **MtGenStatusVO** | `org.tarzan.common.domain.vo.MtGenStatusVO` |
| **MtGenStatusVO2** | `org.tarzan.common.domain.vo.MtGenStatusVO2` |
| **MtGenTypeBaseVO** | `org.tarzan.common.domain.vo.MtGenTypeBaseVO` |
| **MtGenTypeVO** | `org.tarzan.common.domain.vo.MtGenTypeVO` |
| **MtGenTypeVO2** | `org.tarzan.common.domain.vo.MtGenTypeVO2` |

## 方法列表

### 1. genStatusPropertyGet

**用途**：获取单个生成状态信息

**参数**：
- tenantId：租户ID
- genStatusId：生成状态ID

**返回值**：MtGenStatusBaseVO - 生成状态信息

### 2. genStatusPropertyBatchGet

**用途**：批量获取生成状态信息

**参数**：
- tenantId：租户ID
- genStatusIds：生成状态ID列表

**返回值**：List<MtGenStatusBaseVO> - 生成状态信息列表

### 3. codeLimitGenStatusBasicBatchQuery

**用途**：根据编码批量查询生成状态基本信息

**参数**：
- tenantId：租户ID
- genStatusCodes：生成状态编码列表

**返回值**：List<MtGenStatusBaseVO> - 生成状态基本信息列表

### 4. genStatusPropertyGet

**用途**：获取单个生成状态详细信息

**参数**：
- tenantId：租户ID
- genStatusId：生成状态ID

**返回值**：MtGenStatusVO - 生成状态详细信息

### 5. genStatusPropertyBatchGet

**用途**：批量获取生成状态详细信息

**参数**：
- tenantId：租户ID
- genStatusIds：生成状态ID列表

**返回值**：List<MtGenStatusVO> - 生成状态详细信息列表

### 6. genStatusLimitGenStatusQuery

**用途**：查询生成状态

**参数**：
- tenantId：租户ID
- queryVO：生成状态查询对象

**返回值**：List<MtGenStatusVO2> - 生成状态列表

### 7. genStatusLimitGenStatusBatchQuery

**用途**：批量查询生成状态

**参数**：
- tenantId：租户ID
- queryVOs：生成状态查询对象列表

**返回值**：List<MtGenStatusVO2> - 生成状态列表

### 8. genTypePropertyGet

**用途**：获取单个生成类型信息

**参数**：
- tenantId：租户ID
- genTypeId：生成类型ID

**返回值**：MtGenTypeBaseVO - 生成类型信息

### 9. genTypePropertyBatchGet

**用途**：批量获取生成类型信息

**参数**：
- tenantId：租户ID
- genTypeIds：生成类型ID列表

**返回值**：List<MtGenTypeBaseVO> - 生成类型信息列表

### 10. codeLimitGenTypeBasicBatchQuery

**用途**：根据编码批量查询生成类型基本信息

**参数**：
- tenantId：租户ID
- genTypeCodes：生成类型编码列表

**返回值**：List<MtGenTypeBaseVO> - 生成类型基本信息列表

### 11. genTypePropertyGet

**用途**：获取单个生成类型详细信息

**参数**：
- tenantId：租户ID
- genTypeId：生成类型ID

**返回值**：MtGenTypeVO - 生成类型详细信息

### 12. genTypePropertyBatchGet

**用途**：批量获取生成类型详细信息

**参数**：
- tenantId：租户ID
- genTypeIds：生成类型ID列表

**返回值**：List<MtGenTypeVO> - 生成类型详细信息列表

### 13. genTypeLimitGenTypeQuery

**用途**：查询生成类型

**参数**：
- tenantId：租户ID
- queryVO：生成类型查询对象

**返回值**：List<MtGenTypeVO2> - 生成类型列表

### 14. genTypeLimitGenTypeBatchQuery

**用途**：批量查询生成类型

**参数**：
- tenantId：租户ID
- queryVOs：生成类型查询对象列表

**返回值**：List<MtGenTypeVO2> - 生成类型列表

## 使用示例

### 示例1：批量获取生成状态信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenStatusBaseVO;

List<Long> genStatusIds = Arrays.asList(1L, 2L, 3L);
List<MtGenStatusBaseVO> genStatuses = mtGenRpcClient.genStatusPropertyBatchGet(tenantId, genStatusIds);
Map<Long, String> genStatusCodeMap = genStatuses.stream()
    .collect(Collectors.toMap(MtGenStatusBaseVO::getGenStatusId, MtGenStatusBaseVO::getGenStatusCode));
```

### 示例2：根据编码批量查询生成状态基本信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenStatusBaseVO;

List<String> genStatusCodes = Arrays.asList("CREATED", "IN_PROGRESS", "COMPLETED");
List<MtGenStatusBaseVO> genStatuses = mtGenRpcClient.codeLimitGenStatusBasicBatchQuery(tenantId, genStatusCodes);
Map<String, Long> genStatusIdMap = genStatuses.stream()
    .collect(Collectors.toMap(MtGenStatusBaseVO::getGenStatusCode, MtGenStatusBaseVO::getGenStatusId));
```

### 示例3：批量获取生成状态详细信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenStatusVO;

List<Long> genStatusIds = Arrays.asList(1L, 2L, 3L);
List<MtGenStatusVO> genStatuses = mtGenRpcClient.genStatusPropertyBatchGet(tenantId, genStatusIds);
Map<Long, String> genStatusNameMap = genStatuses.stream()
    .collect(Collectors.toMap(MtGenStatusVO::getGenStatusId, MtGenStatusVO::getGenStatusName));
```

### 示例4：查询生成状态

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenStatusVO2;

MtGenStatusVO2 queryVO = new MtGenStatusVO2();
queryVO.setGenStatusCode("COMPLETED");
List<MtGenStatusVO2> genStatuses = mtGenRpcClient.genStatusLimitGenStatusQuery(tenantId, queryVO);
```

### 示例5：批量获取生成类型信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeBaseVO;

List<Long> genTypeIds = Arrays.asList(1L, 2L, 3L);
List<MtGenTypeBaseVO> genTypes = mtGenRpcClient.genTypePropertyBatchGet(tenantId, genTypeIds);
Map<Long, String> genTypeCodeMap = genTypes.stream()
    .collect(Collectors.toMap(MtGenTypeBaseVO::getGenTypeId, MtGenTypeBaseVO::getGenTypeCode));
```

### 示例6：根据编码批量查询生成类型基本信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeBaseVO;

List<String> genTypeCodes = Arrays.asList("AUTO", "MANUAL", "SCHEDULED");
List<MtGenTypeBaseVO> genTypes = mtGenRpcClient.codeLimitGenTypeBasicBatchQuery(tenantId, genTypeCodes);
Map<String, Long> genTypeIdMap = genTypes.stream()
    .collect(Collectors.toMap(MtGenTypeBaseVO::getGenTypeCode, MtGenTypeBaseVO::getGenTypeId));
```

### 示例7：批量获取生成类型详细信息

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeVO;

List<Long> genTypeIds = Arrays.asList(1L, 2L, 3L);
List<MtGenTypeVO> genTypes = mtGenRpcClient.genTypePropertyBatchGet(tenantId, genTypeIds);
Map<Long, String> genTypeNameMap = genTypes.stream()
    .collect(Collectors.toMap(MtGenTypeVO::getGenTypeId, MtGenTypeVO::getGenTypeName));
```

### 示例8：查询生成类型

```java
import org.tarzan.boot.common.client.MtGenRpcClient;
import org.tarzan.common.domain.vo.MtGenTypeVO2;

MtGenTypeVO2 queryVO = new MtGenTypeVO2();
queryVO.setGenTypeCode("AUTO");
List<MtGenTypeVO2> genTypes = mtGenRpcClient.genTypeLimitGenTypeQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 生成状态用于表示业务对象生成过程中的不同阶段，如创建、进行中、完成等
4. 生成类型用于表示业务对象的生成方式，如自动生成、手动生成、计划生成等
5. 不同方法返回的对象类型不同，使用时需要注意类型转换
6. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
7. 生成状态和生成类型通常用于日志记录、状态跟踪和业务流程管理
8. 生成状态编码和生成类型编码通常是系统预定义的，具有特定的业务含义
9. 使用生成状态和生成类型前，需要确保相关的编码已在系统中定义