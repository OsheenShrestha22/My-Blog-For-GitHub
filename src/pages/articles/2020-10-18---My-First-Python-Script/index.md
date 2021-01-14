---
title: Let's Automate Zoom Using Pyautogui
date:  "2020-09-17T22:40:32.169Z"
layout: post
draft: false
path: "/posts/AutomateZoom/"
category: "Project"
tags:
  - "First Project"
  - "Automation"
  - "Pyautogui"
  - "Zoom"
description: "Hey! This is my first python project where I have learned to automate zoom using Pyautogui."
---

Hey! This is my first python project where I have learned to automate zoom using **Pyautogui**.
Due to the pandemic, it's been more than months that I have been working from home. I feel so fortunate enough that I can work from home.
Our manager has requested to host the zoom during the working hour to create a virtual work environment. Since Deerwalk is not wealthy enough to buy a premium version we need to add the zoom id every 40 minutes which I found tiresome. Therefore, I decided to automate this instead. And I thought since I have learned Python why not show some of my Python skills.
Here, is the code that I have written.

~~~
import pyautogui
import time
import os
import sys

def automate_zoom():
    os.startfile('C:\\Users\\Lenovo\\AppData\\Roaming\\Zoom\\bin\\Zoom.exe')
    time.sleep(5)
    pyautogui.FAILSAFE = True
    pyautogui.click(800, 450) # Depend on your screen size
    pyautogui.write('01111111111', interval=0.25) # Zoom id here
    pyautogui.press('enter')
    time.sleep(15)
    pyautogui.typewrite('01Liq2t', interval=0.25) # Password here
    pyautogui.press('enter')
    pyautogui.press('enter')

automate_zoom()
~~~

In order to run this script every 40 minutes, we need to create a task in the task scheduler.
Steps:

* Go to the task scheduler
* In the right side, click the create basis task
* A window will pop up:
  * Put the name for the task. For mine, I have named Automate Zoom

* Then click the action tab, hit the new button
* In Program/Script, place the location of your python.exe
  * C:\Python\Python382\python.exe
* For Add arguments(optional), place the location of your python script
  * "C:\Users\Lenovo\Desktop\Automate\automate zoom.py"
* Hit the ok button
* Again in Triggers tab,
* Click the task that you have created and hit the edit button

* Then follow the screen shot

![Posing for Instagram feed.](./Capture\\.jpg)

Hope this project will be useful for you guys as well
