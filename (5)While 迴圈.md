
 # 何時會用到迴圈?
```
印出下列圖形
$$$$$$$$$$$
$$$$$$$$$$$
$$$$$$$$$$$

print("$$$$$$$$$$$")
print("$$$$$$$$$$$")
print("$$$$$$$$$$$")

如果印100行呢?
for x in range(1,101):
  print(str(x)+"$$$$$$$$$$$")
```
  
 # While 迴圈
 ```
while 條件判斷式:
#如果條件判斷式成立，就執行這裡面的敘述

i=1
while i < 3:
  print(i)
i+=1

print("abc")
問題：while迴圈的執行範圍為何？何時跳回重覆? 注意避免"無窮迴圈"的產生
```


# for迴圈
```
for 變數 in 序列項目：
  執行敘述
  
range(起始值,終止值,增減值)
例2

for x in range(1,10):
  print ("x")
 # 練習1
 如何讓上下都有1-10???
           
for x in range(1,10):
  print("")
 
``` 

# 巢狀迴圈
```
k =1
h = 1
while k <6 :
  while h < 6:
    print (k,end=(''))
    h+=1
  k+=1
  h =1
  print()
 問: 為甚魔少H不能有12345,而有H卻可一???
 A:因為上面一迴圈6次當H出現他就成為1次而已
```
 # 小題目
```
EX1: 
**********
**********
**********
**********
**********
**********
**********
**********
**********
**********
答案
for x in range(1,11):
  print("**********")

EX2:
*
**
***
****
*****
******
*******
********
答案:
for x in range(1,10):
  for y in range(10,1,-1):
    print("",end="")
  for z in range(1,x):
    print("*",end="")
  print("")

EX3:
*
**
***
****
*****
*****
****
***
**
*
答案

Ex4
         *
        **
       ***
      ****
     *****
    ******
   *******
  ********
 *********
**********
答案
for x in range(1,10):
  for y in range(9,x,-1):
    print(" ",end="")
  for z in range(0,x):
    print("*",end="")
  print("")
```

# 聖誕樹
```
for x in range(1,20,2):
  for y in range(19,x,-2):
    print(" ",end="")
  for z in range(0,x):
    print("*",end="")
  print("")

for k in range(1,5):
  print("       ",end="")
  for h in range(1,6):
    print("*",end="")
  print("")
  
  ###
  不同樹
  for x in range(1,20,2):
  for y in range(19,x,-2):
    print(" ",end="")
  for z in range(0,x):
    print("*",end="")
  print("")

for k in range(1,5):
  print("       ",end="")
  for h in range(1,6):
    print("*",end="")
  print("")
for l in range(1,5):
    print("     *********",end="")
    print(""
```
