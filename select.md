# 讀取資料


```bash
#相關詞
#select, #basic, #crud
```


---


##問題概述
從資料表中選取資料(表1→表2)


表1：myTable
![](origin_select.png)


表2：結果
![](result_select.png)


---


  
##Query語法

```sql
/*選擇指定欄位*/
SELECT 
  `name`, `age`
FROM
  myTable
  
/*選擇所有欄位*/
SELECT 
  *
FROM
  myTable
```



---

##範例解析

在語法中選擇想要取得資料的欄位就OK囉!