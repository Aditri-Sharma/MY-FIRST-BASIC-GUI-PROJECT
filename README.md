# MY-FIRST-BASIC-GUI-PROJECT

from tkinter import *
root=Tk()
root.title("LOGIN PAGE")
root.geometry("500x400")
menu=Menu(root)
item=Menu(menu)
item.add_command(label="new file")
item.add_command(label="open file")
item.add_command(label="recent files")
menu.add_cascade(label="file",menu=item)
root.configure(menu=menu)
l=Label(root,text="Welcome to this login page.................",fg="blue")
l.grid()
lb=Label(root,text="Username",fg="pink")
lb.grid(row=1,column=2)
input_wid=Entry(root)
input_wid.grid(row=1,column=3)
lbl=Label(root,text="Password",fg="pink")
lbl.grid(row=2,column=2)
input_widget=Entry(root)
input_widget.grid(row=2,column=3)
label=Label(root,text="click enter to login..........",fg="brown")
label.grid(row=6,column=2)
def clicked():
    label.configure(text="logged in")
btn=Button(root,text="LOGIN",fg="black",command=clicked)
btn.grid(row=4,column=2)

root.mainloop()
