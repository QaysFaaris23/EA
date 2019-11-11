# QAYS FAARIS's JOURNAL

<img src="https://github.com/QaysFaaris23/The-Engineering-Academy/blob/master/WIN_20191106_22_02_05_Pro%20(2).jpg" width ="300">

Firstly, i would like to explain how i made this blog. I used thid website called Dilinger,which uses markdown and i was able to see in realtime how my edits affected the changes in the blog.This website has the ability to link to one of your Github repositories and thus it was convenient as it saved directly to that repository.

<img src="https://github.com/QaysFaaris23/The-Engineering-Academy/blob/master/Screenshot_of_Dilinger_Website.PNG" width ="1000">

Hi welcome to my weekly journal

# Week 1

### Space Invaders
 After some tests i finally managed to make a sort of functional code.Here is the code:
 ```sh
 from microbit import *
import random
spaceship_x = 2
alienz_x= random.randint(0,4)
alienz_y=0

while True:
    display.clear()
    display.set_pixel(spaceship_x, 4, 5)
    display.set_pixel(alienz_x,alienz_y,9)
    alienz_y=alienz_y +1
    if button_a.is_pressed():
        spaceship_x = spaceship_x - 1
        if spaceship_x ==-1:
            spaceship_x = 0
    if button_b.is_pressed():
        spaceship_x = spaceship_x + 1
        if spaceship_x == 5:
            spaceship_x = 4
    if alienz_x == spaceship_x and alienz_y ==5:
        break
    if alienz_y==5:
        alienz_y=0
        alienz_x= random.randint(0,4)
    sleep(250)
    
display.scroll("YOULOSE",loop=True)
 ```
I faced many diffulties. One such was the microbit had an error if the user presses the button lets say on the right side and it exceded the screen of the microbit, causing an error.I remedied the error by making sure the X value remained the max(4)/min(0) value by making the values returned to the max of min value if exceded. eg if x==6: x=5

I also encountered the problem of the "alien" always spawning at the same X axis.I solved by assigning the alien's X axis to a "random.randit" command everytime it reaches the bottom of the display so it respawns at a random X axis on top.

One tip id give users is always read the error messages as they are really useful, and to not rush writing your codes as you are definitely bound to make careless mistakes.



