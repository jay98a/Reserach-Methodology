# A Survey on 5G Mobile Connectivity Systems and its Prospects on Communication

# Introduction
The fifth-age innovation of media transmission prevalently known as 5G is perhaps the most arising research area nowadays. 5G can be generally public associated with IoT gadgets. It is expected to have a significant change in cellular innovation, like the previous 4G which is been utilized today and had an enormous significant change which has adpated backward compatibility. It likewise makes it workable for much new application which requires an exceptionally less lag for client experience like Mixed Reality, Internet of Things (IoT). According to various reports, the 5G is driving worldwide financial development which will be $ 13.1 Trillion worldwide as a monetary output, $ 22.8 Million new position made and $ 265 Billion worldwide 5G CAPEX and R&D every year throughout the following 15 years.

![616293](https://user-images.githubusercontent.com/65059545/129750239-8692f765-41d4-4323-b6ac-805d738a06fe.jpg)


In 5G, its activity is equivalent to the `past generation (4g)` however it utilizes a technique known as wavelength which undoubtedly have less jumbling and can in this manner convey more data at a lot higher velocities. `5G network configuration` portraying 5G and 4G organizations working together, with focal and nearby workers offering purchasers with speedier substance and low-inertness applications. The 'Radio Access Network' and the 'Center Network' are the two basic parts of a versatile network.

## Design

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
# Badges
![Conda](https://img.shields.io/conda/pn/conda-forge/python)
![CPAN](https://img.shields.io/cpan/l/Config-Augeas)
![Snyk Vulnerabilities for npm package](https://img.shields.io/snyk/vulnerabilities/npm/mocha)
![Ubuntu package](https://img.shields.io/ubuntu/v/ubuntu-wallpapers/bionic)

# References
* “Attention Required! | Cloudflare.” Omdia, omdia.tech.informa.com/OM004591/First-generation-5G-designs-highlight-critical-importance-of-modem-and-RF-integration-in-future-smartphones. Accessed 17 Aug. 2021.
* Cawley, Christian, and Christian Cawley. “How to Tether Any Smartphone to Linux for Mobile Internet.” MUO, 5 May 2020, www.makeuseof.com/tag/how-to-tether-your-smartphone-in-linux/. 
* “Configure Cellular Connections.” Ubuntu, ubuntu.com/core/docs/networkmanager/configure-cellular-connections. Accessed 17 Aug. 2021.
