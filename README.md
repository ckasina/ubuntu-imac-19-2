# Ubuntu/Linux installed + running on Mac!

👾 How I installed Ubuntu 22.04 LTS on the 2019 iMac 21.5" 👾

I made this tutorial since for various sections of this process, since a lot of tutorials (whilst they do give detailed instructions) they're not forwards compatible with breaking changes both Apple and the Ubuntu open source community have made / will make. Which increase the difficulty of getting Ubuntu to run smoothly on Mac.

<br />

### `The usual "don't blame me if this goes wrong!" text (please don't though 🥲):`

<br />

**DISCLAIMER**: Whilst I'll provide universal instructions to install this on other flavours of Ubuntu + other types of Macs, I can only vouch for this working fully on the **Ubuntu 22.04 LTS** on the **2019 iMac 21.5"**

**DISCLAIMER 2**: Make sure you backup all of your data before attempting this, if you're unsure about any step in this tutorial then do further research or seek advice from a professional. **I do not accept any responsibility for any data loss or the loss of function of your computer.**

<br />

... With that said, let's continue with the tutorial! :)

## Prerequisites

- Some form of Mac (MacBook, iMac, Mac Mini etc)
- External media (e.g. USB thumb drive) to flash the iso file to

## Partitioning your Mac storage drive

You will need to partition your Mac storage for both the actual Ubuntu installation, and the _'swap space'_ partition for Ubuntu (if you don't know what _swap space_ is please read [here](https://help.ubuntu.com/community/SwapFaq)!)

Follow these steps:

1. Open Disk Utility on your Mac (this can be found in Launchpad or by using Spotlight Search), you should see a screen like this:

   ![Disk Utility Window](./screenshots/disk-utility/disk-utility-screenshot-1.png)

2. Select the **outer** Macintosh HD **container** (should say 'volumes' next to it) and then click the 'Partition' button in the top right section, you'll be greeted with this popup:

   ![Disk Utility Window - Partition Popup](./screenshots/disk-utility/disk-utility-screenshot-2.png)

3. Click the + button underneath the partition pie chart, and choose **'Add Partition'**, resize to however much space you'd like to allocate to Ubuntu (a minimum of 15GB is ideal), and set the format type to **"MS-DOS (FAT)"** (this will be changed later), make sure you set the name to something identifiable, like "Ubuntu".

   ![Disk Utility Window - How to partition GIF](./screenshots/disk-utility/disk-utility-screenshot-3.gif)

   (You'll notice I didn't resize the partition in this GIF, this is just an example to show how to partition, the Mac used in the recording doesn't have a lot of free storage space left)

   <br />

4. Repeat the same process as step 3 but instead this will be for your **'swap space'** partition, read [here](https://help.ubuntu.com/community/SwapFaq) if you're unsure what swap space is.

   In short, it's like virtual RAM for if the system runs out. As such, you should ideally allocate the same size as your RAM to your swap patition. So if your Mac has 16GB of RAM, then your swap space should have 16GB worth of storage space.

   Format as MS-DOS (FAT) as seen in step 3 and name it something identifiable like "SWAP"

## Creating bootable media

You will need 2 iso file(s):

- **An Ubuntu iso file**: [Official Ubuntu Download](https://ubuntu.com/download/desktop) (you may try this with other flavours of Ubuntu at your own discretion)

- **rEFInd iso file**: [rEFInd ISO Download](https://etcher.balena.io/) rEFInd is a boot manager utility / bootloader with support for Mac platforms, allowing you to boot from Mac / Ubuntu _(and even Windows!)_. We will install this using bootable media **AFTER** the Ubuntu installation since in most cases Ubuntu's GRUB bootloader overrides the MacOS default bootloader.

<br />

You will also need:

- A USB flash drive / other external storage hardware to boot from temporarily

- Software to flash the iso's onto a USB flash drive (I recommend [Balena Etcher](https://etcher.balena.io/))

<br />

![Screenshot of Balena Etcher interface](./screenshots/etcher/etcher-screenshot.png)

Once you've opened Etcher you'll be greeted with the above screen. Then follow these steps:

1. Click _'Flash from file'_, select the **Ubuntu** iso file you've downloaded and confirm.

2. Click _'Select target'_, select the USB flash drive you wish to flash the iso to _(be extremely careful here! Whichver device you choose to flash to will have its current contents **permanently erased**)_.

3. Click _'Flash!'_, the process of flashing the ISO to the USB should start and you'll have to wait, dependent on the speed of your computer this may take a bit of time (on average ~7 mins) so make yourself a coffee then come back! 😃

4. Once the process has finished, **safely** eject your USB then move onto the next section!

## Installing Ubuntu (_`the exciting part!!!`_)
