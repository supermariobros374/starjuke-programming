# Python基本語法整理
> **這是極淺而廣的Python教學筆記**

###動態語言
> 指執行時可以改變其結構的語言
> 如變數參照型態的改變，函式、物件

### 直譯語言
> 編譯語言：寫完全部一次編譯給電腦執行
> 直譯語言：執行時一行行轉為機器碼

### python版本
> python2 和 python3有本質上的差異
> 不過許多套件都是以2版寫成，建議先學2版
> 且先學2版在學3版也不難轉換

### 安裝python
 * 先到官網下載并安裝
 * python預設被裝在 C:\Python版本 這個資料夾(如C:\Python27)
 * 將下列兩個路徑加入環境變數（以自己版本號套入）
 	1. C:\Python版本
 	2. C:\Python版本\Scripts
 * 進入cmd 輸入 `python --version`確認安裝

### python shell & python文件
 * 在terminal中(如cmd)鍵入 `python` 進入python shell
 * [https://docs.python.org/2/](https://docs.python.org/2/)  python完整文件

### 變數命名規則
 1. 以底線或英文字母開頭
 2. 名稱只可含以底線,英文字母和數字
 3. 不可與關鍵字相同
 4. 區分大小寫

### 變數參照
```python
>>> result = 2
```
> 以上是一個變數宣告或指定
> 事實上result沒有直接記錄 2
> 而是記錄了儲存 2 的空間
> 所以是可以轉換儲存形態的(轉換記錄空間)
> ```python
> >>> result = 2
> >>> result = 3.0
> >>> result = 'hello'
> >>> result = [1,2,3]
> ```
> 就像一個容器的***標籤***一樣

### 撰寫一個腳本
 * 通常以.py結尾
 * 以下是簡單的python程式碼(test.py)
```python
a = 10
b = 20
result = a + b
print result # result是20
```
 * `print`是印出資料， `#`後面代表的是註解
 * 接著只要在terminal中執行腳本
   而test.py是檔案名
   
```
python test.py
20
```

### 函式
> 就是封裝一套動作，供使用者**重複執行***
> * 使用函式 ```函式名(參數1,參數2,...)```
>   參數有幾個端看參數設計幾個參數給使用者使用
> * 不論有沒有設計參數，**小括號**都必須存在
> * 以下是使用函式的範例
> ```python
> print avg(1,2,3,4,5) #avg是內建的平均函式
> print abs(-10) #abs是內建的絕對值函式
> ```

### 資料型態
* 以下是整數運算的例子
```python
>>> 2 - 3
-1
>>> 2 * 3
6
>>> 6 / 4
1
>>> 6 % 4 #取餘數
2
>>> 2 ** 6 #次方
64
```

* 以下是浮點數運算的例子
```python
>>> 1.2 + 2
3.2
>>> 1.2e2 - 10 #1.2e2 即科學記號表示法表示120
110.0
>>> 3.2 / 1.1
2.909090909090909
>>> 4.2 % 3.2
1.0
```
* 布林數
> 只有真假值之分，如`false`,`true`

* 以下是字串的例子
```python
>>> string = ''
>>> string_a = 'h'
>>> string_b = 'ello'
>>> string_a + string_b
'hello'
```
字串不論使用 " 還是 ' 都可以
> * 還有特別的 文件字串可以保留格式，以一對 """
> ```python
> string_e = """
>     today is
>     a good day!
> """
> print string_e
> ```
> * 取出特定部分字串使用 [ ]
> ```python
> string = "hello world"
> print string[0] # 即第 0 個元素
> print string[0:5] # 即第 0 個到第 6 個元素
> ```
> **在電腦的世界中一切都是0開始**
>   而 上面的 0 即是 索引(index)
>   上面的 0:5 即是 切片(slicing)
>   
> * 指定切片時捨棄範圍
> ```python
> print string[:5] # 即第 0 個到第 5 個元素
> print string[6:] # 即第 6 個到最後一個
> print string[:] # 即全部
> ```
> * 填充字串，使用`format`方法以位置填充
> ```python
> string = 'My name is {0}, and i'm {1} years old'.format('Leo','10')
> ```
> * 以代名填充
> ```python
> string = 'Time is {time}'.format(time = '21:13')
> ```

* 跳脫字元
```python
>>> print '\thello world'
		hello world
>>> print 'hello\nworld'
hello
world
```
> 以下是一些跳脫字元
> |跳脫字元|說明|
> |:-:|-|
> |\\|倒斜線|
> |\'|單引號|
> |\"|雙引號|
> |\n|換行|
> |\t|縮排|

* 使檔案支援中文
  在第一行加入 
  ```python
  # -*- coding: utf-8 -*-` 
  ```
