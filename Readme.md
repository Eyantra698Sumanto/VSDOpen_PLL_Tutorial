# VSD Open PLL Workshop
This repo contain all my documentation of the  "VSD Open PLL tutorial"

-----------------------------------------------------------------------------------------------------------------------------------------------
# Introduction
The phase locked loop take in a signal to which it locks and can then output this signal from its own internal VCO. At first sight this may not appear particularly useful, but with a little ingenuity, it is possible to develop a large number of phase locked loop applications.

# Block Diagram of PLL
![image](https://user-images.githubusercontent.com/58599984/137809342-e1060500-660e-4212-951b-47adc9b06ff0.png)

# Literature review and architecture design theory points
1. Design of Analog CMOS Integrated Circuits Behzad Razavi
2. Design of CMOS Phase Locked Loops Behzad Razavi

# Theory and Fundamental Concepts
1. CMOS and  Transistor Sizing
2. Control System Feedback Loop
3. IC Fab process
4. Euler path

# Setting up Linux Environment
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

# Installations
## Git
Open terminal and run:
```
sudo apt-get install git
```
Then do:
```
git clone https://github.com/parasgidd/avsdpll_3v3.git
```

# eSim
Install eSim and follow steps from here:
https://esim.fossee.in/downloads

# Magic
Run following Commands in the terminal:
git clone git://opencircuitdesign.com/magic
```
cd magic
sudo ./configure
sudo make
sudo make install
```
# Running eSim and Ngspice

## eSim Schematic of inverter example
![image](https://user-images.githubusercontent.com/58599984/137801190-d231140f-d7cc-4d09-bf5c-7ea701a569e0.png)
## Running Ngspice
```
cd /avsdpll_3v3/prelayout$
ngspice inv.cir
```
![image](https://user-images.githubusercontent.com/58599984/137800719-4022e45d-580d-4491-8d1c-2bd0842b61f3.png)
## Output Waveforms
![image](https://user-images.githubusercontent.com/58599984/137800823-dfd01f99-bffb-4a99-9d9d-e8d466ae1ba2.png)

# Prelayout
## PFD Design
![image](https://user-images.githubusercontent.com/58599984/137802291-905fe5c0-c849-476d-b887-3892ba66a1f9.png)
![image](https://user-images.githubusercontent.com/58599984/137804175-ec5c3a96-ce5b-43b6-9acf-7a042b6f0c5d.png)
![image](https://user-images.githubusercontent.com/58599984/137803982-d01ec0cc-3009-453c-84b0-a5d5759f27a4.png)


## Charge Pump 
![image](https://user-images.githubusercontent.com/58599984/137802034-14a9f0f7-fcc7-4cfe-ad53-17594d4c8283.png)
![image](https://user-images.githubusercontent.com/58599984/137804127-4431757f-2ca6-4188-99bb-141bea372b68.png)
![image](https://user-images.githubusercontent.com/58599984/137804085-c42f68ab-2ab4-4184-9539-b675fa68d82a.png)


## VCO
![image](https://user-images.githubusercontent.com/58599984/137802397-405da180-9bdd-439b-ac85-f7fb59a12b76.png)
![image](https://user-images.githubusercontent.com/58599984/137803903-f62f837a-1985-4b21-b3d1-16c47af1e5f2.png)
![image](https://user-images.githubusercontent.com/58599984/137803841-25743fa1-f2ab-47a2-94a9-78194b6b8c6d.png)

## freq_div
![image](https://user-images.githubusercontent.com/58599984/137803268-58e658e0-c078-486b-b16b-d5c16d28d823.png)
![image](https://user-images.githubusercontent.com/58599984/137803693-2758d866-10fe-4020-972d-23ebd89a1095.png)
![image](https://user-images.githubusercontent.com/58599984/137803737-4fdee911-eb47-4646-8dff-2f8c21d67e7b.png)


## PLL Prelayout
![image](https://user-images.githubusercontent.com/58599984/137803560-d809fcaf-de56-4957-8956-ceca47224643.png)
![image](https://user-images.githubusercontent.com/58599984/137803604-0f6e51ae-66e5-471c-8358-9bc270c9c51e.png)

# Physical Design Introduction
## Layout of Inverter
Run the following command to open Magic:
```
magic -T SCN6M_SUBM.10.tech
```
![image](https://user-images.githubusercontent.com/58599984/137804925-456124c5-572c-4967-aac0-be0c58751d5c.png)

## Layout of PFD
![image](https://user-images.githubusercontent.com/58599984/137805430-9c634f42-baca-4add-b448-5c845f06b344.png)
![image](https://user-images.githubusercontent.com/58599984/137807859-dbc755d1-730c-4431-bb40-1aca5880c734.png)
![image](https://user-images.githubusercontent.com/58599984/137807827-86f6ce04-5dc0-4848-aa8d-9f7ffa7a1f86.png)


## Layout of VCO
![image](https://user-images.githubusercontent.com/58599984/137805522-cda4d825-74c4-48ad-82c4-a6ee3a0d463c.png)
![image](https://user-images.githubusercontent.com/58599984/137807663-ac48bbf3-63e7-4ab8-a6ae-8ab6aefc3194.png)
![image](https://user-images.githubusercontent.com/58599984/137807626-a60550b6-363e-4f21-af4e-a2d4d8cbf64d.png)


## Layout of FreqDiv2
![image](https://user-images.githubusercontent.com/58599984/137805598-fbef718b-496c-409a-9ed5-9c768628f028.png)
![image](https://user-images.githubusercontent.com/58599984/137806722-d288680e-531a-4699-a1ee-4aee5b713a9b.png)
![image](https://user-images.githubusercontent.com/58599984/137806676-9c7a4cb8-e5f1-4171-aa4f-d469b09a9c23.png)


## Layout of FreqDiv8
![image](https://user-images.githubusercontent.com/58599984/137805681-dd68d1d5-dd36-471f-b9d9-44bd924e47bc.png)
![image](https://user-images.githubusercontent.com/58599984/137806952-15c646bf-e746-48da-82ec-2a9eb953c381.png)
![image](https://user-images.githubusercontent.com/58599984/137806882-601a216c-de48-4942-b68e-d6f786395147.png)


## Layout of mux21
![image](https://user-images.githubusercontent.com/58599984/137805764-7e073d29-ccb9-4744-bd42-84d0683a5eae.png)
![image](https://user-images.githubusercontent.com/58599984/137807540-fefee4f7-1f49-4bfd-959a-3c8d6c81f11e.png)
![image](https://user-images.githubusercontent.com/58599984/137807514-1532f8fe-bda1-4b0f-a29e-1fbc2ba27965.png)

## Final Layout of PLL
![image](https://user-images.githubusercontent.com/58599984/137808002-3792ab3e-71d8-4a63-9fac-dfc1fa886a32.png)
![image](https://user-images.githubusercontent.com/58599984/137808639-e36c0650-7b18-49ea-bc2c-0bd01f3314eb.png)
![image](https://user-images.githubusercontent.com/58599984/137810247-91623d29-4dd7-4f60-89f7-e19cb99e362d.png)

![image](https://user-images.githubusercontent.com/58599984/137810210-55674103-460b-4b67-bb56-675d14b9136b.png)

![image](https://user-images.githubusercontent.com/58599984/137810183-5e484849-894b-4c17-a705-3b7bdff30f94.png)

![image](https://user-images.githubusercontent.com/58599984/137810124-de262a92-f1fb-4f1f-840b-85c61d5883d3.png)

# Acknowlegment
I would like to thank Mr.Kunal Ghosh and Mr. Paras Gidd for the tutorial explained in the simplest way possible. It helped me to learn more about the PLL and layout design and simulations using Magic and Ngspice in a very easy and structured manner. 

# References
1. https://www.vlsisystemdesign.com/registration/<br>
2. https://vsdiat.com/<br>
3. https://github.com/parasgidd/avsdpll_3v3<br>
4. https://www.virtualbox.org/<br>
5. http://opencircuitdesign.com/magic/download.html<br>
6. https://esim.fossee.in/downloads<br>
7. https://www.electronics-notes.com/articles/radio/pll-phase-locked-loop/tutorial-primer-basics.php









