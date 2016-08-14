# 更新資料


```bash
#相關詞
#update, #basic, #crud
```


---


##問題概述
修改單一筆資料某欄位中的資料(表1→表2)


表1：myTable
![](origin_update.png)

表2：結果
![](result_update.png)


---


  
##Query語法

```sql
/*單數*/
UPDATE 
  myTable
SET 
  phone = "0940890706"
WHERE
  name = "Nick";

/*複數*/
UPDATE 
  myTable
SET 
  phone = "0940890706", 
  age = "18"
WHERE
  name = "Nick";

```



---

##範例解析
WHERE後面接的是條件，也就是用來描述你想更改的那筆資料的特徵