# 如果資料不存在，才更新

```bash
#相關詞
#IF NOT EXIST, #UPDATE
```


---


##問題概述
查詢想要變更的資料是否已經存在，如果已經存在就不更新了  
通常用於使用者想更改具有唯一性的東西時，  
例如：身分證字號、手機、電子郵件等等





---


  
##Query語法

```sql
UPDATE
  myTable
SET
  email = `adam@c8763.com`
WHERE
  name = `Adam`
AND NOT EXISTS
  (SELECT
    *
   FROM
     (SELECT
       1
     FROM
       myTable
     WHERE
       email = `adam@c8763.com`) temp)
```



---

##範例解析
資料表temp中若不到東西的話會返回0行資料  
也滿足了`NOT EXISTS`的條件
只有在這個狀況下才會進行資料更新
