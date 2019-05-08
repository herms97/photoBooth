# Raspberry pi photobooth 
### University of Agder, IS-213 Semester Project 



![alt text](https://i.gyazo.com/3fd2cb4127e25c7e600b90c4a1a52758.jpg)
### This photo booth is meant to work as a fun gadget people can use in social events to take fun photos with friends or colleagues.
### The photo booth works with dropbox and will automatically upload your pictures to chosen dropbox folder.


## Table of Contents

1. [Hardware](#hardware)
2. [Software](#Software)
3. [installation](#installation)
4. [setup](setup)
5. [Licens](#Licens)
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
    
    
   ## setup
   
   1. Start the setup with downloading the repository from github: https://github.com/herms97/photoBooth
  
   2. Set up your dropbox account
   
     2.1 First step is to create an account at DropBox - you do not have to pay for an account, do not worry. 
     2.2 Second step is to locate the folder called ‘dropbox-uploader’ that should be included when pulling / cloning from our github.
        Note: You may have pulled or cloned the project to a specific folder, make sure when changing directory that you know where the           dropbox-uploader is located.
        Go into cmd (command window) and type:
        
1. cd dropbox-uploader 
2. LS
    (the command ls, will list files in the folder you are located. You do not have to do this, but you will then see that the script         dropbox_uploader.sh is inside the folder dropbox_uploader).

    Simply run the script by typing: ./dropbox_uploader.sh
    
     If this dont work, type: chmod +x dropbox_uploader.sh
     
     This will allow you (give permission) to execute the file.


    






