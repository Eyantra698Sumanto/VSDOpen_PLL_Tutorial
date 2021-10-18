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
```
cd magic
sudo ./configure
sudo make
sudo make install
```
## Running eSim and Ngspice

### eSim Schematic of inverter example
![image](https://user-images.githubusercontent.com/58599984/137801190-d231140f-d7cc-4d09-bf5c-7ea701a569e0.png)
### Running Ngspice
```
cd /avsdpll_3v3/prelayout$
ngspice inv.cir
```
![image](https://user-images.githubusercontent.com/58599984/137800719-4022e45d-580d-4491-8d1c-2bd0842b61f3.png)
### Output Waveforms
![image](https://user-images.githubusercontent.com/58599984/137800823-dfd01f99-bffb-4a99-9d9d-e8d466ae1ba2.png)

## Prelayout
### PFD Design
![image](https://user-images.githubusercontent.com/58599984/137802291-905fe5c0-c849-476d-b887-3892ba66a1f9.png)
![image](https://user-images.githubusercontent.com/58599984/137804175-ec5c3a96-ce5b-43b6-9acf-7a042b6f0c5d.png)

![image](https://user-images.githubusercontent.com/58599984/137803982-d01ec0cc-3009-453c-84b0-a5d5759f27a4.png)


### Charge Pump 
![image](https://user-images.githubusercontent.com/58599984/137802034-14a9f0f7-fcc7-4cfe-ad53-17594d4c8283.png)
![image](https://user-images.githubusercontent.com/58599984/137804127-4431757f-2ca6-4188-99bb-141bea372b68.png)
![image](https://user-images.githubusercontent.com/58599984/137804085-c42f68ab-2ab4-4184-9539-b675fa68d82a.png)


### VCO
![image](https://user-images.githubusercontent.com/58599984/137802397-405da180-9bdd-439b-ac85-f7fb59a12b76.png)
![image](https://user-images.githubusercontent.com/58599984/137803903-f62f837a-1985-4b21-b3d1-16c47af1e5f2.png)
![image](https://user-images.githubusercontent.com/58599984/137803841-25743fa1-f2ab-47a2-94a9-78194b6b8c6d.png)

### freq_div
![image](https://user-images.githubusercontent.com/58599984/137803268-58e658e0-c078-486b-b16b-d5c16d28d823.png)
![image](https://user-images.githubusercontent.com/58599984/137803693-2758d866-10fe-4020-972d-23ebd89a1095.png)
![image](https://user-images.githubusercontent.com/58599984/137803737-4fdee911-eb47-4646-8dff-2f8c21d67e7b.png)


### PLL Prelayout
![image](https://user-images.githubusercontent.com/58599984/137803560-d809fcaf-de56-4957-8956-ceca47224643.png)
![image](https://user-images.githubusercontent.com/58599984/137803604-0f6e51ae-66e5-471c-8358-9bc270c9c51e.png)







