# Ch18 用for迴圈走訪容器中元素:

## 程式18.1  用for迴圈走訪字串中的字元
```
for ch in "Python is fun!":
  print("the character is", ch)
  
  答案:
          the character is P
          the character is y
          the character is t
          the character is h
          the character is o
          the character is n
          the character is  
          the character is i
          the character is s
          the character is  
          the character is f
          the character is u
          the character is n
          the character is !
```
## 觀念驗證18.1  任意輸入字串，用for將(a,e,i,o,u)列印出來
```
string= input("輸入字串: ")
for ch in string :
  if (ch=="a" or ch=="e" or ch=="i" or ch=="o" or ch=="u"):
    print("the character is", ch)
  
  答案:
       輸入字串: Python is fun!
          the character is o
          the character is i
          the character is u
```
## 程式18.2 用for迴圈走訪字串中的索引值(比較程式18.1)
```
my_string= "Python is fun!"
len_s=len(my_string)
for i in range(len_s):
  print("the character is", my_string[i])
  
  答案:
          the character is P
          the character is y
          the character is t
          the character is h
          the character is o
          the character is n
          the character is  
          the character is i
          the character is s
          the character is  
          the character is f
          the character is u
          the character is n
          the character is !
```
## 程式18.3 用for迴圈走訪tuple
```
winners= ("Peter","Mark","Joy")
print("恭喜以下得獎者:")
for name in winners:
  print(name)
  
  答案:  
          恭喜以下得獎者:
          Peter
          Mark
          Joy
```
## 程式18.4 用for迴圈走訪tuple的索引值
```
prizes=("頭獎","二獎","三獎")
winners= ("Peter","Mark","Joy")
print("恭喜以下得獎者:")
for i in range(3):
  print(prizes[i]+ ":" + winners[i])

  答案:       
        恭喜以下得獎者:
        頭獎:Peter
        二獎:Mark
        三獎:Joy
```
## 程式18.5  用for迴圈走訪二層的tuple
```
winners=(("頭獎","Peter"),("二獎","Mark"),("三獎","Joy"))
print("恭喜以下得獎者:")
for e in winners:
  print(e[0]+ ":" + e[1])
  
  答案:
        恭喜以下得獎者:
        頭獎:Peter
        二獎:Mark
        三獎:Joy
```
## 觀念驗證18.2 將分開的姓和名用for迴圈走訪二層的tuple 全名列印出來
```
Name=(("張","天才"),("王","子帥"),("陳","美美"))
for e in Name:
  print(e[0] + e[1]) 
  
  答案:
        張天才
        王子帥
        陳美美
```
## 程式18.6  多變數走訪二層的tuple
```
winners=(("頭獎","Peter"),("二獎","Mark"),("三獎","Joy"))
print("恭喜以下得獎者:")
for prize , winner in winners:
  print(prize+ ":" + winner)
  
  答案:   
        恭喜以下得獎者:
          頭獎:Peter
          二獎:Mark
          三獎:Joy
```
## 觀念驗證18.3 多變數走訪三層的tuple
```
students=(('22',('張','天才')),('23',('王','子帥')),('24',('陳','美美')))
for (Seat, (lastname, firstname)) in students:
    print(Seat+ "號" + " - " + lastname+ firstname)
      
  答案:   
        22號 - 張天才
        23號 - 王子帥
        24號 - 陳美美
```
## 程式18.7 for 迴圈 vs. while 迴圈
```
for x in range(3):
    print("var x is",x)
      
  答案:   
        var x is 0
        var x is 1
        var x is 2
x=0
while x<3:
    print("var x is",x)
    x+=1
      
  答案:   
        var x is 0
        var x is 1
        var x is 2
```
## 觀念驗證18.4  下列 while 迴圈改成for迴圈
```
password = "robot fort flower graph"
space_count = 0
i=0
while i < len(password):
  if password[i] == " ":
      space_count +=1
  i+=1
print(space_count)
      
  答案:   
        3
        
password = "robot fort flower graph"
space_count = 0
len_s=len(password)
for i in range(len_s):
  if password[i] == " ":
      space_count +=1
print(space_count)
答案:   
        3
        
```
## Ch18習題1 輸入多個名字以空白分隔程式針對名字說Hi
```
string= input("輸入名字: ")
for n in string.split():
  print("Hi "+n)
  
   答案: 輸入名字: 張天才 小小 apple Young
          Hi 張天才
          Hi 小小
          Hi apple
          Hi Young
```
## Ch18習題2 用while迴圈輸入購買清單再用for迴圈把購買清單列出
```
commoditys=[]
while True:
  commodity = input("請輸入要買的商品(沒了 = 結束)：")
  if (commodity!="沒了"):
    commoditys.append(commodity)
  if (commodity=="沒了"):
      print("以下是您購買的清單:")
      for n in commoditys:
        print(n)
      break
  
  答案:  請輸入要買的商品(沒了 = 結束)：香蕉
          請輸入要買的商品(沒了 = 結束)：牛奶
          請輸入要買的商品(沒了 = 結束)：衛生紙
          請輸入要買的商品(沒了 = 結束)：牙刷
          請輸入要買的商品(沒了 = 結束)：沒了
            以下是您購買的清單:
            香蕉
            牛奶
            衛生紙
            牙刷
```
## Ch18習題3 用多變數走訪的方式把18到22歲的會員列出來
```
members=(('Jam',16),('Sam',21),('Mark',17),('Ken',24),('Ben',18))
print("會員名單:") 
for Name , age in members:
  if age>17 and age < 23 :
     print("會員:", Name , age , "歲")
  
  答案:  會員名單:
         會員: Sam 21 歲
        會員: Ben 18 歲
```
