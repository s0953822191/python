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
左下有一個開始,按右鍵找到職行(R),因為要下在所以打上pip install pyinstaller按Enter,但上面那些
需要下載到桌面，所以先打開Python把上面計算體重的東西複製下來，執行、在建立一個檔案名字隨便，放到桌上
在打上            進去資料夾裡找上面顯示的檔案biet
