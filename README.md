# menu-baar
TITLE = (HOW TO CREATE A MENUBAR)

CODE
from  tkinter import *

def save():
    print("file has been saved")
def delete():
    print("file has been delete")
def move():
    print("file has been moved")
window= Tk()

saveimage=PhotoImage(file="save.png")
deleteimage=PhotoImage(file="delete.png")
#movimage=PhotoImage(file="move")

menubar=Menu(window)
window.config(menu=menubar)

filemenu=Menu(menubar,tearoff=0,font=("MV boli",10))
menubar.add_cascade(label="File",menu=filemenu)
filemenu.add_separator()
filemenu.add_command(label="save",command=save,image=saveimage,compound='left')
filemenu.add_separator()
filemenu.add_command(label="delete",command=delete,image=deleteimage,compound='left')
filemenu.add_separator()
filemenu.add_command(label="move",command=move )#,image=movimage)

editmenu=Menu(menubar,tearoff=0,font=("MV boli",10))
menubar.add_cascade(label="Edit",menu=editmenu)
editmenu.add_command(label="edit all")
editmenu.add_separator()
editmenu.add_command(label="un edit all")
editmenu.add_separator()
editmenu.add_command(label="unchaged")
viewmenu=Menu(menubar,tearoff=0,font=("MV boli",10))
menubar.add_cascade(label="View",menu=viewmenu)
savemenu=Menu(menubar,tearoff=0,font=("MV boli",10))
menubar.add_cascade(label="Save",menu=savemenu)
deletemenu= Menu(menubar,tearoff=0,font=("MV boli",10))
menubar.add_cascade(label="Delete",menu=deletemenu)


window.mainloop()

END()...............................................................................

TITLE  (HOW TO CREATE BUTTONS IN A FRAME)

CODE
from tkinter import *

window= Tk()

frame=Frame(window,bg="pink",bd=5,relief=SUNKEN)
#frame.pack(side=BOTTOM)
#or
frame.place(x=0,y=30)

Button(frame,text="W",font=("Arial",20)).pack(side=TOP)
Button(frame,text="A",font=("Arial",20)).pack(side=LEFT)
Button(frame,text="B",font=("Arial",20)).pack(side=LEFT)
Button(frame,text="C",font=("Arial",20)).pack(side=LEFT)

window.mainloop()

END()..........................................................................................................

TITLE= (HOW TO CREATE NEW WINDOW AND DESTROY OLD WINDOW)
CODE
from tkinter import *

def create_window():
    #new_window=Toplevel()
    new_window=Tk()
    window.destroy() #finish the window or delete the window

window=Tk()

button=Button(window,text='create new window',command=create_window)
button.pack()

window.mainloop()

END().................................................................................................

