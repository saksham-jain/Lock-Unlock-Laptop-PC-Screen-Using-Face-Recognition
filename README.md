# Lock-Unlock-Laptop/PC-Screen-Using-Face-Recognition
## Face ID-like feature for windows.
#### Kindly note that this program cannot be used as a serious authentication system for your laptop/PC. This has been designed only for general purposes. 

I have been using this program and it works just fine for me.
This program basically adds a cool feature in your laptop/PC. After setting all of the functions written below your laptop will have a similar feature as that provided by Windows Hello.
But since Windows Hello is not compatible with most of the basic devices there is the need of program like this.

Your laptop will be able to recognize difference between you and any stranger (only to your laptop, maybe not for you) and lock unlock itself depending on who is in front of its webcam.

## Requirements :
* Webcam and requisite hardware to run Python 3.6.
* Python Modules - OpenCV, Numpy, ~PIL (Python Image Library)~ Pillow (PIL is no longer maintained, Pillow is a fork of PIL), pyautogui (Used to operate mouse and keyboard using python script).
* Windows Task Scheduler must be working.

Program has been divided into three Script :
1) create_face_datasets.py - Script that is meant to create dataset. This will capture 100 photos from webcam and will save them in a folder named dataset. (You dont need to create dataset folder, python script will create one on its own).
2) training_model.py - Script which will train the model using dataset which has been already created using above mentioned script. This script will create a folder named trainer and will save a .yml file in it. On successful creation of .yml file, the model is now trained.
3) lock_unlock_face_recognition.py - Script which will recognize face from webcam and check whether the model is trained for this face or not. If model is trained for this face, then process will get terminated. But if the face seems to be someone else, then your workstation will get locked (simple lock screen will appear depending on your lock screen setting of Windows and user will have to open it again and same process will occur).

# How to run script?
#### To run Python Script, a script_runner.bat file has already been created. You just have to edit this file and change addresses of python.exe (as it will be different in your laptop as compared to mine) and script which you want to run.

# Steps to setup : 

1) Download all the files and get the location where you have saved your files. 
2) Install all the prerequisites using ```pip install -r requirements.txt```
3) Run create_face_datasets.py using .bat file (as mentioned above). Make sure you have changed the address of xml file in script otherwise you will get an error. 
4) Now run training_model.py. You can check trainer folder has been created and yml file is inside it.
5) Now change name of script in .bat file to lock_unlock_face_recognition.py and run .bat file. This will run lock_unlock_face_recognition.py. 
6) In order to make above py file run automatically, you will have to setup task scheduler. For this open Windows Task Scheduler and Create Task. A window will appear. In Triggers tab click New and select 'On workstation Unlock' in drop down menu.
7) Now in Action tab, click new and select 'Start a Program' in drop down menu, Then browse the script_runner.bat file and select it.         
Congrats!! Works has been done.
*) Now you just have to check by locking your device.

Comments has been added in scripts to understand codes.

### Improvements will be appreciated. Thank you in advance.
