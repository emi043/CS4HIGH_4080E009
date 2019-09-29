# 學習重點
```
1.使用range 函式 的功能建立整數循序數列
2.使用for 廻圈 執行固定次數的廻圈運算(通常)
3.使用while 廻圈執行沒有固定次數的廻圈運算
4.使用continue 指令--- 通常也是用於廻圈中，是在廻圈執行中途暫時停住不往下執行，而跳到廻圈的起始處執行
5.使用break 指令 通常用於廻圈中，可以在廻圈執行中途強迫跳離廻圈，跳到廻圈後面的程式繼續執行。
6.廻圈中又包含廻圈的 巢狀廻圈(nested loop)設計===九九乘法表
```
# Ch16 while迴圈:

## 程式16.1指定訊息顯示內容和次數
```
s = input("請輸入顯示內容: ")
n = int(input("請輸入顯示次數: "))
while(n > 0):
  print(s)
  n=n-1
  
  答案:
        請輸入顯示內容: 嗨!
        請輸入顯示次數: 5
        嗨!
        嗨!
        嗨!
        嗨!
        嗨!
```
## 觀念驗證16.1  顯示n值的變化
```
s = input("請輸入顯示內容: ")
n = int(input("請輸入顯示次數: "))
while(n > 0):
  print(n,s)
  n=n-1
  
  答案:
        請輸入顯示內容: 你好!
        請輸入顯示次數: 6
        6 你好!
        5 你好!
        4 你好!
        3 你好!
        2 你好!
        1 你好!
```
## 程式16.2猜數字
```
lucky_num=77
guess= int(input("猜一個數字(0-99): "))
tries=1
while guess != lucky_num:
      print("您猜測第",tries,"次")
      guess= int(input("再猜: "))
      tries+=1
print("你猜中了")
  
  答案:
          猜一個數字(0-99): 6
          您猜測第 1 次
          再猜: 12
          您猜測第 2 次
          再猜: 89
          您猜測第 3 次
          再猜: 44
          您猜測第 4 次
          再猜: 77
          你猜中了
```
## 觀念驗證16.2  改寫While內3行程式
```
lucky_num=77
guess= int(input("猜一個數字(0-99): "))
tries=1
while guess != lucky_num:
      tries+=1
      print("您猜測第",tries,"次")
      guess= int(input("再猜: "))
print("你猜中了")
  
  答案:   會先次數加一才會顯示猜測第幾次，故不會有猜測第一次
        猜一個數字(0-99): 66
        您猜測第 2 次
        再猜: 17
        您猜測第 3 次
        再猜: 33
        您猜測第 4 次
        再猜: 77
        你猜中了
```
## 程式16.3 使用break跳離迴圈(猜字5次自動跳出迴圈)
```
secret="code"
max_tries=5
guess= input("猜词: ")
tries=1
while guess != secret:
      print("您猜測第",tries,"次")
      if tries == max_tries:
        print("沒有機會了。")
        break
      guess= input("再猜:  ")
      tries+=1
if tries <= max_tries and guess == secret:
      print("你猜中了")
  
  答案:      猜词: 嗨
            您猜測第 1 次
            再猜:  好
            您猜測第 2 次
            再猜:  a
            您猜測第 3 次
            再猜:  s
            您猜測第 4 次
            再猜:  e
            您猜測第 5 次
            您沒有嘗試。
```
## 觀念驗證16.3  不限次數猜單字
```
secret="code"
max_tries="EXIT"
guess= input("猜词: ")
tries=1
while guess != secret:
      print("您猜測第",tries,"次")
      if guess == max_tries:
        print("結束")
        break
      guess= input("再猜:  ")
      tries+=1
if guess != max_tries and guess == secret:
      print("你猜中了")
  
  答案:
          猜词: a
          您猜測第 1 次
          再猜:  s
          您猜測第 2 次
          再猜:  EXIT
          您猜測第 3 次
          結束
  另一種答案:
          猜词: a
          您猜測第 1 次
          再猜:  s
          您猜測第 2 次
          再猜:  d
          您猜測第 3 次
          再猜:  code
          你猜中了
```
## 程式16.4 使用continue跳過5不印
```
i=1
while (i<10):
      if (i ==5):
        i+=1
        continue
      print(i, end=' ')
      i+=1
print("End")
  
  答案:
        1 2 3 4 6 7 8 9 End
```
## 觀念驗證16.4  刪除if後的i+=1
```
i=1
while (i<10):
      if (i ==5):
        continue
      print(i, end=' ')
      i+=1
print("End")
  
  答案:   會卡在4後無法執行，因為i一直等於5
          1 2 3 4 
```
## 程式16.5 輸入通關密語
```
s=""
while s != "喵喵":
      if (s != ""):
        print("不對喔!")
      s= input("請輸入通關密語:")
      if s== "out":
        break
else:
      print("恭喜你過關了")
print("再見!")
  
  答案:
          請輸入通關密語:2
          不對喔!
          請輸入通關密語:喵喵
          恭喜你過關了
          再見!
  另一種答案:
          請輸入通關密語:z
          不對喔!
          請輸入通關密語:out
          再見!
```
## Ch16習題1 修改程式
```
num=8
guess= int(input("猜一個數字: "))
while guess != num:
      guess= input("再猜: ")
print("猜中")

執行結果:
        猜一個數字: 5
        再猜: 8
        再猜: 1
        再猜: 

  
  答案:   修改處為:  guess= input("再猜: ")=guess= int(input("再猜: "))
          因為再次輸入時為字串並不是數字因此無法跳出迴圈
          num=8
          guess= int(input("猜一個數字: "))
          while guess != num:
                guess= int(input("再猜: "))
          print("猜中")
  執行結果:
          猜一個數字: 1
          再猜: 5
          再猜: 8
          猜中
```
## Ch16習題2 寫猜數字遊戲
```
lucky_num=5
start= input("是否進行遊戲(y=yes,n=no): ")
if start == "y":
    guess= int(input("猜一個數字(1-10): "))
    while guess != lucky_num:
      if guess >= 11:
        print("超過範圍")
      guess= int(input("再猜: "))
    print("你猜中了")
    
elif start == "n":
   print("退出遊戲")
else:
  print("輸入錯誤")

  
  答案1:  是否進行遊戲(y=yes,n=no): n
          退出遊戲
  答案2:
         是否進行遊戲(y=yes,n=no): q
         輸入錯誤
  答案3:
         是否進行遊戲(y=yes,n=no): y
         猜一個數字(1-10): 12
         超過範圍
         再猜: 6
         再猜: 4
         再猜: 5
         你猜中了
```
