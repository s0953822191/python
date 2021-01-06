# Hello World
以下是一個以 tkinter 建立視窗的 hello world 範例程式：
```
# 引入 tkinter 模組
import tkinter as tk

# 建立主視窗 Frame
window = tk.Tk()

# 設定視窗標題
window.title('Hello World')

# 設定視窗大小為 300x100，視窗（左上角）在螢幕上的座標位置為 (250, 150)
window.geometry("300x100+250+150")

# 執行主程式
window.mainloop()
```
# 加入按鈕（Button）
如果要在 tkinter 的視窗程式中加入按鈕，可以使用 Button 這個元件，以下是使用範例：
```
import tkinter as tk

# 自訂函數
def hello():
    print("Hello, world.")

window = tk.Tk()
window.title('Hello World')
window.geometry("300x100+250+150")

# 建立按鈕
button = tk.Button(window,          # 按鈕所在視窗
                   text = 'Hello',  # 顯示文字
                   command = hello) # 按下按鈕所執行的函數

# 以預設方式排版按鈕
button.pack()

window.mainloop()
```
# 標示文字（Label）
如果要在視窗中加入文字，可以使用 Label 這個元件，以下是使用範例：
```
import tkinter as tk

window = tk.Tk()
window.title('Hello World')
window.geometry("300x100+250+150")

# 標示文字
label = tk.Label(window,                 # 文字標示所在視窗
                 text = 'Hello, world')  # 顯示文字

# 以預設方式排版標示文字
label.pack()

window.mainloop()

如果需要更改文字的字型、大小與顏色等屬性，只要調整對應的參數即可：
import tkinter as tk

window = tk.Tk()
window.title('Hello World')
window.geometry("300x100+250+150")

# 標示文字
label = tk.Label(window,                 # 文字標示所在視窗
                 text = 'Hello, world',  # 顯示文字
                 bg = '#EEBB00',         #  背景顏色
                 font = ('Arial', 12),   # 字型與大小
                 width = 15, height = 2) # 文字標示尺寸   

# 以預設方式排版標示文字
label.pack()

window.mainloop()
```
# 加入輸入欄位（Entry）
若要讓使用者輸入文字資料，可以運用 Entry 元件，以下是使用範例：
```
import tkinter as tk

def onOK():
    # 取得輸入文字
    print("Hello, {}.".format(entry.get()))

window = tk.Tk()
window.title('Hello World')
window.geometry("300x100+250+150")

# 標示文字
label = tk.Label(window, text = '姓名')
label.pack()

# 輸入欄位
entry = tk.Entry(window,     # 輸入欄位所在視窗
                 width = 20) # 輸入欄位的寬度
entry.pack()

# 按鈕
button = tk.Button(window, text = "OK", command = onOK)
button.pack()

window.mainloop()
```
# 跳出訊息視窗
如果希望以跳出的視窗來顯示訊息文字，可以使用 tkinter.messagebox 這個模組，以下是使用範例：
```
import tkinter as tk

# 引入訊息視窗模組
import tkinter.messagebox

def onOK():
    msg = "Hello, {}.".format(entry.get())
    tkinter.messagebox.showinfo(title = 'Hello', # 視窗標題
                                message = msg)   # 訊息內容

window = tk.Tk()
window.title('Hello World')
window.geometry("300x100+250+150")

# 標示文字
label = tk.Label(window, text = '姓名')
label.pack()

# 輸入欄位
entry = tk.Entry(window, width = 20)
entry.pack()

# 按鈕
button = tk.Button(window, text = "OK", command = onOK)
button.pack()

window.mainloop()
```
今天我們學了python他有分兩種1.單一 2.多分解,因為我們要去了解python,我們使用的是第2種,我們上網找python視窗程式設計教學,以上是我們學到的東西,我們還玩了顏色的色碼表#BBFFFF他是淺藍色,我喜歡的顏色!
# 計算器(身高M體重)
```
import tkinter as tk
import math

window = tk.Tk()
window.title('BMI App')
window.geometry('480x360')
window.configure(background='#66FFFF')   #淺色藍

def calculate_bmi_number():
    height = float(height_entry.get())/100     #/=除100,因為他是公尺,需除100
    weight = float(weight_entry.get())
    bmi_value = round(weight / math.pow(height, 2), 2)
    result = '你的 BMI 指數為：{} {}'.format(bmi_value, get_bmi_status_description(bmi_value))
    result_label.configure(text=result)

def get_bmi_status_description(bmi_value):
    if bmi_value < 18.5:
        return '體重過輕囉，多吃點！'
    elif bmi_value >= 18.5 and bmi_value < 24:
        return '體重剛剛好，繼續保持！'
    elif bmi_value >= 24 :
        return '體重有點過重囉，少吃多運動！'

header_label = tk.Label(window, text='BMI 計算器')
header_label.pack()

height_frame = tk.Frame(window)
height_frame.pack(side=tk.TOP)
height_label = tk.Label(height_frame, text='身高（cm）')
height_label.pack(side=tk.LEFT)
height_entry = tk.Entry(height_frame)
height_entry.pack(side=tk.LEFT)

weight_frame = tk.Frame(window)
weight_frame.pack(side=tk.TOP)
weight_label = tk.Label(weight_frame, text='體重（kg）')
weight_label.pack(side=tk.LEFT)
weight_entry = tk.Entry(weight_frame)
weight_entry.pack(side=tk.LEFT)

result_label = tk.Label(window)
result_label.pack()

calculate_btn = tk.Button(window, text='馬上計算', command=calculate_bmi_number)
calculate_btn.pack()

window.mainloop()

我的身高173,體重56,他能計算我們體重是否剛好,還是過重或是過輕,我是剛好耶!!!!!我可以吃從56吃到71重
而#66FFFF他能改變後面的顏色,上面有打說是淺色藍!!!!喜歡~~~~
```
# 包裝
```
左下有一個開始,按右鍵找到職行(R),打上cmd,因為要下在所以打上pip install pyinstaller按Enter,但上面那
些需要下載到桌面，所以先打開Python把上面計算體重的東西複製下來，執行、在建立一個檔案名字隨便，放到桌
上在回去把這個打上pyinstaller -F ./hello.py 進去資料夾裡找上面顯示的檔案biet找,就完成了
```
# 計算機加包裝
```
#!/usr/bin/python 
# coding: utf-8 
# 引入Tkinter庫 
import tkinter as tk
from tkinter import *
# 操作事件繫結的函式，這些函式中都會對顯示的內容進行更新，因此顯示內容display作為全域性變數 
# 更新顯示內容函式，由按鈕事件觸發，將按鈕內容新增到已顯示內容後 

def updateDisplay(buttonString): 
 content = display.get() 
 if content == "0": 
  content = "" 
 display.set(content + buttonString) # 計算表示式的結果，表示式即為顯示的內容，並將結果顯示出來（需要換行並新增等於號） 

def calculate(): 
 result = eval(display.get()) 
 display.set(display.get() + '= ' + str(result)) # 清空操作，由清空按鈕事件觸發 

def clear(): 
 display.set('0') # 刪除操作，由刪除按鈕事件觸發，刪除前一個字元 

def backspace(): 
 display.set(str(display.get()[:-1])) # 定義主視窗，設定視窗名稱和大小200×320，並設定螢幕座標為(300,300) 

mainUI = tk.Tk() 
mainUI.title('Calculator') 
mainUI.geometry('300x270+300+300') # 設定顯示內容，預設顯示0 

# 這裏使用StringVar屬於Tkinter庫，在介面程式設計的時候，有時需要跟蹤變數值的變化， 
# 以保證值的變更隨時可以顯示在介面上。python無法直接做到，所以定義了一系列新的的物件， 
# 例如StringVar、BooleanVar、DoubleVar、IntVar。 

display = StringVar() 
display.set('0') 

# 新增計算器顯示區域，使用Label，並設定背景色及大小
textLabel = Label(mainUI) 
# 這裏需要注意width寬度的單位，如果你在Label中顯示文字， 
# 那麼這些選項將以文字的單位為定義按鈕的尺寸。 
# 如果你替而代之顯示圖象，那麼按鈕的尺寸將是畫素（或其它的螢幕單位）。 

textLabel.config(bg='grey', width=41, height=7, anchor = SE) 
textLabel['textvariable'] = display 

# 設定顯示區域在Grid佈局中的位置 

textLabel.grid(row=0, column=0, columnspan=4) 

# 新增按鈕並放置到適當的區域 
# 清空按鈕，其中text為按鈕上的文字，fg為按鈕的字型顏色（bg為文字背景的按鈕顏色），width為按鈕寬度 
# command引數為按鈕事件繫結函式，繫結到clear()函式，按鈕按下時觸發 

clearButton = Button(mainUI, text = 'C', fg = 'orange', width = 8, command = clear) 

# 設定清空按鈕的位置，行號為1，列號為0，即第二行第一列 
clearButton.grid(row = 1, column = 0) 

# 其他按鈕位置，由於與清空按鈕類似不再註釋，請自行檢視Grid中的位置，有的按鈕採用lambda來生成匿名函式，原因是需要處理傳入的引數 
Button(mainUI, text = 'DEL', width = 6, command = backspace).grid(row = 1, column = 1) 
Button(mainUI, text = '/', width = 6, command = lambda:updateDisplay('/')).grid(row = 1, column = 2) 
Button(mainUI, text = '*', width = 6, command = lambda:updateDisplay('*')).grid(row = 1, column = 3) 
Button(mainUI, text = '7', width = 6, command = lambda:updateDisplay('7')).grid(row = 2, column = 0) 
Button(mainUI, text = '8', width = 6, command = lambda:updateDisplay('8')).grid(row = 2, column = 1) 
Button(mainUI, text = '9', width = 6, command = lambda:updateDisplay('9')).grid(row = 2, column = 2) 
Button(mainUI, text = '-', width = 6, command = lambda:updateDisplay('-')).grid(row = 2, column = 3) 
Button(mainUI, text = '4', width = 6, command = lambda:updateDisplay('4')).grid(row = 3, column = 0) 
Button(mainUI, text = '5', width = 6, command = lambda:updateDisplay('5')).grid(row = 3, column = 1) 
Button(mainUI, text = '6', width = 6, command = lambda:updateDisplay('6')).grid(row = 3, column = 2) 
Button(mainUI, text = '+', width = 6, command = lambda:updateDisplay('+')).grid(row = 3, column = 3) 
Button(mainUI, text = '1', width = 6, command = lambda:updateDisplay('1')).grid(row = 4, column = 0) 
Button(mainUI, text = '2', width = 6, command = lambda:updateDisplay('2')).grid(row = 4, column = 1) 
Button(mainUI, text = '3', width = 6, command = lambda:updateDisplay('3')).grid(row = 4, column = 2) 
Button(mainUI, text = '=', width = 6, bg = 'orange', height = 3,command = lambda:calculate()).grid(row = 4, column = 3, rowspan = 2) 
Button(mainUI, text = '0', width = 18, command = lambda:updateDisplay('0')).grid(row = 5, column = 0, columnspan = 2) 
Button(mainUI, text = '.', width = 6, command = lambda:updateDisplay('.')).grid(row = 5, column = 2) 
# 進入主迴圈 
mainUI.mainloop()
```
後面沒用到包裝,因為時間不夠,又加上我不會用,會很耗時間,所以我沒用包裝,上面是電腦內的計算機,雖然錯誤很多,但是我們已經改好了!!!

