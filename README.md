# Raspberry pi photobooth 
### University of Agder, IS-213 Semester Project 



![alt text](https://i.gyazo.com/3fd2cb4127e25c7e600b90c4a1a52758.jpg)
### This photo booth is meant to work as a fun gadget people can use in social events to take fun photos with friends or colleagues.
### The photo booth works with dropbox and will automatically upload your pictures to chosen dropbox folder.


## Table of Contents

1. [Intent](#Intent)
2. [Hardware](#hardware)
3. [Software](#Software)
4. [Installation](#Installation)
5. [Setup](#Setup)
6. [Tutorial](#tutorial)
7. [License](#License)
8. [Contribute](#Contribute)
9. [Credits](#Credits)

## Intent:
  Our intention with this project is to make a fun and easy to learn/use program that will drive more young people into the open source  
  community and hopefully will draw new developers into open source. PhotoBooth are more populare in weddings and social events than 
  before, this photobooth works with dropbox wich is also populare by the youth today and with our photobooth its is possible to further 
  develop and customize the photobooth to your need. We hope that this will trigger new developers to get into open source and further 
  develop the community


## Hardware
1. Raspberry Pi 3 model B plus
2. Raspberry Pi Camera module
3. Micro usb cable (to power raspberry)
4. micro-Sd card (with Raspbian) 
5. Ethernet cable (wifi works to as long as its optional on you raspberry)

![alt text](https://i.gyazo.com/7bfbf4dce722df779b5b43597ac0ee86.jpg)
picture of hardware used

## Software
1. Raspbian (OS)
2. Picamera
3. PyGame
4. Python
5. VNC (optional if you want to control it with another device) 

## Installation
Before Running the code we need to make sure everything is up to date. If the software above is installed and up to date you can go 
directly down to [setup](setup)

1. PyGame
  Download PyGame by typing the following into the command line:
  sudo apt-get install python-pygame
  
2. Camera
  Before installing Picamera, we will have to activate the camera.
  Follow this Guide if you haven't activated the raspberry camera before: 
  https://thepihut.com/blogs/raspberry-pi-tutorials/16021420-how-to-install-use-the-raspberry-pi-camera
 
 3. Picamera 
  (1) Download Picamera by typing the following into the command line:
      sudo apt-get update
      sudo apt-get install python3-picamera


  (2) Activate camera
      Activate Picamera by typing the following into the command line:
      sudo raspi-config
      Select ‘Enable camera’ and reboot the Raspberry Pi.
      
  4. Python
    Download Python by typing the following into the command line:
    sudo apt-get update
    sudo apt-get install python3 
    
    
## Setup

#### Dropbox
   
1. Start the setup with pulling / cloning the repository from github: https://github.com/herms97/photoBooth
   
2. Locate the folder called ‘dropbox-uploader’ that should be included when pulling / cloning from our github.
   ### Note: 
   You may have pulled or cloned the project to a specific folder, make sure when changing directory that you        know where the dropbox-uploader is located.
      
   Go into Terminal (command window) and type:
        
   `cd dropbox-uploader`
      
   `ls`

   (The command ls, will list files in the folder you are located. You do not have to do this, but you will           then see that the script dropbox_uploader.sh is inside the folder dropbox_uploader).

   Simply run the script by typing: 
      
    `./dropbox_uploader.sh`
    
    If this dont work, type:
      
    `chmod +x dropbox_uploader.sh`
     
    This will allow you (give permission) to execute the file.
      
    First time executing the shell script will give you this:
      
   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_9.png)
    
3. You need to create an account at DropBox - you do not have to pay for an account, do not worry.

4. Now you have to create an app, where you can get an access token (connect your dropbox app folder to the          script). Click here to create dropbox app

5. Click create app, and fill out:

   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_7.png)
   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_8.png)
   
6.  When you have given a name and created your app, you should be able to see this when you scroll down:
    
    ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_5.png)
    
    Click on the generate button, then your access token will be displayed.
    
    ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_6.png)
    
7.  Type in the generated access token in the input field, hit enter, then type y and enter again to confirm:
    
     ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_9.png)
    
    ### If you entered the correct token you are done setting up your dropbox!
    
    If you unfortunately entered wrong token, you can simply run the script `./dropbox_uploader.sh` again, then this will show up:
    ![Alt text]( https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/startover_dropboxcmd.png)
    
    It will list several commands, make sure you type `./dropbox_uploader.sh unlink`. Then you will get this         message: make sure to type `y` (if you want to reset) then hit enter. Now if you type `./dropbox_uploader.sh`     you will see the same as shown in the previous picture. Just make sure to type in the correct access token.
    
    ### Note:
    Your folder names might not be the same as the path in our code, follow next step beneath to be sure.
    
#### choose folder where your images should be uploaded

1. To upload images to your wanted folder, open up the python file camera.py included in the photoBooth folder.

   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_2.png)
   
2. Scroll down to line 364, as you can see on the left side. If code-line option is not turned on, press `ctrl+f`    on windows or `cmd+f` on mac to open up the search bar inside your IDE and simply enter `command`. 

   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_3.png)
  
   You should then easy locate this line of code:
  
   ![Alt text](https://github.com/herms97/photoBooth/blob/testMasterXXX/picturefiles/Screenshot_1.png)

3. On line 364, as seen in the screenshot from our code, you can see behind `+ Dropbox_var +` the folder for        where the image is uploaded to the dropbox. In our code we have `/Apps/PythonUploader/` because this is the      folder where we wanted to upload our pictures.

   You just have to change this to your desired path, and now you are done.
   
   ### Note:
   The program will run an exception if the path to your folder includes typos, or foloder do not exist. It is      also case sensitive so remember to type the path correctly.
   
   
## Tutorial
To Run the program simply type in terminal: Python camera.py
This will run the program, and then its you just have to follow the instruction on the screen, which is basiclly "press the arrowkey facing down" and to exit simply press "ESC" and it will stop the program.
  
   
   
## License
Collection of licenses that applies to this project.

### Our license
[Licensed under the MIT license](https://github.com/herms97/photoBooth/blob/master/LICENSE)

The reason for licensing our project under the MIT license is that our project is based on other open source projects and that we want our project to be open for others to use. We want this project to be open so that others can contribute or use it as they like. The MIT license is therefore a good fit because it is very open for every kind of use, but doesn’t guarantee any kind of warranty or liability which we don’t have the resources for or can guarantee.

### 3rd party licenses
[PyGame is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)\
[PiCamera is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)\
[Python 2.2 and above is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)



## Credits
This idea was inspired and built up of two projects.
### We used theese two project as inspiration and built our own simulare project based on theire technincs

### Project 1: https://github.com/sabat54i/photoboothdiy/blob/master/camera.py
Project 1 is made by Anthony Sabatella (Github user: sabat54i). He made the photobooth printer that our project is built on.
You can read more about his project here:https://www.hackster.io/sabat54i/wedding-photo-booth-with-raspberry-pi-1cea3a

### project 2: https://github.com/andreafabrizi/Dropbox-Uploader
Project 2 is made by Andrea Fabrizi (github user: andreafabrizi). He made the dropbox uploader (that we used for inspiration).
You can read more about the dropbox uploader here: https://raspi.tv/2013/how-to-use-dropbox-with-raspberry-pi.




