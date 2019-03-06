# orangepi-h6-ubuntu-base-minimal

Ubuntu 18.04 base minimal image tested on the Orange Pi One Plus

This is a follow up on the mainline kernel 5.0 for the H6 SBC:

* Mainline Kernel 5.0
* HDMI
* DVFS
* Gbps and fast ethernet


OS Img is available here (use 7z to unzip and burn to SD card with Win32DiskImager or Etcher):
https://mega.nz/#!NPoSkIyT!Ul1n_1WVklPXlR2nHQxEE356_2iM8WAWWm9AWNR08hg

  User: ubuntu     
  Pasw: ubuntu


|  SBC Dev Board sample  |   Orange Pi One Plus  |
|------------------------|-----------------------|
| kernel version         |      5.0.0 mainline   |
| gcc version            |      8.2.0            |
| display                |      hdmi             |
| graphical interface    |      CLI              |
| pmic                   |      axp806           |
| idle Temp ºC / freq    |  40 ºC / ~480 Mhz     |
| full Temp ºC / freq    |  78 ºC / 1.8 GHz      |
| RAM memory usage (avg) |      65  Mbytes       |
| i2c                    |      no               |
| spi                    |      no               |
| Camera                 |      no               |
| Wifi                   |      no               |
| BT                     |      no               |
| ethernet               |    100 MBit / 1 GBit  |
| issues                 | reboot = shutdown     |

You need *wget* and *curl* installed to grab the files in a Linux distro or use the **img** above.

Get the latest files by running (or seee below to fetch specific Release version files):


	wget $(curl -s https://api.github.com/repos/avafinger/orangepi-h6-ubuntu-base-minimal/releases/latest | grep -oP '"browser_download_url": "\K(.*)(?=")')


then

	Unzip the file and flash it to SD card (8GB) using




# Release v1.0

* minor fixes and optimizations (4K, journaling , heart-beat)
* DHCP enabled (default)

		user: ubuntu
		password: ubuntu


Get v1.0 files:

		wget $(curl -s https://api.github.com/repos/avafinger/orangepi-h6-ubuntu-base-minimal/releases | grep -oP '"browser_download_url": "\K(.*)(?=")' | grep v1.0)


Boot takes about 5 seconds or less depending on SD card in use. 
**Tip**: If you can't see anything on screen, type enter twice!


On first login:

	sudo apt-get update
	sudo apt-get dist-upgrade



**Tip**: You may need to update the file **resolver.conf** to reflect your network (DNS)

[![htop](https://github.com/avafinger/orangepi-h6-ubuntu-base-minimal/raw/master/img/htop.png)]

