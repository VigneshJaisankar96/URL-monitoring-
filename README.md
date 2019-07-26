# URL-monitoring-
# Opening multiple url in single browser
# taking screenshot of each tab in browser
# saving the screenshot using variable name 
import time
import pyautogui
import ctypes  
import subprocess
import win32api
from pymsgbox import *
subprocess.call([r'path\file_name.bat'])  #code to open bat file which opens multiple url in browser
i=0

time.sleep(70)  #waiting delay until the page loads
while(i!=number of url):
    # below line is for adding variable name along with filename to save screenshot
    pyautogui.screenshot(r"path\filename"+str(i)+".png") 
    pyautogui.hotkey('ctrlleft', 'pagedown') #command to switch between tabs
    time.sleep(2) 
    i=i+1

#this below code is for pages which gives popups whenever the page is loaded so u can automatically cancel the popups using keyboard controls
time.sleep(3)
subprocess.call([r'path\file_name.bat'])
time.sleep(5)
pyautogui.press('tab') #popups with okay & cancel button can be highlighted using tab key press
pyautogui.press('tab')
pyautogui.press('tab')
pyautogui.press('enter') #by pressing enter on the highligted button you can cancel the popup then you can take the screenshot
pyautogui.screenshot(r"path\screenshot"+str(i)+".png")
    

if(i>=number of URL):
    win32api.MessageBox(0, 'hello', 'title',1)  #message box for alert after completion
    alert(text='Screenshot taken', title='ALERT', button='OK') #alert box for after completion
    

