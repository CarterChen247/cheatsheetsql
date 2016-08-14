# 新增資料

```bash
#相關詞
#insert #basic #crud
```


---


##問題概述
將資料寫入資料表(表1→表2)


表1：myTable
![](origin_insert.png)

表2：結果
![](result_insert.png)


---


  
##Query語法

```sql
/*單數*/
INSERT INTO  
  myTable (name)
VALUES 
  ("Nick");
  
/*複數*/
INSERT INTO  
  myTable (name, age, phone)
VALUES 
  ("Nick", "25", "0910806449");

```



---

##範例解析

只要選定資料表，然後提供相對應的欄位值就好了
