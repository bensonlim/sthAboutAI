# MtCalendarRpcClient 方法文档

## 概述

MtCalendarRpcClient 是一个跨服务客户端，用于查询日历相关的信息，包括日历基本信息、班次信息、工作日信息、组织日历关系等。

## 类路径

| 类名 | 包路径 |
|------|--------|
| **MtCalendarRpcClient** | `org.tarzan.boot.model.client.MtCalendarRpcClient` |
| **MtCalendarBaseVO** | `org.tarzan.model.domain.vo.MtCalendarBaseVO` |
| **MtCalendarShiftBaseVO** | `org.tarzan.model.domain.vo.MtCalendarShiftBaseVO` |
| **MtCalendarShiftVO** | `org.tarzan.model.domain.vo.MtCalendarShiftVO` |
| **MtCalendarShiftVO1** | `org.tarzan.model.domain.vo.MtCalendarShiftVO1` |
| **MtCalendarShiftWorkDayVO** | `org.tarzan.model.domain.vo.MtCalendarShiftWorkDayVO` |
| **MtCalendarOrgRelVO** | `org.tarzan.model.domain.vo.MtCalendarOrgRelVO` |
| **MtCalendarOrgRelVO1** | `org.tarzan.model.domain.vo.MtCalendarOrgRelVO1` |
| **MtCalendarVO2** | `org.tarzan.model.domain.vo.MtCalendarVO2` |

## 方法列表

### 1. calendarBasicPropertyGet

**用途**：获取单个日历基本信息

**参数**：
- tenantId：租户ID
- calendarId：日历ID

**返回值**：MtCalendarBaseVO - 日历基本信息

### 2. calendarBasicPropertyBatchGet

**用途**：批量获取日历基本信息

**参数**：
- tenantId：租户ID
- calendarIds：日历ID列表

**返回值**：List<MtCalendarBaseVO> - 日历基本信息列表

### 3. codeLimitCalendarBasicBatchQuery

**用途**：根据编码批量查询日历基本信息

**参数**：
- tenantId：租户ID
- calendarCodes：日历编码列表

**返回值**：List<MtCalendarBaseVO> - 日历基本信息列表

### 4. calendarShiftPropertyGet

**用途**：获取单个班次基本信息

**参数**：
- tenantId：租户ID
- shiftId：班次ID

**返回值**：MtCalendarShiftBaseVO - 班次基本信息

### 5. calendarShiftPropertyBatchGet

**用途**：批量获取班次基本信息

**参数**：
- tenantId：租户ID
- shiftIds：班次ID列表

**返回值**：List<MtCalendarShiftBaseVO> - 班次基本信息列表

### 6. codeLimitCalendarShiftBatchQuery

**用途**：根据编码批量查询班次基本信息

**参数**：
- tenantId：租户ID
- shiftCodes：班次编码列表

**返回值**：List<MtCalendarShiftBaseVO> - 班次基本信息列表

### 7. calendarShiftWorkDayQuery

**用途**：查询班次工作日信息

**参数**：
- tenantId：租户ID
- queryVO：班次工作日查询对象

**返回值**：MtCalendarShiftWorkDayVO - 班次工作日信息

### 8. calendarShiftWorkDayBatchQuery

**用途**：批量查询班次工作日信息

**参数**：
- tenantId：租户ID
- queryVO：班次工作日查询对象列表

**返回值**：List<MtCalendarShiftWorkDayVO> - 班次工作日信息列表

### 9. calendarLimitOrgRelQuery

**用途**：查询日历组织关系

**参数**：
- tenantId：租户ID
- queryVO：日历组织关系查询对象

**返回值**：List<MtCalendarOrgRelVO> - 日历组织关系列表

### 10. calendarLimitShiftQuery

**用途**：查询班次信息

**参数**：
- tenantId：租户ID
- queryVO：班次查询对象

**返回值**：List<MtCalendarShiftVO> - 班次信息列表

### 11. calendarLimitCalendarQuery

**用途**：查询日历信息

