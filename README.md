# new-lab

## made in 2023 updated 2025

I had a good run of luck. One of my friends offered me two small servers, then other people started offering things, so I got a very nice lab built for almost nothing. I started with a 12-bay SuperMicro. I decided to get some SSDs, some m.2, and some normal 3.5's (as this is a 2u Super Micro). I ran this for about 1.5 years. It was given OMV bare metal on an SSD. I ran into the same issue i had with the other server where it would just randomly crash when doing anything with nessus, cloud things or kasm when this happen it would break docker totally, while i never fully figured this out i will assume it is a omv specfic issue so after round about the 20th format I got tired of fixng it and decide to go another route.


main supermicro 
![alt text](20211024_160607.jpg)



early setup of rack>
try one:
![alt text](20250317_113617.jpg)
try two:
![alt text](20210329_152832-1.jpg)

## Starting mikrotik

Starting a network:  seeing how I had the large server, I got a rack and decided to get some networking gear, but what? I decided to go with Supermicro. The network gear I went with is Supermicro and MikroTik, mostly for price but also due to the fact that I could use SFP+. This allowed me to use DAC or fiber. I went with fiber because the price at the time was cheaper, and 10 Gbps was the only thing a home user could get without some crazy connection or price. After getting all the gear, I realized at the last minute that the network would need wifi as well as a router. I did not take this into consideration. The one they would give us was cat-only, at least on the user side. This was a problem, so I did a fast order and grabbed up a Dell R720 and made this a hardware-only firewall. Mostly just for the fact that it was very cheap and I could put in some fiber cards.

I was not only new to Mikrotik, but I was also new to OPNsense, the firewall I had chosen to go with. I played around with around 10 or 11 of them. However, the more user-friendly OpenSense, I decided to go with this.


![alt text](sfp6.PNG)

![alt text](<network gear.JPG>)

![alt text](sfp2.PNG)  

![alt text](sfp3.PNG)

![alt text](sfp4.PNG)

![alt text](sfp5.PNG)

After a short time of learning curve area, I got the hardware down. Now I have my R720 and my setup. While this took a lot of power, it ran GREAT for two or so years.

I then decided to downgrade the power and upgrade the offline electric: I did this by getting two new batteries, and the old one only did 7 minutes for the full lab, enough to shut down but not run, so it bypassed our little 1-30 second offlines in the wintertime. So now I have three total batteries, 1 of 1 brand and 2 of another. The others are much, much better. My  main actual network, that's both  switch the level 2 and the level 3 are on one battery, one of the actual server "main server" is on the other, and the extra server (the old Dell R720) is on number three 


## Main firewall setup part2 (ms-01)

![alt text](<opnsense overview NEEDS EDIT.JPG>)

![alt text](<opnsense 2.JPG>)

Game setup for amp:
![alt text](<opn game rules.JPG>)

Working automated bans redirects and ddos prevention

![alt text](<does it work firewall bans-1.JPG>)

Forcing a guest out over a VLAN while using a VPN exit node.
![alt text](<guest out 1.5.JPG>)

![alt text](<guest out wg home.JPG>)

![alt text](<guest wifi only.JPG>)

![alt text](<wg guest setup.JPG>)

![alt text](<wg mullvad out only.JPG>)

![alt text](<wg wg.JPG>)


# Mini pc x2
![alt text](20210516_020900.jpg)
Fan Modification

![alt text](20230826_174046.jpg)


## Had a idea to conserve space

final setup:
from top to bottom:
I decided to place networking at the rear top, opposite the power.

 ![alt text](20250317_193507-1.jpg)

below on the shelf is the ms-01 the replacement for the dell firewall:

![alt text](Minisforum-MS-01-Front.jpg)

![alt text](Minisforum-MS-01-Back.jpg)

![alt text](Minisforum-MS-01-Internal.jpg)
1/4th shelf  that holds both the power brick and the ms-01: (for now)
![alt text](20251019_200946.jpg)

On the front:
![alt text](<top 01.jpg>)
![alt text](<top 02.jpg>)
![alt text](<top 03.jpg>)
![alt text](<top 04-1.jpg>)

side project for the modem (fiber)
![alt text](<modem rig.jpg>)

final cleanup 
before:
![alt text](<before sidewire.jpg>)
after:
![alt text](<after sidewire.jpg>)

and at the very top we have the junk top:
![alt text](<top junktop game rig.jpg>)
and the game rig:
![alt text](<top game rig.jpg>)

current rack overview:
![alt text](rack.jpg)


The current network topology is described in words.

![alt text](<network_diagram. words only.drawio.png>)

visualzation of network setup:
![alt text](current_network.drawio.png)

# General speed test on 10/100/1000 networking card:
![alt text](<speed 2.PNG>)

This concludes the physical setup. I’ll refer back to it when assigning VLAN IDs or discussing Proxmox in the future.