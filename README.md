# Ubuntu/Linux installed + running on Mac!

👾 How I installed Ubuntu 22.04 LTS on the 2019 iMac 21.5" 👾

I made this tutorial since for various sections of this process, since a lot of tutorials (whilst they do give detailed instructions) they're not forwards compatible with breaking changes both Apple and the Ubuntu open source community have made / will make. Which increase the difficulty of getting Ubuntu to run smoothly on Mac

**DISCLAIMER**: Whilst I'll provide universal instructions to install this on other flavours of Ubuntu + other types of Macs, I can only vouch for this working fully on the **Ubuntu 22.04 LTS** on the **2019 iMac 21.5"**

## Prerequisites

- Some form of Mac (MacBook, iMac, Mac Mini etc)
- External media (e.g. USB thumb drive) to flash the iso file to

## Creating bootable media

You will need 2 iso file(s):

<br />

- **An Ubuntu iso file**: [Official Ubuntu Download](https://ubuntu.com/download/desktop) (you may try this with other flavours of Ubuntu at your own discretion)

- **rEFInd iso file**: [rEFInd ISO Download](https://etcher.balena.io/) rEFInd is a boot manager utility / bootloader with support for Mac platforms, allowing you to boot from Mac / Ubuntu _(and even Windows!)_. We will install this using bootable media **AFTER** the Ubuntu installation since in most cases Ubuntu's GRUB bootloader overrides the MacOS default bootloader.

<br />

You will also need:
<br />

- A USB flash drive / other external storage hardware to boot from temporarily

- Software to flash the iso's onto a USB flash drive (I recommend [Balena Etcher](https://etcher.balena.io/))

<br />

![Screenshot of Balena Etcher interface](./screenshots/etcher/Etcher%20Screenshot.png)

Once you've opened Etcher you'll be greeted with the above screen. Then follow these steps:

1. Click _'Flash from file'_, select the **Ubuntu** iso file you've downloaded and confirm.

2. Click _'Select target'_, select the USB flash drive you wish to flash the iso to _(be extremely careful here! Whichver device you choose to flash to will have its current contents **permanently erased**)_.

3. Click _'Flash!'_, the process of flashing the ISO to the USB should start and you'll have to wait, dependent on the speed of your computer this may take a bit of time (on average ~7 mins) so make yourself a coffee then come back! 😃

4. Once the process has finished, **safely** eject your USB then move onto the next section!
