# 如果資料不存在，才新增（存在就更新）

```bash
#相關詞
#IF NOT EXIST, #INSERT, #UPDATE
```


---


##問題概述
先找找看資料表中有沒有這筆資料，不然就新增；但如果存在的話，就更新!
通常用於一次更動多筆資料的時機



---


  
##Query語法

```sql
INSERT INTO
  user(name, phone)
VALUES
  (`Adam`, `1234567890`)
ON DUPLICATE KEY UPDATE
  phone = `1234567890`
```



---

##範例解析
這真的沒什麼好說的XDDDD  
就直接給他`ON DUPLICATE KEY UPDATE`下去XDDDDD
