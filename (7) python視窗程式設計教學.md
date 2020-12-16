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
