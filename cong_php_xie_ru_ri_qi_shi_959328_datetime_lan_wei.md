# 處理SQL日期時間(DATETIME)欄位


```bash
#相關詞
#php, #sql, #datetime
```


---


##問題概述
透過php將時間寫入資料表欄位中  
MySQL的DATETIME格式為**yyyy-mm-dd hh:mm:ss**


表1：myTable
![](origin_php_datetime.png)


表2：結果
![](result_php_datetime.png)


---


  
##php語法

```php
$time = date("Y-m-d H:i:s");

/*接下來使用PDO寫入資料庫(略)*/
```



---

##範例解析
