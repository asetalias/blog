+++
title = "A Guide to Flashing Custom ROMs [Android]"
slug = "custom-rom-101"
date = "2018-02-25T00:00:00"
image = "img/rohanvtk/csrom.jpg"
description = "Sick and tired of the bloatware on your current OEM ROM. Head over and learn how to flash custom ROMs."
author = "RohanVTK"
tags = ['Smartphone', 'Customization','Android']
categories = ['Android']
+++

**_This blog starts off with a warning: Although the process is super easy and the chances of your phone getting bricked(useless) are negligible but, it's my responsibility to make you aware of it_**

The guide would be inclined more towards Xiaomi devices as I own one and have worked with it. But, all other devices follow a similar process, so go ahead and give it a read.

* To start off with, you should have an unlocked bootloader.

    **_For Xiaomi devices refer to the following link : [Click-Here](https://en.miui.com/unlock/)_**

    Follow the process and you'll surely have an unlocked bootloader in no time.
*(Although it might take some time for Xiaomi to process your request but thereafter, it just takes a couple of minutes)*

* **_Download ADB(Android Debug Bridge) and Fastboot files from this link: [Click-Here](http://rootjunkysdl.com/files/?dir=Adb%20Fastboot%20Files)_**

    A `.zip` file will be downloaded. Extract these files to a folder. (If you're using Windows all the drivers will be installed automatically)

* **_Next, download twrp recovery file(a `.img` file). Make sure that the twrp file is downloaded from here: [Click-Here](https://twrp.me/Devices/)_**

Place this file inside the folder created in the above step.

**_Make sure that the ADB, fastboot, recovery file and the rest of the files are placed inside the same folder._**

* Now download a ROM of your choice. *(I personally use AOSP Extended ROM, it's pretty stable and is really performant when compared to other ROMs).*

    **_Link to AOSP Extended: https://www.aospextended.com/_**

* Also, download google apps .zip file.

    **_Link to OpenGapps: https://opengapps.org/_**

* Now open up the command prompt on Windows with **_adminitrator priviliges_**.

    _(To do that, press the `Windows key` on your keyboard and search 'cmd', right click when command prompt comes up and chose 'Run as Administrator')_

* Now go the directory where the files you downloaded have been stored.
    if you don't know how to use Command Prompt

> `cd <dirname>` is use to go up a directory

> `cd..` is used to go down one directory

Enable Developer Options on your phone and enable USB-Debugging. To know more [click-here](https://www.google.com/search?rlz=1C1CHBD_enIN850IN850&ei=5L_7XI0insTPuw-E0JiIAQ&q=how+to+enable+developer+option+in+android&oq=how+to+enable+developer+option+in+android&gs_l=psy-ab.3..35i39j0j0i20i263j0l4j0i30l3.2954.3254..4277...0.0..0.140.265.0j2......0....1..gws-wiz.......0i71j35i304i39j0i13j0i13i30.0E6WUqzOMPo)

Finally, enter fastboot mode on your phone. How-to methods have been listed below(Use any one of the following):

1. Reboot to Bootloader ->(Hold Power + Volume down)    {*_For Xiaomi Devices_*}

2. Connect your phone to the PC after enabling the ADB debugging mode in the developer settings

> type `adb devices` when your device shows up 

> type `adb reboot-bootloader`

----

Now to check that your device has entered the fastboot mode and is connected to the system _(connect your phone to the system if you followed method 1 mentioned above)_

> type-in `fastboot devices` if your device shows up then,

> type-in `fastboot flash recovery <nameOfTheRecoveryFile.img>`

Flashing would be done within a few minutes.

*So, the tough part's over.* :D

Moving on.

> type-in `fastboot boot <nameOfTheRecoveryFile.img>`

Now the TWRP recovery opens up. _(You might have to wait a few seconds)_

Transfer the ROM & Gapps file to the phone storage and click on install in TWRP recovery.

Find the .zip files.

Install the ROM and thereafter install Google Apps from the .zip file.

_After completing the process make sure to clear the Dalvik Cache and Cache memory._

_Reboot the Device._

**_Congratulations! Now you have a phone with a CUSTOM ROM of your own choice with no bloatwares._**

______

*If during the process you encoutered any issues, do look up your issues on XDA or else Google your issues, you'll surely find a solution.*

*If you found this article helpful, do let me know by tweeting to me on my __twitter-handle @RohanVTK__.*

*If you encouter any dead links do tweet about it, the links will be updated.*

