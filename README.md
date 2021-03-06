# city-timezone

word city timezone data 世界主要城市时区信息

### 文件说明

- timezone.csv 为csv文件方便导入数据库
- timezone.json 为json格式的timezone数据

### 数据来源

- 城市数据来源于网上爬取的城市三字码
- timezone数据来源于百度api http://mvideo.baidu.com/index.php?title=webapi/guide/timezone

### 两种使用方式
- 直接拷贝文件timezone.json或者timezone.csv 导入数据库
- 使用npm install city-timezone
```javascript
    var timezone = require("city-timezone");
    //第一个参数为日期字符串，第二个为城市三字码
    var d = timezone.getTimezoneDate("2016-12-12 12:00:00", "BJS");
```
### 测试

```
    mocha

      timezone
        ✓ #getTimezoneDate with citycode=BJS (北京) should be ok
        ✓ #getTimezoneDate with citycode=LHR (伦敦) should be ok
        ✓ #getTimezoneDate with citycode=JFK (纽约) should be ok


      3 passing (12ms)

```

### 后续

现在数据大概有1400多条，欢迎您能反应问题或者pull request来完善信息
