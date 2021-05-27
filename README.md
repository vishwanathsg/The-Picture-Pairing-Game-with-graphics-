# The-Picture-Pairing-Game-with-graphics-
This is the graphical version of the picture pairing game

from tkinter import *
from tkinter import messagebox
root = Tk()
root.title("The Picture Pairing Game")
root.geometry("500x500")
from PIL import ImageTk, Image


#Creating pairs for game
pairs = [1,2,2,1]

#creating frame
main_frame = Frame(root)
main_frame.pack(pady=10)

#Defining variables
count = 0
answer_list = []
answer_dictionary = {}

def button_click(b, images, number):
    global count, answer_list, answer_dictionary
    if b["text"] == '' and count <2:
        b["text"] = pairs[number]

        #Add number to answer list
        answer_list.append(number)

        #Add button and number to answer dictionary
        answer_dictionary[b] = pairs[number]

        #incrememnting counter
        count += 1

    if len(answer_list) == 2:
        if pairs[answer_list[0]] == pairs[answer_list[1]]:
            my_label.config(text = "Congratulations! that's the correct pair!")
            for key in answer_dictionary:
                key["state"] = "disabled"
            count = 0
            answer_list = []
            answer_dictionary = {}
        else:
            my_label.config(text="oops! try again")
            count = 0
            answer_list = []
            #pop up box
            messagebox.showinfo("Incorrect", "Incorrect")

            #reset the buttons
            for key in answer_dictionary:
                key["text"] = " "

            answer_dictionary = {}


level1_00 = ImageTk.PhotoImage(Image.open("lv1_00.png"))
my_label0 = Label(image=level1_00)
#my_label0.pack()

level1_01 = ImageTk.PhotoImage(Image.open("lv1_01.png"))
my_label1 = Label(image=level1_01)
#my_label1.pack()

level1_10 = ImageTk.PhotoImage(Image.open("lv1_10.png"))
my_label2 = Label(image=level1_10)
#my_label2.pack()

level1_11 = ImageTk.PhotoImage(Image.open("lv1_11.png"))
my_label3 = Label(image=level1_11)
#my_label3.pack()


#making buttons
b0 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b0, my_label0.pack(), 0))
b1 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b1, my_label1.pack(), 1))
b2 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b2, my_label2.pack(), 2))
b3 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b3, my_label3.pack(), 3))

b0.grid(row=0, column=0)
b1.grid(row=0, column=1)
b2.grid(row=1, column=0)
b3.grid(row=1, column=1)

my_label = Label(root, text="")
my_label.pack(pady=20)

root.mainloop()











#Creating pairs for game
pairs = [1,3,3,2,1,2,3,2,1]

#creating frame
main_frame = Frame(root)
main_frame.pack(pady=10)

#Defining variables
count = 0
answer_list = []
answer_dictionary = {}

def button_click(b, images, number):
    global count, answer_list, answer_dictionary
    if b["text"] == '' and count <3:
        b["text"] = pairs[number]

        #Add number to answer list
        answer_list.append(number)

        #Add button and number to answer dictionary
        answer_dictionary[b] = pairs[number]

        #incrememnting counter
        count += 1

    if len(answer_list) == 3:
        if pairs[answer_list[0]] == pairs[answer_list[1]] == pairs[answer_list[2]]:
            my_label.config(text = "Congratulations! that's the correct pair!")
            for key in answer_dictionary:
                key["state"] = "disabled"
            count = 0
            answer_list = []
            answer_dictionary = {}
        else:
            my_label.config(text="oops! try again")
            count = 0
            answer_list = []
            #pop up box
            messagebox.showinfo("Incorrect", "Incorrect")

            #reset the buttons
            for key in answer_dictionary:
                key["text"] = " "

            answer_dictionary = {}


level2_00 = ImageTk.PhotoImage(Image.open("lv2_00.png"))
my_label0 = Label(image=level2_00)
level2_01 = ImageTk.PhotoImage(Image.open("lv2_01.png"))
my_label1 = Label(image=level2_01)
level2_02 = ImageTk.PhotoImage(Image.open("lv2_02.png"))
my_label2 = Label(image=level2_02)


level2_10 = ImageTk.PhotoImage(Image.open("lv2_10.png"))
my_label3 = Label(image=level2_10)
level2_11 = ImageTk.PhotoImage(Image.open("lv2_11.png"))
my_label4 = Label(image=level2_11)
level2_12 = ImageTk.PhotoImage(Image.open("lv2_12.png"))
my_label5 = Label(image=level2_12)


level2_20 = ImageTk.PhotoImage(Image.open("lv2_20.png"))
my_label6 = Label(image=level2_20)
level2_21 = ImageTk.PhotoImage(Image.open("lv2_21.png"))
my_label7 = Label(image=level2_21)
level2_22 = ImageTk.PhotoImage(Image.open("lv2_22.png"))
my_label8 = Label(image=level2_22)



#making buttons
b0 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b0, my_label0.pack(), 0))
b1 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b1, my_label1.pack(), 1))
b2 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b2, my_label2.pack(), 2))

b3 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b3, my_label3.pack(), 3))
b4 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b4, my_label4.pack(), 4))
b5 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b5, my_label5.pack(), 5))

b6 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b6, my_label6.pack(), 6))
b7 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b7, my_label7.pack(), 7))
b8 = Button(main_frame, text ='', height=3, width=6, command=lambda: button_click(b8, my_label8.pack(), 8))


b0.grid(row=0, column=0)
b1.grid(row=0, column=1)
b2.grid(row=0, column=2)

b3.grid(row=1, column=0)
b4.grid(row=1, column=1)
b5.grid(row=1, column=2)

b6.grid(row=2, column=0)
b7.grid(row=2, column=1)
b8.grid(row=2, column=2)

my_label = Label(root, text="")
my_label.pack(pady=20)

root.mainloop()


