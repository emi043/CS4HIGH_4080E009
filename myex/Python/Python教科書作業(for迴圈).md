
# Ch17 for迴圈:

## 程式17.1用for連續列印10次
```
for i in range(10):
  print("Hello Python")
  
  答案:
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
        Hello Python
```
## 程式17.2用for依序顯示數列元素
```
for i in range(3):
  print("var i is",i)
  
  答案:
        var i is 0
        var i is 1
        var i is 2
```
## 觀念驗證17.1  下列程式碼顯示答案為
```
list1 = range(1)
print(list(list1))

list2 = range(5)
print(list(list2))

list3 = range(100)
print(list(list3))
  
  答案:
        [0]
        
        [0, 1, 2, 3, 4]
        
        [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 
        29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55,
        56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 
        83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]
```
## 程式17.3不同數列範圍
```

for i in range(10,1,-1):
  print( i,end=" " )
print()
for i in range(0,9,2):
  print( i,end=" " )
  
  答案:
      10 9 8 7 6 5 4 3 2 
      0 2 4 6 8 
```
## 觀念驗證17.2  用for顯示下列range函式
```
list1=range(0,9)
list2=range(3,8)
list3=range(-2,3,2)
list4=range(5,-5,-3)
list5=range(4,1,2)

print(list(list1))
print(list(list2))
print(list(list3)) 
print(list(list4))   
print(list(list5))   
  
  答案:  
        [0, 1, 2, 3, 4, 5, 6, 7, 8]
        [3, 4, 5, 6, 7]
        [-2, 0, 2]
        [5, 2, -1, -4]
        []
```
## 程式17.4 九九乘法表
```
for i in range(1,10):
  for j in range(1,10):
    print( j, "x", i, "=", j*i, end=' ' )
  print()

  答案:       
  1 x 1 = 1   2 x 1 = 2   3 x 1 = 3   4 x 1 = 4   5 x 1 = 5   6 x 1 = 6   7 x 1 = 7   8 x 1 = 8   9 x 1 = 9 
  1 x 2 = 2   2 x 2 = 4   3 x 2 = 6   4 x 2 = 8   5 x 2 = 10  6 x 2 = 12  7 x 2 = 14  8 x 2 = 16  9 x 2 = 18 
  1 x 3 = 3   2 x 3 = 6   3 x 3 = 9   4 x 3 = 12  5 x 3 = 15  6 x 3 = 18  7 x 3 = 21  8 x 3 = 24  9 x 3 = 27 
  1 x 4 = 4   2 x 4 = 8   3 x 4 = 12  4 x 4 = 16  5 x 4 = 20  6 x 4 = 24  7 x 4 = 28  8 x 4 = 32  9 x 4 = 36 
  1 x 5 = 5   2 x 5 = 10  3 x 5 = 15  4 x 5 = 20  5 x 5 = 25  6 x 5 = 30  7 x 5 = 35  8 x 5 = 40  9 x 5 = 45 
  1 x 6 = 6   2 x 6 = 12  3 x 6 = 18  4 x 6 = 24  5 x 6 = 30  6 x 6 = 36  7 x 6 = 42  8 x 6 = 48  9 x 6 = 54 
  1 x 7 = 7   2 x 7 = 14  3 x 7 = 21  4 x 7 = 28  5 x 7 = 35  6 x 7 = 42  7 x 7 = 49  8 x 7 = 56  9 x 7 = 63 
  1 x 8 = 8   2 x 8 = 16  3 x 8 = 24  4 x 8 = 32  5 x 8 = 40  6 x 8 = 48  7 x 8 = 56  8 x 8 = 64  9 x 8 = 72 
  1 x 9 = 9   2 x 9 = 18  3 x 9 = 27  4 x 9 = 36  5 x 9 = 45  6 x 9 = 54  7 x 9 = 63  8 x 9 = 72  9 x 9 = 81 
```
## 觀念驗證17.3  倒數計時
```
reciprocal= int(input("輸入倒數分鐘數: "))
s=reciprocal%60
m=reciprocal//60
for i in range(m,-1,-1):
  for j in range(s,-1,-1):
      print(i, ":",j )
      s=59
  
  答案:
          輸入倒數分鐘數: 65
          1 : 5
          1 : 4
          1 : 3
          1 : 2
          1 : 1
          1 : 0
          0 : 59
          0 : 58
          0 : 57
          0 : 56
          0 : 55
          0 : 54
          0 : 53
          0 : 52
          0 : 51
          0 : 50
          0 : 49
          0 : 48
          0 : 47
          0 : 46
          0 : 45
          0 : 44
          0 : 43
          0 : 42
          0 : 41
          0 : 40
          0 : 39
          0 : 38
          0 : 37
          0 : 36
          0 : 35
          0 : 34
          0 : 33
          0 : 32
          0 : 31
          0 : 30
          0 : 29
          0 : 28
          0 : 27
          0 : 26
          0 : 25
          0 : 24
          0 : 23
          0 : 22
          0 : 21
          0 : 20
          0 : 19
          0 : 18
          0 : 17
          0 : 16
          0 : 15
          0 : 14
          0 : 13
          0 : 12
          0 : 11
          0 : 10
          0 : 9
          0 : 8
          0 : 7
          0 : 6
          0 : 5
          0 : 4
          0 : 3
          0 : 2
          0 : 1
          0 : 0
```
## 程式17.5 使用continue跳過5不印222222222222
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
while start == "y":
    guess= int(input("猜一個數字(1-10): "))
    while guess != lucky_num:
      if guess >= 11:
        print("超過範圍")
      guess= int(input("再猜: "))
    print("你猜中了")
    start= input("是否進行遊戲(y=yes,n=no): ")
    continue
if start == "n":
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
        再猜: 3
        再猜: 5
        你猜中了
        是否進行遊戲(y=yes,n=no): y
        猜一個數字(1-10): 12
        超過範圍
        再猜: 3
        再猜: 5
        你猜中了
        是否進行遊戲(y=yes,n=no): n
        退出遊戲
```
