# A Survey on 5G Mobile Connectivity Systems and its Prospects on Communication

# Introduction
The fifth-age innovation of media transmission prevalently known as 5G is perhaps the most arising research area nowadays. 5G can be generally public associated with IoT gadgets. It is expected to have a significant change in cellular innovation, like the previous 4G which is been utilized today and had an enormous significant change which has adpated backward compatibility. It likewise makes it workable for much new application which requires an exceptionally less lag for client experience like Mixed Reality, Internet of Things (IoT). According to various reports, the 5G is driving worldwide financial development which will be $ 13.1 Trillion worldwide as a monetary output, $ 22.8 Million new position made and $ 265 Billion worldwide 5G CAPEX and R&D every year throughout the following 15 years.

![616293](https://user-images.githubusercontent.com/65059545/129750239-8692f765-41d4-4323-b6ac-805d738a06fe.jpg)


In 5G, its activity is equivalent to the `past generation (4g)` however it utilizes a technique known as wavelength which undoubtedly have less jumbling and can in this manner convey more data at a lot higher velocities. `5G network configuration` portraying 5G and 4G organizations working together, with focal and nearby workers offering purchasers with speedier substance and low-inertness applications. The 'Radio Access Network' and the 'Center Network' are the two basic parts of a versatile network.

# Working 


# Design

Some commands to connect any computer to a mobile network are as under:

To connect to mobile network from computer, you will need a linux operating system (IOS Devices).
1. Open Settings from your mobile
2. Go to Personal Hotspot

```
sudo apt install libimobiledevice6
eth0 or eth1 - Look for USB teathering
```

Now, You have sucessfully connected to the IOS network

To connect to mobile network from computer, you will need a linux operating system (Android Devices).
1. Connect usb cable to the computer
2. Click allow 
3. Go to settings and turn on USB tethering 
4. Check for ip adresss using `ifconfig` 

Type the below command in the terminal

```
usb0
```

Now, You have sucessfully connected to the Android network


## Configuring Connections on Linux Operating System

To configure your mobile device with the computer you need to follow the following commands:
1. Install Modem Manager
2. Check if the modem is detected or not
3. List the detailed information of the modem. (This will show hardware, system, Numbers, Status, Modes, Bands, IP, SIM, Bearers)
4. If the sim has pin locking enabled then we need to send `sim index`. In this case it is `0`. For disabling the pin locking, change the sim index.
5. The next step is adding cellular connections with `GSM`.
6. Finally, we will add `WWAN connection` to our state.

The commands of the  whole process is given below:

```
$ snap install modem-manager
$ sudo modem-manager.mmcli -L
$ sudo modem-manager.mmcli -m 0
$ sudo modem-manager.mmcli -i 0 --pin=<PIN>
$ nmcli c add type gsm ifname <interface> con-name <name> apn <operator_apn>
$ nmcli r wwan on
sudo nmcli c add type gsm ifname '*' con-name <name> apn <operator_apn>
$ nmcli r wwan off
$ nmcli c modify <name> connection.autoconnect [yes|no]
$ nmcli c down <name>
$ nmcli c add type gsm ifname <interface> con-name <name> apn <operator_apn> username <user> password <password> pin <PIN>

```
# Proposed Methodology

It is appropriately said in that it will be truly hard to limit the clients with high portability to low rates and other with high rate in light of the fact that it will be exceptionally difficult at mmWave frequencies to do handoffs since the sending and the getting radiates must be adjusted to convey. Also, as depicted in that mmWave is generally encouraging to use for the 5G network on account of the great information rates be that as it may, it makes it more unpredictable at the base station to deal with every one of the solicitations.. Unmistakably, it tends to be seen that there is a great deal of space for improvement before the 5G can be industrially be dispatched for most of the shoppers and every one of the clients taking benefit of it. The help of portability to the clients is turning out to be more troublesome with the networks proceeds to densify and heterogeneity increments. 


![Capture](https://user-images.githubusercontent.com/65059545/129929551-c02d7764-7fe9-4921-a5da-3c98c849c25e.PNG)


In any event, when Tactile Internet comes into the image, in which people may remotely control genuine and virtual objects, won't be accomplished except if monstrous framework plan obstructions are survived. For people to cooperate with anything from nature to any framework the reaction time ought to be pretty much as low as 100ms, 10ms, or 1ms for hearing and visualizing separately. As far as network, the greater part of the papers examined above have their own specific manner for the 5G mmWave band availability due to the complications looked in it because of the essential idea of mmWave as being exceptionally powerless to blockage, with such a large number of obstructions in the middle of the quality decreases radically.

Basically the same as 5G remote correspondence benefits the drones have as of late pulled in a ton of interest for their capacity to play out an assortment of errands going from transportation of things to clients, logical exploration, to notice or gather information about imperiled species, or in pivotal military tasks. At the point when distant circumstances are viewed as these robots consummately fit in because of their capacity of controller and reach to arrive at these spots.

For placement of drones, the following formula will come into use:

![drone_formula](https://user-images.githubusercontent.com/65059545/129927850-bdf684a8-1054-4740-a048-07082b9cdc18.PNG)

The below choice factors permit us to characterize which targets are covered by each allotted drone:

![drone_formula_1](https://user-images.githubusercontent.com/65059545/129927707-4430d93d-1654-4308-a603-9cecc327ebb0.PNG)

(x,y,h) is coordinate placement of the drone.



# Badges
![Conda](https://img.shields.io/conda/pn/conda-forge/python)
![CPAN](https://img.shields.io/cpan/l/Config-Augeas)
![Snyk Vulnerabilities for npm package](https://img.shields.io/snyk/vulnerabilities/npm/mocha)
![Ubuntu package](https://img.shields.io/ubuntu/v/ubuntu-wallpapers/bionic)

# References
* “Attention Required! | Cloudflare.” Omdia, omdia.tech.informa.com/OM004591/First-generation-5G-designs-highlight-critical-importance-of-modem-and-RF-integration-in-future-smartphones. Accessed 17 Aug. 2021.
* Cawley, Christian, and Christian Cawley. “How to Tether Any Smartphone to Linux for Mobile Internet.” MUO, 5 May 2020, www.makeuseof.com/tag/how-to-tether-your-smartphone-in-linux/. 
* “Configure Cellular Connections.” Ubuntu, ubuntu.com/core/docs/networkmanager/configure-cellular-connections. Accessed 17 Aug. 2021.
* Simsek, Meryem, et al. "5G-enabled tactile internet." IEEE Journal on Selected Areas in Communications 34.3 (2016): 460-473.
* Zorbas, Dimitrios, et al. "Optimal drone placement and cost-efficient target coverage." Journal of Network and Computer Applications 75 (2016): 16-31.
