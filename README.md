# QRcode1
import pyqrcode
import png
from pyqrcode import QRCode
import tkinter as tk
from tkinter import *
window=Tk()
window.geometry('500x250')
window.title('Pythongeeks')
Label(window,text='Let’s Create QR Code',font='arial 15').pack()
def create_qrcode():
    sl=S.get()
    qr=pyqrcode.create(sl)
    qr.png=png.create(scale=10)
    Label(window,text='QR Code is created and saved successfully').pack()
    Entry(window,textvariable=S,font='arial 15').pack()
    Button(window,text='create',bg='blue',command=create_qrcode).pack()
    window.mainloop()
