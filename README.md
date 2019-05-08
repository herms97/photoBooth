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
    
    ## Setup
    Start the setup with downloading the repository from github: https://github.com/herms97/photoBooth
    






