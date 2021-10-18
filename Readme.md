# VSD Open PLL Workshop
## Introduction
The phase locked loop take in a signal to which it locks and can then output this signal from its own internal VCO. At first sight this may not appear particularly useful, but with a little ingenuity, it is possible to develop a large number of phase locked loop applications.

## Block Diagram of PLL
## Literature review and architecture design theory points
1. Design of Analog CMOS Integrated Circuits Behzad Razavi
2. Design of CMOS Phase Locked Loops Behzad Razavi

## Theory and Fundamental Concepts
1. CMOS and  Transistor Sizing
2. Control System Feedback Loop
3. IC Fab process
4. Euler path

## Setting up Linux Environment
Download the latest version of Virtual Box from the following link:
https://www.virtualbox.org/
After installation it will look somewhat like this:
![image](https://user-images.githubusercontent.com/58599984/137799120-6b9eb544-bccc-48b9-8e44-99d417506a08.png)
Download the Ubuntu Disk Image:
https://ubuntu.com/download/desktop
Create a new machine:
![image](https://user-images.githubusercontent.com/58599984/137799330-77062e35-35fe-44bc-bc6f-aa348c28f879.png)
Follow the steps hereafter.

After complete installation the Ubuntu window looks like this:
![image](https://user-images.githubusercontent.com/58599984/137799601-0bc2c1de-46ff-4fdc-9650-45f808ed0766.png)

## Installations
### Git
Open terminal and run:
```
sudo apt-get install git
```
Then do:
```
git clone https://github.com/parasgidd/avsdpll_3v3.git
```

## eSim
Install eSim and foolow steps from here:
https://esim.fossee.in/downloads

## Magic
Run following Commands in the terminal:
git clone git://opencircuitdesign.com/magic
'''
cd magic
sudo ./configure
sudo make
sudo make install
'''



