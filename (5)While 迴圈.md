```
i=1
while i < 3:
  print(i)
i+=1

print("abc")
問題：while迴圈的執行範圍為何？何時跳回重覆? 注意避免"無窮迴圈"的產生
```

```
#for迴圈

for 變數 in 序列項目：
  執行敘述
  
range(起始值,終止值,增減值)
例2

for x in range(1,10):
  print ("x")
```
```
#巢狀迴圈

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
```
