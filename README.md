# Lock-Unlock-PC-Using-Face-Recognition

This program basically adds a fun feature in your laptop/PC. After setting all of the functions written below your laptop will have a similar feature as that provided by Windows Hello.
But since Windows Hello is not compatible with most of the basic devices there is the need of program like this.

Your laptop will be able to recognize difference between you and any stranger(only to your laptop, may be not for you) and lock unlock itself depending on who is in front of its webcam.

## Requirements :
* Webcam and requisite hardware to run Python 3.6.
* Python Modules - OpenCV, Numpy, PIL(Python Image Library).
* Windows Task Sheduler must be working.

Program has been divided into three Script :
1) create_face_datasets.py - Script that is meant to create dataset. This will capture 100 photos from webcam and will save them in a folder named dataset.(You dont need to create dataset folder, python script will create one on its own).
2) training_model.py - Script which will train the model using dataset which has been already create using above mentioned script.This script will create a folder named trainer and will save a .yml file in it. On successful creation of .yml file model is now trained.
3) lock_unlock_face_recognition.py - Script which will recognize face from webcam and check whether the model is trained for this face or not. If model is trained for this face then process will get terminate. But if the face seems to be strangers then your Work Station will get locked(simple Lock Screen will appear and user will have to open it again and same process will occur).

# How to run script?
####  To run Python Script a script_runner.bat file has already been created. You just have to edit this file and change addresses of python.exe(as it will be different in your laptop as compared to mine) and script which you want to run.

# Steps to setup : 
1) Download all the files and get the location where you have saved your files. First you need to open 
2) 
