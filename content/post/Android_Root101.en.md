+++
title = "A Guide to Flashing Custom ROMs [Android]"
slug = "flash_custom_rom"
date = "2018-02-25T00:00:00"
image= "https://github.com/rohanvtk/images-for-everybody/blob/master/andro_root%20(1).jpg"
description = "Sick and tired of the bloatware on your current OEM ROM. Head over and learn how to flash custom ROMs."
author = "RohanVTK"
tags = ['Smartphone', 'Customization']
categories = ['Android']
+++

**_(Warning: The following process might brick your device.)_**

* To start with, you should have an unlocked bootloader.

    **_For Xiaomi devices refer to the following link : [Click-Here](https://en.miui.com/unlock/)_**

    Follow the process to unlock your phone's bootloader.
*(Xiaomi takes 3 days to process your request to unlock your bootloader.)*

* **_Download ADB(Android Debug Bridge) and Fastboot files from this link: [Click-Here](http://rootjunkysdl.com/files/?dir=Adb%20Fastboot%20Files)_**

    A .zip file for Windows will be downloaded. Extract these files to a folder.

* **_Next, download TWRP recovery file(a `.img` file). Make sure that the twrp file is downloaded from here: [Click-Here](https://twrp.me/Devices/)_**

Place this file inside the same folder created in the previous step.

* Download a ROM of your choice.

    **_Link to AOSP Extended: https://www.aospextended.com/_**

    **_Link to Resurrection Remix: https://www.resurrectionremix.com/_**

    **_Link to Pixel Experience: https://download.pixelexperience.org/_**

* Download google apps .zip file as well. (Skip this step for Pixel Experience ROM)

    **_Link to OpenGapps: https://opengapps.org/_**

* Now open up the command prompt on Windows with **_adminitrator priviliges_**.

    _('WindowsKey + R'. Type in 'cmd'. Hit 'Ctrl+ Shift + Enter')_

* Open up the folder in which you downloaded all these files.

Open CMD in that directory.

![Easy Trick to open CMD](https://github.com/rohanvtk/images-for-everybody/blob/master/andro_root%20(3).jpg#center)

Open up CMD already pointing to that folder by typing in 'cmd' in the address bar i.e. where 'Quick access' is written in this image.

> `cd <dirname>` is used to enter the mentioned directory <dirname>

> `cd ..` is used to go down one directory

Finally, pick up your phone and enter fastboot mode (two methods have been listed below use any):

1. Method One

    Reboot to Bootloader ->(Hold Power + Volume down) 
    (for Xiaomi Devices. Try Holding Power + Volume Up Button if this doesn't work.)

2. Method Two
    
    Connect your phone to the PC after enabling the ADB debugging mode in the 'Developer Settings'. 
    To enable Developer Setting/Developer Options. Go to 'About Device' and tap on 'Build Number' 7 times. 
    (this procedure will vary with respect to device manufacturer and OS version)
    
    > type `ADB devices` if your device shows up then,
    
    > type `ADB reboot-bootloader`

To check whether your device has entered the fastboot mode or not _(connect your phone to your PC if you followed method 1 mentioned above)_

> type-in `fastboot devices` if your device shows up then,

> type-in `fastboot flash recovery <nameOfTheRecoveryFile.img>`

Flashing will take a few seconds.

*So, the tough part's over now.* :D

Moving on.

> type-in `fastboot boot <nameOfTheRecoveryFile.img>`

Now, the TWRP should open up.

![TWRP](https://github.com/rohanvtk/images-for-everybody/blob/master/andro_root%20(4).jpg#center)

That's what TWRP recovery looks like.

Transfer the ROM & Gapps file to the phone storage and click on install in TWRP recovery.

Find the .zip files.

Install the ROM followed by Google Apps from the .zip file.

_After completing the process make sure you clear the Dalvik Cache and Cache memory._

_Reboot the Device and wait, as the initial boot takes time._

![customromdone](https://github.com/rohanvtk/images-for-everybody/blob/master/andro_root%20(2).jpg#center)
______

**Au Revoir**

**RohanVTK** 

Connect with me on [Twitter](https://twitter.com/RohanVTK) | [LinkedIn](https://www.linkedin.com/in/rohan-verma-574821158/)