**参数**：
- tenantId：租户ID
- queryVO：日历查询对象

**返回值**：List<MtCalendarVO2> - 日历信息列表

### 12. calendarLimitShiftDetailQuery

**用途**：查询班次详细信息

**参数**：
- tenantId：租户ID
- queryVO：班次详细查询对象

**返回值**：List<MtCalendarShiftVO1> - 班次详细信息列表

### 13. calendarLimitOrgCalendarQuery

**用途**：查询组织日历

**参数**：
- tenantId：租户ID
- queryVO：组织日历查询对象

**返回值**：List<MtCalendarOrgRelVO1> - 组织日历列表

## 使用示例

### 示例1：批量获取日历基本信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarBaseVO;

List<Long> calendarIds = Arrays.asList(1L, 2L, 3L);
List<MtCalendarBaseVO> calendars = mtCalendarRpcClient.calendarBasicPropertyBatchGet(tenantId, calendarIds);
Map<Long, String> calendarCodeMap = calendars.stream()
    .collect(Collectors.toMap(MtCalendarBaseVO::getCalendarId, MtCalendarBaseVO::getCalendarCode));
```

### 示例2：根据编码批量查询日历基本信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarBaseVO;

List<String> calendarCodes = Arrays.asList("CAL001", "CAL002", "CAL003");
List<MtCalendarBaseVO> calendars = mtCalendarRpcClient.codeLimitCalendarBasicBatchQuery(tenantId, calendarCodes);
Map<String, Long> calendarIdMap = calendars.stream()
    .collect(Collectors.toMap(MtCalendarBaseVO::getCalendarCode, MtCalendarBaseVO::getCalendarId));
```

### 示例3：批量获取班次基本信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarShiftBaseVO;

List<Long> shiftIds = Arrays.asList(1L, 2L, 3L);
List<MtCalendarShiftBaseVO> shifts = mtCalendarRpcClient.calendarShiftPropertyBatchGet(tenantId, shiftIds);
Map<Long, String> shiftCodeMap = shifts.stream()
    .collect(Collectors.toMap(MtCalendarShiftBaseVO::getShiftId, MtCalendarShiftBaseVO::getShiftCode));
```

### 示例4：查询班次工作日信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarShiftWorkDayVO;

MtCalendarShiftWorkDayQueryVO queryVO = new MtCalendarShiftWorkDayQueryVO();
queryVO.setShiftId(shiftId);
queryVO.setWorkDate(workDate);
MtCalendarShiftWorkDayVO workDay = mtCalendarRpcClient.calendarShiftWorkDayQuery(tenantId, queryVO);
```

### 示例5：查询组织日历

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarOrgRelVO1;

MtCalendarOrgRelVO1 queryVO = new MtCalendarOrgRelVO1();
queryVO.setOrganizationId(organizationId);
queryVO.setCalendarType("WORK");
List<MtCalendarOrgRelVO1> orgCalendars = mtCalendarRpcClient.calendarLimitOrgCalendarQuery(tenantId, queryVO);
```

### 示例6：查询班次详细信息

```java
import org.tarzan.boot.model.client.MtCalendarRpcClient;
import org.tarzan.model.domain.vo.MtCalendarShiftVO1;

MtCalendarShiftVO1 queryVO = new MtCalendarShiftVO1();
queryVO.setShiftId(shiftId);
queryVO.setQueryType("DETAIL");
List<MtCalendarShiftVO1> shiftDetails = mtCalendarRpcClient.calendarLimitShiftDetailQuery(tenantId, queryVO);
```

## 注意事项

1. 所有方法都需要传入租户ID（tenantId）作为参数
2. 批量查询方法的性能优于单个查询方法，建议优先使用批量查询方法
3. 班次工作日查询需要提供班次ID和工作日期参数
4. 组织日历查询需要正确设置组织ID和日历类型
5. 不同方法返回的对象类型不同，使用时需要注意类型转换
6. 部分方法支持可选的fields参数，可以指定要查询的字段，减少数据传输量
7. 日历查询时需要注意时间格式的正确性