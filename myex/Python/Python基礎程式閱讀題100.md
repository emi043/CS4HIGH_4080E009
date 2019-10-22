# 數值計算
```
底下程式執行後, z之值為何?
x = 3
y = 5
z = (x + y) / 2
```

```
底下程式執行後, 其值為何?
3 / 2
3 // 2
-1 // 2

51 + 122 - 33*42-(44*3)/5
3000000000*3.0
3000000000*3

int(200.2)
int(2e2)
float(200)
```

### 複數運算
```
3 + 2j - (4 + 4j)
1j*1j
(1 + 2j) * (3 + 4j)

z = 3+5j
z.real
z.imag


import cmath
cmath.sqrt(-1)
```


# 字串

```
1.print("3*2*(17-2)")會印出甚麼結果:
(A)0   (B)90  (C)出現錯誤,無法印出  (D)3*2*(17-2)

2.print(3*2*(17-2))會印出甚麼結果:
(A)0   (B)90  (C)出現錯誤,無法印出  (D)3*2*(17-2)

3.print("abc""+""def")會印出甚麼結果:
(A)出現錯誤,無法印出   (B)abc+def  (C)abc""+""def  (D)abcdef

4.print("abc"+"def")會印出甚麼結果:
(A)出現錯誤,無法印出   (B)abc+def  (C)abc""+""def  (D)abcdef

5.底下程式執行後結果為何?
word = "arttarataaa"
print(word.replace("a", "z",3))
(A)出現錯誤,無法印出   (B)arttarataaa  (C)zrttzrztaaa (D)zrttzrztzzz

6.底下程式執行後結果為何?
word = "arttarataaa"
print(word.replace("a", "z"))
(A)出現錯誤,無法印出   (B)arttarataaa  (C)zrttzrztaaa (D)zrttzrztzzz

7.底下各行輸出為何?
sentence = 'To Be or NOT to Be: that is the question: '
print(sentence.upper())
print(sentence.lower())
print(sentence.capitalize())
print(sentence.count('o'))
```

```
底下各行輸出為何?
x = "Hello"
x[0]
x[5]
x[-1]
x[1:]
x[1:-1]
```
```
底下輸出為何?
x = "Goodbye\n"
x = x[:-1]
x
```
```
len("Goodbye")
```
### 基本的字串操作
```
x = "Hello " + "Mydeargreatteacher"
x
```
```
8 * "x"
```
### Unicode轉義字元
```
unicode_a ='\N{LATIN SMALL LETTER A}'
unicode_a
```
```
unicode_a_with_acute = '\N{LATIN SMALL LETTER A WITH ACUTE}'      
unicode_a_with_acute
```
```
"\u00E1"
```
### 字串處理常用的method(方法)
```
# 使用join()連接字串
"".join(["Separated", "by", "nothing"])

" ".join(["join", "puts", "spaces", "between", "elements"])

"::".join(["Separated", "with", "colons"])
```
```
# 使用split()切割字串
x = "You\t\t can have tabs\t\n \t and newlines \n\n mixed in"
x.split()

x = "Mississippi"
x.split("ss")

x = 'a b c d'
x.split(' ', 1)

['a', 'b c d']
x.split(' ', 2)

['a', 'b', 'c d']
x.split(' ', 9)
```
```
# 使用strip(()、lstrip()、rstrip()去除多餘空白

底下程式執行後各行結果為何?
x = "  Hello,    World\t\t "
x.strip()
x.lstrip()
x.rstrip()


底下程式執行後各行結果為何?
x = "www.python.org"
x.strip("w")  
x.strip("gor")       
x.strip(".gorw")  
```
```
底下程式執行後各行結果為何?
x = "123"
x.isdigit()
x.isalpha()

底下程式執行後各行結果為何?
x = "M"
x.islower()
x.isupper()
```
```
# 使用內建函數:用int() 和float()函示將字串轉換為數字

下列程式執行後結果為何?何者有誤?
float('123.456')
float('xxyy') 

int('3333')
int('123.456') 
int('10000', 8)             
int('101', 2)
int('ff', 16)
int('123456', 6)   
```
### while loop
```
7根據底下程式,下列敘述何者為非?[複選題]

names = ['龍', '聖']
index = 0

while index < len(names):
    name = names[index]
    print(name)
    index = index + 1
    
(A)len(names)=2  
(B)names[1]是 龍 
(C)程式執行完後,index最後為2
(D)如果把條件改成 index > len(names),中index最後為2
```
