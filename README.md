# Raspberry pi photobooth 
### University of Agder, IS-213 Semester Project 



![alt text](https://i.gyazo.com/3fd2cb4127e25c7e600b90c4a1a52758.jpg)
### This photo booth is meant to work as a fun gadget people can use in social events to take fun photos with friends or colleagues.
### The photo booth works with dropbox and will automatically upload your pictures to chosen dropbox folder.


## Table of Contents

1. [Hardware](#hardware)
2. [Software](#Software)
3. [Installation](#Installation)
4. [Setup](#Setup)
5. [License](#License)
6. [Contribute](#Contribute)

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
   
1. Start the setup with pulling / cloning the repository from github: https://github.com/herms97/photoBooth
   
2. Locate the folder called ‘dropbox-uploader’ that should be included when pulling / cloning from our github.
   ### Note: 
   You may have pulled or cloned the project to a specific folder, make sure when changing directory that you        know where the dropbox-uploader is located.
      
   Go into cmd (command window) and type:
        
   `cd dropbox-uploader`
      
   `ls`

   (The command ls, will list files in the folder you are located. You do not have to do this, but you will           then see that the script dropbox_uploader.sh is inside the folder dropbox_uploader).

   Simply run the script by typing: 
      
    `./dropbox_uploader.sh`
    
    If this dont work, type:
      
    `chmod +x dropbox_uploader.sh`
     
    This will allow you (give permission) to execute the file.
      
    First time executing the shell script will give you this:
      
    --link
    
3. You need to create an account at DropBox - you do not have to pay for an account, do not worry.

4. Now you have to create an app, where you can get an access token (connect your dropbox app folder to the          script). Click here to create dropbox app

5. Click create app, and fill out:

   --link
   --link
   
6.  When you have given a name and created your app, you should be able to see this when you scroll down:
    
    --link
    
    Click on the generate button, then your access token will be displayed.
    
    --link
    
7.  Type in the generated access token in the input field, hit enter, then type y and enter again to confirm:
    
    --link
    
    ### If you entered the correct token you are done setting up your dropbox!
    
    If you unfortunately entered wrong token, you can simply run the script `./dropbox_uploader.sh` again, then       this will show up:

    --link
    
    It will list several commands, make sure you type `./dropbox_uploader.sh unlink`. Then you will get this         message: make sure to type `y` (if you want to reset) then hit enter. Now if you type `./dropbox_uploader.sh`     you will see the same as shown in the previous picture. Just make sure to type in the correct access token.
    
    ### Note:
    Your folder names might not be the same as the path in our code, follow next step beneath to be sure.
    
## License
Collection of licenses that applies to this project.

### Our license
[Licensed under the MIT license](https://github.com/herms97/photoBooth/blob/master/LICENSE)

The reason for licensing our project under the MIT license is that our project is based on other open source projects and that we want our project to be open for others to use. We want this project to be open so that others can contribute or use it as they like. The MIT license is therefore a good fit because it is very open for every kind of use, but doesn’t guarantee any kind of warranty or liability which we don’t have the resources for or can guarantee.

### 3rd party licenses
[PyGame is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)\
[PiCamera is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)\
[Python 2.2 and above is licensed under the LGPL 3.0 license](https://opensource.org/licenses/lgpl-3.0.html)







