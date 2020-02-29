"# Youtube-video-downloader" 

import os
from tkinter import *

win =Tk()
win.geometry("350x350")
win.title("MADE BY---HEMRAJ")
def runit():
    os.startfile('link.bat')
    
def downloadytv():
    with open('link.bat','w') as down_load:
        down_load.write(f'youtube-dl {link.get()}')
        down_load.close()
    runit()

f=Frame(win)
f.grid()
Label(f,text="***youtube video downloader (-.-) ***",font=15,padx=6).pack()
f1=Frame(win)
f1.grid()
Label(f1,text="Enter utube link here",font=5).grid(row=1)

link=StringVar()
Entry(f1,font=5,textvariable=link).grid(row=1,column=1,pady=5,padx=10)
Button(f1,text="Download",padx=50,relief=RAISED,font=10,borderwidth=5,command=downloadytv).grid(column=1,pady=5)
win.mainloop()

