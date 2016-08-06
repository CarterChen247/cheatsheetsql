# 行列轉換
```bash
相關詞
#pivot, #row to column
```


---


##問題概述
將一列一列的資料轉換成以欄位顯示的表格(表1→表2)


表1：myTable
>![](origin_pivot.png)

表2：結果
>![](result_pivot.png)


---


  
##Query語法

```sql
SELECT 
  MAX(IF(pid=1, order, 0)) ApplePie,
  MAX(IF(pid=2, order, 0)) Biscuit,
  MAX(IF(pid=2, order, 0)) Cake,
  MAX(IF(pid=2, order, 0)) Donut,
FROM
  myTable
```



---

##範例解析
```sql
MAX(IF(pid=1, order, 0)) ApplePie,
```
表示當pid中的值=1時，在ApplePie(自定義)欄位中填入order欄位中的資料。