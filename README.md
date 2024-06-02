# Raspberry-Pi-OpenPLC-with-Modbus
Creating a PLC with a Raspberry Pi, OpenPLC, and Modbus and seeing how it looks over the network.

### Table of contents

1. [Introduction](#introduction)
2. [Getting Started](#starting)
3. [Software Installation](#software)
4. [Breadboarding](#breadboard)
5. [palcehodler](#assessment)
6. [placeholder](#summary)

## Introduction <a name="introduction">
In this Project, I will use a Raspberry Pi running OpenPLC to create a switch to turn on and off an LED. I will then use Modbus to control the PLC (Raspberry Pi) over the network. I will also use (insert program) to monitor the activity between Modbus and the PLC.

## Getting Started <a name="starting">
We will need a Raspberry Pi, a project breadboard, an LED, a couple of jump wires, a 220 ohm resistor, two push buttons, and a computer. I bought this from Amazon as it had all the necessary items.   
[Starter Kit for Raspberry Pi](https://www.amazon.com/FREENOVE-Ultimate-Raspberry-558-Page-Detailed/dp/B06W54L7B5/ref=sr_1_2?crid=137OMN2ITGV7Z&dib=eyJ2IjoiMSJ9.GZW428gjohLopQ4YjAL731KQlescXYe9p8UTtopiUVObrhS8zyO8TdGjMn0GaHB9i73Y5sl1RAIQ5ZBbgfnqsscUse9cfc0f0oSpxE2e2qAWFEvjztiRzOR_F9WexFCJoVMQeRvJc8ATG3jJLktPVzfIvX99O1t_9gQsXjk4CG4BrUFIV9jLh5Zepu05XoVcfOq5WKL2pdHLW2tAs6CqcLs34oHkRyw6IlbnukW7dHCSsx4h-0AOcm71h3F71mhdmPSAVVC3gso0o7oZF0Q9Kh8YGxceL6Rlg2MdZQUtDnw.FqbyPBW7yhmTjdwOh8kxuP8jc__tzGTqbGzE1V07lxw&dib_tag=se&keywords=Freenove+Ultimate+Starter+Kit+for+Raspberry+Pi+5+4+B+3+B%2B+400%2C+558-Page+Detailed+Tutorial%2C+Python+C+Java+Scratch+Code%2C+223+Items%2C+104+Projects&qid=1717290931&s=electronics&sprefix=freenove+ultimate+starter+kit+for+raspberry+pi+5+4+b+3+b%2B+400%2C+558-page+detailed+tutorial%2C+python+c+java+scratch+code%2C+223+items%2C+104+projects%2Celectronics%2C280&sr=1-2)

## Software installation <a name="software">
Let's start by installing the OpenPLC runtime, OpenPLC editor, and Radzio Modbus Master Simulator. Don't worry; it's straightforward.

We will need to install the OpenPLC editor on your computer, and you can follow the instructions for your operating system with this video.  
[Installing OpenPLC Editor](https://youtu.be/iC5s4CEiOB4?si=wJh1vriMxQ14dKNB)

We will need to install OpenPLC Runtime on our Raspberry Pi. The installation process is described in this video.  
[Installing OpenPLC Runtime](https://youtu.be/Il0bCK5Luto?si=YuJfXPOuYSHyYUJl&t=669)

Radio Modbus Master Simulator is also very straightforward and does not require an installation as it runs as a portable program. The download link can be found here.  
[Modbus Master Simulator](https://en.radzio.dxp.pl/modbus-master-simulator/)

## Breadboarding <a name="breadboard">
Now that we have all the necessary software, it is time to connect everything to the breadboard and create our switch to turn an LED on and Off. Here is a 
![circuit](https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/cca5c8a6-d061-4761-975d-6f986cfde367)
![93cuu016](https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/c70b7871-b893-4320-91ec-0fe224ca756e)
