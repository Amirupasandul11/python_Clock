# python_Clock


## 1 

```
'''
Creation of the Digital Clock in Python
'''
from tkinter import *
from tkinter.ttk import *

from time import strftime

main = Tk()

main.title('The Digital clock in Python')

def clock():
	tick = strftime('%H:%M:%S %p')

	clock_label .config(text =tick)

	clock_label .after(1000, clock)

clock_label = Label(main, font =('sans', 80), background = 'yellow', foreground = 'green')

clock_label.pack(anchor= 'center')

clock()
mainloop()

```


## 2

```

# importing the entire tkinter module
from tkinter import *
from tkinter.ttk import *

# to retrieve the system's time, you need to import the strftime function
from time import strftime

# creation of the tkinter window
main = Tk()
main.title('The digital clock in Python')

# This function displays the current time on the label defined herein
def displayTime():
	string = strftime('%H:%M:%S %p')
	clock_label.config(text = string)
	clock_label.after(1000, displayTime)


# creating an attractive look:  needs styling the label widget
clock_label = Label(main, font = ('calibri', 42, 'bold'),
			background = 'purple',
			foreground = 'white')

# defining how to place the digital clock at the centre tkinter's window
clock_label.pack(anchor = 'center')
displayTime()

mainloop()

```

## 3

```
# start by importing all the necessary libraries

from tkinter import *
import sys
import time #library to get the current time
 
#create a function displayTime and variable time_now
def displayTime():
    #show the current hour,minute,seconds
    time_now = time.strftime("%H : %M : %S")
    #clock configuration
    clock_label.config(text=time_now)
    #after every 200 microseconds the clock will change
    clock_label.after(200,displayTime)
 
#Creation of a variable responsible for storing the tkinter window
main=Tk()
#window size defined
main.geometry("720x420")

#First label - shows the time,
#Second label - shows hour:minute:second,
#Third label - shows the digital clock's title at the top
clock_label=Label(main,font=("times",72,"bold"),bg="yellow")
clock_label.grid(row=2,column=2,pady=25,padx=100)
displayTime()
 
#creation of a digital clock's variable
digital_clock_title=Label(main,text="The Digital Clock in Python",font="times 24 bold")
digital_clock_title.grid(row=0,column=2)
 
hours_mins_secs=Label(main,text="Hours        Minutes        Seconds",font="times 15 bold")
hours_mins_secs.grid(row=3,column=2)
 
main.mainloop()

```
