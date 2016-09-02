# 如果資料不存在，才新增（存在就略過）

```bash
#相關詞
#IF NOT EXIST, #INSERT
```


---


##問題概述
先找找看資料表中有沒有這筆資料，不然就新增(新增表1到myTable資料表)
適用於調查使用者喜好更改的時機


表1：
![](origin_adam_cake_c.png)





---


  
##Query語法

```sql
INSERT INTO
  myTable(user, product)
SELECT
  *
FROM
  (SELECT user, product) AS tmp
WHERE NOT EXISTS
  (SELECT
    user
  FROM
    myTable
  WHERE
	user = 'Adam')
LIMIT
  1";
```



---

##範例解析
這是INSERT INTO和SELECT的合體用法喔
