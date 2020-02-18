## Ashwins weekly journal 




Welcome to my weekly Journal
> ### Week 1
Creating the Weekly Journal
<p>&nbsp;</p>
To create the journal I used a text editor with a Markdown preview ,
---
layout: post
title: How to MarkDown and Git
---

"Markdown is a markup language without tags. So basically, you use special symbols before the sentence or words you want to type to style it."

For example

```
 # Example 1
 ## Example 2
 ### Example 3
 #### Example 4
```

will give you

# Example 1

## Example 2

### Example 3

#### Example 4

> Spacing **AFTER** the hashtags are **very very** important

Some more things you can do

```
*Test1*
**Test2**
~~Test3~~
```

_Test1_
**Test2**
~~Test3~~

Even **MORE** things you can do

```
>Lorem Ipsum
1. This
2. Is
3. A
4. List
```

> Lorem Ipsum

1. This
2. Is
3. A
4. List

And finally, I'm too lazy too add more of the things you can do, so this is the final one

````c++
 "```"c++
  cout << "Code here" << endl;
 "```"

 [hyperlink text](www.theActualLinkItself.com.sg)
````

> remove the bunny ears, its there just to make everything is rendered properly

```c++
 cout << "Code here" << endl;
```

[hyperlink text](www.theActualLinkItself.com.sg)

Learn more by clicking here: [how to MD](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Learning how to git (collab)

Go to the directory that you want to save the repo in **locally**
Key in the following to clone the whole repo

```git
git clone <insert_git_url>
```

That's it!
With that you will have the whole repo locally in your computer :D

#### Making changes

When you make changes in the repo, follow the following flow.
**Always** fetch before making changes, fetching will get all the other changes that others (might) have done.

```c++
git pull
```

After fetching, you can now do your work!
When you have done doing your work always remember to _Ctrl + S_ !
BUT, this will only make changes locally, to save it to your repo, do

```c++
git commit -a -m "<Description here"
```

This will save your changes into your repo, much like saving your files locally.
However, try to commit in logical chucks of changes as this will help in your version controlling in the future
<p>&nbsp;</p>



> ### Week 2
Mark down update
Our team learn about this markdown editor called https://dillinger.io/
it really helps out in workflow as we are able to really type things out quikly:)


> ### Week 3
Im used to coding in C++ and java ect but never used python however mr rodney intorduced it to us so for the remiander for this journal im going to use python:

**if your new to New to python?**

Useful links for Thonny IDE:

[![](http://img.youtube.com/vi/lWaCl0WjNZI/0.jpg)](http://www.youtube.com/watch?v=lWaCl0WjNZI "")

 * Complete guide to downloading and setting up Thonny IDE
 * Basic walk-through into simple arithmetic and functions
# thonny is a use full ide to have because it enables u to do every thing even flashing ur micro python board 

The main board we are going to use is the Esp 32 board https://www.espressif.com/en/products/hardware/esp32/overview
its the  wroom esp 32 board it looks like this :0
<img src="https://img3.bgxcdn.com/thumb/large/oaupload/banggood/images/91/B5/e0d42ff6-a8c7-44ba-8576-89f62f1d5c5a.jpeg" width =“500”>

Imagine an arduino but on steroids yes that my friend is what the esp 32 is

another Board we recived was the BBc micro bit it is a board that is actually given free to most singaporeans so if you want on go down to those coding competion 
the microbit allows you to do micropython coding , and if your new to coding they even have block coding on their website https://microbit.org/
if ur wonderin g how it looks like heres how it looks like 
<img src="data:image/jpeg;base64,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" width =“500”>

one of the abilities of the microbit is the ability to read accelometer and it even has a lcd display which u can play around below is a basic code for the microbit for a code for space invaders game

### space invaders  

### Space Invaders
 So after playing around in the microbit heres my code:
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

I also encountered the problem of the "alien" always spawning at the same X axis.I solved by assigning the alien's X axis to a "random.randit" command everytime it reaches the bottom of the display so it respawns at a random X axis on top so ya 








