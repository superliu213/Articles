## java.util.Calendar
- 用于日期和时间的运算  
- 抽象类，不能实例化
- 瞬间可用毫秒值来表示，它是距历元（即格林威治标准时间 1970年1月1日的00:00:00.000，格里高利历）的偏移量
```java
Calendar rightNow = Calendar.getInstance();
```

## java.util.GregorianCalendar
- GregorianCalendar(格利高里日期) 是 Calendar 的一个具体子类，提供了世界上大多数国家/地区使用的标准日历系统

## 实例化GregorianCalendar
```java
Calendar calendar = new GregorianCalendar();
```

## 获取年、月、日等
```java
Calendar calendar = new GregorianCalendar();

int year       = calendar.get(Calendar.YEAR);
int month      = calendar.get(Calendar.MONTH);
int dayOfMonth = calendar.get(Calendar.DAY_OF_MONTH); // Jan = 0, not 1
int dayOfWeek  = calendar.get(Calendar.DAY_OF_WEEK);
int weekOfYear = calendar.get(Calendar.WEEK_OF_YEAR);
int weekOfMonth= calendar.get(Calendar.WEEK_OF_MONTH);

int hour       = calendar.get(Calendar.HOUR);        // 12 hour clock
int hourOfDay  = calendar.get(Calendar.HOUR_OF_DAY); // 24 hour clock
int minute     = calendar.get(Calendar.MINUTE);
int second     = calendar.get(Calendar.SECOND);
int millisecond= calendar.get(Calendar.MILLISECOND);
```

## 设置年、月、日
```java
Calendar calendar = new GregorianCalendar();

calendar.set(Calendar.YEAR, 2009);
calendar.set(Calendar.MONTH, 11); // 11 = december
calendar.set(Calendar.DAY_OF_MONTH, 24); // christmas eve
```

## 添加和减少年、月、日等
```java
Calendar calendar = new GregorianCalendar();

//set date to last day of 2009
calendar.set(Calendar.YEAR, 2009);
calendar.set(Calendar.MONTH, 11); // 11 = december
calendar.set(Calendar.DAY_OF_MONTH, 31); // new years eve

//add one day
calendar.add(Calendar.DAY_OF_MONTH, 1);

//date is now jan. 1st 2010
int year       = calendar.get(Calendar.YEAR);  // now 2010
int month      = calendar.get(Calendar.MONTH); // now 0 (Jan = 0)
int dayOfMonth = calendar.get(Calendar.DAY_OF_MONTH); // now 1

calendar.add(Calendar.DAY_OF_MONTH, -1);
```
## 陷阱和误区
### 月份陷阱
- 月份从0到11

### 星期误区
- 1 = sunday, 2 = monday, …, 7 = Saturday

#### 参考资料
- http://ifeve.com/java-util-calendar/
- http://baike.baidu.com/item/GregorianCalendar
