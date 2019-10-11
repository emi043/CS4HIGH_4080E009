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
## Ch18習題1 輸入名字程式針對名字加Hi
```
a=0
for i in range(3, 100,3):
      a+=1    
      print(i)
print("3的倍數總共有:",a,"個")
  
   答案:  3
          6
          9
          12
          15
          18
          21
          24
          27
          30
          33
          36
          39
          42
          45
          48
          51
          54
          57
          60
          63
          66
          69
          72
          75
          78
          81
          84
          87
          90
          93
          96
          99
          3的倍數總共有: 33 個
```
## Ch17習題2 寫出可產生任意層數三角形
```
s= int(input("請指定三角形層數: "))
for i in range(s):
  for j in range(s - i - 1): 
           print(" ", end = "")
  for k in range(i + 1):                
          print("* ", end = "" )
  print()    

  
  答案1:  請指定三角形層數: 7
              * 
             * * 
            * * * 
           * * * * 
          * * * * * 
         * * * * * * 
        * * * * * * * 
```
