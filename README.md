# Ragnarok rocket
---
### General

https://github.com/joseph-elf/RagnarokRocket/assets/61538081/3cf62bc8-52d9-4bc3-b385-68cddac05cf4


---
### Propulsion

A mix of Sugar, Potassium Nitrate and Iron oxyde to power the rocket. This mix is stable and easy to prepare, it is possible to melt it and cast it into the desired shape.

For the first prototype, a simple motor in iron is manufactured.
Due to overpressure, the motor exploded; a 1 centimeter thick iron plate has completely disintegrated.

<img height="300" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/1d8848b7-3b77-49f6-ada5-e67be75eacc0">


A prototype of 3D printed motor is experimentated, the motor melted due to a slow combustion ( caused by an under pressure ) :

<img height="300" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/6ac2a370-f8e2-45cb-ae06-7490f1a6a310">
<img height="300" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/e81200f0-586f-4a3e-bf93-bbbbc2657d44">



---
### Electronic

<img align="right" width="250" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/e87d69b7-ca00-4980-9aa1-b9f5d912ddcf">

#### 1st prototype

A computer composed of two independants PCB manages the flight of Ragnarok I :

* One measures altitude using a BMP180 and triggers parachute ejection through the activation of a relay.
* One measures acceleration (MPU6050) and altitude, save them into the EEPROM memory of an arduino and is able to communicate it to a computer using a bluetooth connection.


<br />
<br />
<br />
<br />

#### PCB printing

<img height="250" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/a3a49132-ee9e-4d7a-a352-18403606ebd3">
<img height="250" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/81af55c5-d59a-495a-b1f6-c7635de01876">

In order to improve reliability and to learn how to use PCBs, the previous recovery chip is engraved.

#### Data collector prototype
<img height="250" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/92838d71-0fa2-4288-84bc-9909311398d4">

* Arduino nano manage data flux and save it into its EEPROM.
* BMP 180 measures pressure (and so altitude).
* MPU6050 measures acceleration and rotation.
* NEO-6M use the GPS signal to recover position and velocity.
* HC12 send all data on 433MHz and receive instructions from the ground.

<img align="right" height="350" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/be9730b2-278d-46ca-8c6f-d8431c5484e0">

#### Flight Control Computer

A Raspberry Pi is linked to a HC12 module to recover flight data and send control sequence. The computer is portable and autonomous.
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<img align="right" height="350" src="https://github.com/joseph-elf/RagnarokRocket/assets/61538081/906ee7c8-555c-48c9-8391-a8bfe31b9b46">

#### Launch Remote Control
A little remote send the launch signal to the fire mechanism. HC12 is again used. To avoid false launch signal, the remote is bilateraly connected and has to send a precise "launch sentence".

---

### Design
