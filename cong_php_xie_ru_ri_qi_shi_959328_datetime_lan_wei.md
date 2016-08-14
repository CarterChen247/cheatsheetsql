# 處理SQL日期時間(DATETIME)欄位


```bash
#相關詞
#php, #sql, #datetime
```


---


##問題概述
透過php將時間寫入myTable資料表欄位
輸入的資料必須遵循MySQL的欄位格式  
MySQL的DATETIME格式為**yyyy-mm-dd hh:mm:ss**


表1：myTable
![](origin_php_datetime.png)


表2：結果
![](result_php_datetime.png)


---


  
##php語法

```php
$time = date("Y-m-d H:i:s"); //取得目前的時間，並轉為yyyy-mm-dd hh:mm:ss格式

/*接下來使用PDO寫入資料庫(略)*/
```



---

##延伸範例
可以在取得時間前，可以事先設定時區：
```php
date_default_timezone_set('Asia/Taipei');//將時區設為台北標準時間
$time = date("Y-m-d H:i:s"); 

/*接下來使用PDO寫入資料庫(略)*/
```
透過strtotime()函式可以將時間轉為數字，並加以計算：
```php
$elapsed_time = strtotime($time2) - strtotime($time1);
//$elapsed_time將得到秒數，除以60便是分，再除以60便是時

```
 