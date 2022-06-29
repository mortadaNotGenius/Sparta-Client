from tkinter import *                                  #types of relief font "RIDGE GROOVE  SUNKEN RAISED FLAT"
from time import *
import os
from tkinter import messagebox
import webbrowser
import sys
import subprocess
from tkinter import Tk, font
from tkinter import ttk
#gui main app
window = Tk()  # open window
window.geometry("1280x800")  # size
desert = PhotoImage(file="desert.png")
desert1 = Label(window,image=desert)
desert1.pack(side=LEFT)
desert1.place(x=0,y=0)
window.title("Sparta Client")  # title the window
photo = PhotoImage(file="photo Client.png")  # icon photo

window.iconphoto(True, photo)
Sparta = Label(window, text="Sparta Client", font=("arial", 35, "bold"), fg="#1B2631", bg="#3498DB", relief=RAISED,
              bd=10, padx=30, pady=10)
Sparta.pack()  # label text with color and background and font, size and title


label = Label(window, text="To stop the Robot do Ctrl+Q or pause Ctrl+P", font=("arial", 25, "bold"), fg="white", bg="black", relief=FLAT,
              bd=10, padx=20, pady=10,borderwidth = 0)
label.pack()
def discordlevel():
    os.startfile("Sparta discord level.exe")


button = Button(window,
text="Discord Auto level",
font=("IMPACT", 20, "bold"),
fg="white", bg="#239B56", activeforeground="white",
activebackground="#239B56",
command=discordlevel,
state=ACTIVE,padx=3,pady=5)
button.place(x=-10,y=300)


def AutoBuild():
    os.startfile("Sparta Auto Build NBT.exe")


button = Button(window,
text="Auto Build NBT NPC",
font=("Consolas", 22, "bold"),
fg="white", bg="green", activeforeground="white",
activebackground="green",
command=AutoBuild,
state=ACTIVE,padx=2,pady=7)
button.pack(side=LEFT)
button.place(x=-10,y=370)

def Realmfinder ():
    os.startfile("auto realm finder.exe")

button = Button(window,
text="Auto realm finder Bedrock",
font=("Comic sans Ms", 22, "bold"),
fg="yellow",bg="Black",activeforeground="yellow",
activebackground="Black",
command=Realmfinder,relief=FLAT,
state=ACTIVE,padx=1,pady=1)
button.pack(side=LEFT)
button.place(x=-10,y=445)


def Extractor ():
    os.startfile("Extractor Commands NBTs .exe")
#auto realm finder button
button = Button(window,
text="Extractor NBTs commands",
font=("Uniespace", 20, "bold"),
fg="black",bg="#239B56",activeforeground="black",
activebackground="#239B56",
command=Extractor,relief=FLAT,
state=ACTIVE,padx=0,pady=5)
button.pack(side=LEFT)
button.place(x=-10,y=520)


def AutoFarmMinecraft ():
    os.startfile("Auto Farm Minecraft .exe")

button = Button(window,
text="Auto Farm Minecraft",
font=("IMPACT", 21),
fg="white",bg="#239B56",activeforeground="white",
activebackground="#239B56",
command=AutoFarmMinecraft,relief=FLAT,
state=ACTIVE,padx=1,pady=5)
button.pack(side=LEFT)
button.place(x=-10,y=590)

def AutoBuildV2CBE ():
    os.startfile("Sparta Auto Build NBT  V2.exe")

button = Button(window,
text="Auto Build V2 CBE",
font=("IMPACT", 21),
fg="Navy",bg="Silver",activeforeground="Navy",
activebackground="Silver",
command=AutoBuildV2CBE,relief=FLAT,
state=ACTIVE,padx=1,pady=5)
button.pack(side=LEFT)
button.place(x=410,y=300)

def Realmlist ():
    webbrowser.open('https://downgit.github.io/#/home?url=https://github.com/mortadaNotGenius/Sparta-Client/blob/main/realm%20code%20list%20by%20mortada.txt')

button = Button(window,
text="Realm list Bedrock",
font=("IMPACT", 21 , "bold"),
fg="orange",bg="Black",activeforeground="orange",
activebackground="Black",
command=Realmlist,relief=FLAT,
state=ACTIVE,padx=0,pady=5)
button.pack(side=LEFT)
button.place(x=409,y=373)

def NBTGENERATOR ():
    os.startfile('NBT.Generator.exe')

button = Button(window,
text="NBT Generator",
font=("IMPACT", 21 , "underline"),
fg="white",bg="Black",activeforeground="white",
activebackground="Black",
command=NBTGENERATOR,relief=FLAT,
state=ACTIVE,padx=0,pady=5)
button.pack(side=LEFT)
button.place(x=409,y=450)


#terms of services check box

def terms():
    if(x.get()==1):
        messagebox.showinfo(title="Terms of Services",message='1 = Use it at your own risk.\n2 = you are not allowed to sell'
        '\n3 = if u find problems please tell us, thank you \n4 = You Can Share only the original link')

x = IntVar()

check_button = Checkbutton(window,text="terms of services",variable=x,
                           onvalue=1,
                           offvalue=0,
                           command=terms,font=("arial",15),fg="red",bg="#151515"
                           ,activebackground="#151515"
                           ,activeforeground="red")
check_button.pack(side=TOP, ipady=1)
check_button.pack()

#gui clock
def update():
    time_string = strftime("%I:%M:%S %p")
    time_label.config(text=time_string)

    day_string = strftime("%A")
    day_label.config(text=day_string)

    date_string = strftime("%B %d, %Y")
    date_label.config(text=date_string)

    window.after(1000,update)


time_label = Label(window,font=("Arial",40 ,"bold"),fg="#00FF00",bg="black")
time_label.pack()

day_label = Label(window,font=("Fira Code",35,"bold"),fg="red",bg="black")
day_label.pack(side=BOTTOM,padx=5,pady=5)

date_label = Label(window,font=("Sans",27),fg="red",bg="black")
date_label.pack(side=BOTTOM)

update()

def Github():
 webbrowser.open('https://github.com/mortadaNotGenius/Sparta-Client')

Github = Button(window,
text=" Github ",
font=("DejaVu Sans Mono", 25 ,""),
fg="yellow", bg="black", activeforeground="yellow",
activebackground="black",
command=Github,
state=ACTIVE,relief=FLAT)
Github.pack(side=LEFT,padx=10,pady=10)
Github.place(x=5,y=10)


def Clean():
 os.startfile("test.bat - Shortcut")


Clean = Button(window,
text=" Clean ",
font=("DejaVu Sans Mono", 27 ,"bold"),
fg="white", bg="black", activeforeground="white",
activebackground="black",
command=Clean,
state=ACTIVE,relief=FLAT)
Clean.pack(side=LEFT,padx=50,pady=10)
Clean.place(x=5,y=100)


discord = PhotoImage(file="discord.png")
def Discord():
 webbrowser.open('https://discord.gg/d5yxxSRW6T')

discord1 = Button(window,
text=" Discord link  ",
font=("Vintage", 25),
fg="#6495ED", bg="#1B2631", activeforeground="#6495ED",
activebackground="#1B2631",
command=Discord,
state=ACTIVE,image=discord)
discord1.pack(side=RIGHT,padx=50,pady=50)
discord1.place(x=0,y=750)


window.mainloop()
