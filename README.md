# dice_simulator
RANDOM DICE ROLLING SIMULATION GAME

from tkinter import *
import random

root = Tk()

root.configure(bg="white")

root.geometry("500x500")

root.title("Dice rolling stimulator")

root.resizable(0,0)





def roll_dices():
    dice_dots = ['\u2680', '\u2681',
                 '\u2682', '\u2683',
                 '\u2684', '\u2685']
    
    result1= random.choice(dice_dots)
    result2= random.choice(dice_dots)
    label.configure(text=f'{result1}{result2}')
    label.pack()

    converted1=ord(result1)
    converted2=ord(result2)
    
    if(converted1>converted2):
         labelX= Label(root, text="Player one wins ", font=("Arial", 10))
         labelX.place(x=195, y=200)
    else:
        labely= Label(root, text="Player two wins ", font=("Arial", 10))
        labely.place(x=195, y=200)



   


roll_button = Button(root, text=" Click to Roll Dice",
                     width=20, height=2,
                     font=15, bg="yellow",
                     bd=2, command=roll_dices)
label3 = Label(root, text="Click to Roll Again ", font=("Arial", 10))
label3.place(x=195, y=5)

label1 = Label(root, text="PLAYER 1 ", font=("Arial", 10))
label1.place(x=100, y=100)

label2 = Label(root, text="PLAYER 2 ", font=("Arial", 10))
label2.place(x=300, y=100)


roll_button.pack(padx=10, pady=15)

label = Label(root, font=("Arial", 250),
              bg="black", fg="blue")

root.mainloop()
