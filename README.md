# Raspberry-Pi-OpenPLC-with-Modbus
Creating a PLC with a Raspberry Pi, OpenPLC, and Modbus and seeing how it looks over the network.

### Table of contents

1. [Introduction](#introduction)
2. [Getting Started](#starting)
3. [Software Installation](#software)
4. [Breadboarding](#breadboard)
5. [Programming with OpenPLC Editor](#openplc)
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
Now that we have all the necessary software, it is time to connect everything to the breadboard and create our switch to turn an LED on and Off. Below is a diagram of how I connected the LED to the Raspberry Pi.  
![circuit](https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/cca5c8a6-d061-4761-975d-6f986cfde367)

The Raspberry Pi GPIO pins are referenced using the IEC 61131-3 addressing. It's important to note that OpenPLC has allocated all the left-side (odd) pins as inputs and all the right-side (even) pins as outputs. Here is a Pinout of the inputs and outputs we will use for the OpenPLC editor. For the input side, push button 1 is connected to "%IX0.0," and push button 2 is connected to "%IX0.0." For the output side, the LED is connected to "QX0.0."      
![93cuu016](https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/c70b7871-b893-4320-91ec-0fe224ca756e)

## Programming with OpenPLC Editor <a name="openplc">
Now that we have our breadboard, let's create the program logic that OpenPLC will use to run on our Raspberry Pi. Pushbutton 1 will turn on the LED, and Pushbutton 2 will turn it off. We will use Ladder logic on the OpenPLC editor to create our program logic.  

Ladder logic was one of the first IEC 61131-3 programming languages. It was developed as a graphic representation for relay logic hardware circuit diagrams. The term "ladder" comes from the fact that the logic looks a little like a ladder, with a vertical power rail on the left side and a vertical ground rail on the right side. Then, a series of horizontal lines or "rungs" are wiring hardware components between the rails.

For my Ladder Logic I followed this video.  
[OpenPLC on Raspberry Pi with Modbus](https://youtu.be/iC5s4CEiOB4?si=wJh1vriMxQ14dKNB)  
![Screenshot 2024-06-01 193350](https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/ca09e21a-b0d3-441e-b57d-4b70c430e9ea)

You can follow the rest of the video on how to send the OpenPLC program we created to our Raspberry Pi.  
https://github.com/IzharSalvanaSyed/Raspberry-Pi-OpenPLC-with-Modbus/assets/156041933/756bfb64-7f62-4c03-b0ca-c8200366e39b

