+++
title = "A Guide to Flashing Custom ROMs [Android]"
slug = "Flashing Custom ROMs 101"
date = "2018-02-25T00:00:00"
description = "Sick and tired of the bloatware on your current OEM ROM. Head over and learn how to flash custom ROMs."
author = "RohanVTK"
+++

(This blog starts of with a warning: Although the process is super easy and there hardly is a chance that you will brick your device during the process but do consider it)

The guide would be inclined more towards Xiaomi devices as I own one and have worked with it. But, all other devices follow the same process, so do give it a read.

To start off with, you should have a unlocked bootloader.
For Xiaomi devices refer to the following link : https://en.miui.com/unlock/
Follow the process and you'll surely have an unlocked bootloader in no time.
(Although it might take some time for Xiaomi to process your request but thereafter it's a really fast process)

Download ADB(Android Debug Bridge) and Fastboot files from this link: http://rootjunkysdl.com/files/?dir=Adb%20Fastboot%20Files
A .zip file for Windows will be downloaded. Extract these files to a folder.

Next, download twrp recovery file. Make sure that the twrp file is downloaded from here: https://twrp.me/Devices/

Place this file inside the folder created after extraction.

Make sure that the ADB, fastboot, recovery file and the rest of the files are inside the same folder.

Now download a ROM of your choice. (I personally use AOSP Extended ROM, it's pretty stable and is really performant when compared to other ROMs).
Link to AOSP Extended: https://www.aospextended.com/

Now open up the command prompt on Windows with adminitrator priviliges.
(To do this press the Windows key on your keyboard and search 'cmd' right click when command prompt comes up and chose 'Run as Administrator')
Now go the directory where the files you downloaded have been stored.
    if you don't know how to use Command Prompt
        'cd <dirname>' is use to go up that directory
        'cd..' is used to go down one directory


Finally pick your phone up and go to the fastboot mode, two methods have been listed below use any:
1. Reboot to Bootloader ->(Hold Power + Volume down)
2. Connect your phone to the PC after enabling the ADB debugging mode in the developer settings
    *type 'adb devices' if your device shows up then,
    *type 'adb reboot-bootloader'

Now to check that your device has entered the fastboot mode and is connected to the system(connect your phone to the system if you followed method 1)
    *type-in 'fastboot devices' if your device shows up then,
    *type-in 'fastboot flash recovery <nameOfTheRecoveryFile.img>'

Flashing would be done within a few minutes.

Congratulations!
You have completed the most difficult part of the process.

Moving on. 
    *type-in 'fastboot boot <nameOfTheRecoveryFile.img>'

Now the TWRP recovery opens up.

Transfer the ROM & Gapps file to the phone storage and click on install in TWRP recovery.
You will see the .zip files. 
First, you need to install the ROM and thereafter install the Gapps.
After completing the process make sure to clear the Dalvik Cache and Cache memory.

Reboot the Device.
Now you have a phone with a CUSTOM ROM of your own choice with no bloatwares.



===
If during the process you encoutered any issues do look up your issues on XDA or else Google your issues, you'll surely find a solution.
If you enjoyed reading this article do let me know by tweeting to me on my twitter-handle @RohanVTK. Your input will highly appreciable as well.
If you encouter any dead links do tweet about it the links will be updated.
