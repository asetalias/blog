+++
title = "Getting Started With Flutter"
slug = "Getting-started-with-Flutter"
cover.image = "images/flutter.jpg"
date = "2019-06-05T00:00:00"
description = "Blog on how to setup Flutter from scratch."
disableComments = false
author = "Kaushlendra Pratap"
tags = ['Flutter','App-Dev','Android']
categories = ['Setup-&-Installation']
+++

[**Flutter**](https://flutter.dev/) is Google’s portable UI toolkit for building beautiful, natively-compiled applications for mobile, web, and desktop from a single codebase.


## More on Flutter...

According to me, Flutter has a very bright future ahead as Google is using Flutter for the development of their own apps. It has very expressive and Flexible UI and it is famous for its Native Performance. The main challenge is that cross-platform development can be problematic. In recent years we have seen the emergence of various mobile frameworks like **React Native** and **AngularJS** that help make it easier for the developers. But Google is like -:

![GIF](/blog/images/Challenge.gif#center)

Initially, flutter might look like a mix-up of various Google technologies and concepts however, this results in a powerful mobile framework. It's based on [Dart](https://dart.dev/guides), Google's in-house programming language, which makes Flutter even more special because it gives flutter access to the [Skia graphics Library](https://skia.org/) which is what Chrome uses.


I will be sharing the steps to install and setup Flutter in this blog. Let's get rolling!!



## Download the Flutter SDK

***For Window users -:***

1. You can download the SDK from [here](https://storage.googleapis.com/flutter_infra/releases/beta/windows/flutter_windows_v0.5.1-beta.zip)

2. Extract the zip file and place the contained flutter in the desired installation location for the Flutter SDK `(eg. C:\src\flutter;` do not install Flutter in a directory like `C:\Program Files\ that requires elevated privileges)`.

3. Look for the file  `flutter_console.bat` inside the `flutter` directory. Start it by double-clicking.


***For Mac users -:***

1.  For Mac users, You can download the SDK from [here](https://storage.googleapis.com/flutter_infra/releases/beta/macos/flutter_macos_v0.5.1-beta.zip)

2. Extract the file in the desired location, for example:

![Img](/blog/images/MAC-os.png#center)



3. After downloading the flutter SDK from one of the above links. Extract the download into a suitable folder and then add `bin` folder location to your path.


***For Linux Users-:***

1. For Linux users, the tar file can be downloaded from [here](https://storage.googleapis.com/flutter_infra/releases/beta/linux/flutter_linux_v0.5.1-beta.tar.xz)

2. Extract the file in the desired location, for example:

![File](/blog/images/linux.png#center)

3. After downloading the flutter SDK from one of the above links. Extract the download into a suitable folder and then add `bin` folder location to your path.


***Flutter Doctor***

After completing the process of downloading and adding the `bin` folder to the path, you can check the status of flutter by using the command

`flutter doctor`

The output would be like:

![output2](/blog/images/output.png#center)

I have the android studio and an ide (VS code--my preference) pre-installed.

You can install and download [**Android Studio**](https://developer.android.com/studio/).


### Setting up your Mobile 

Connect your device to the pc and use the following command to verify that flutter recognizes your device:

`flutter devices`

The output would be something like this:

![output](/blog/images/flutter_devices.png#center)


### Final Steps...

I hope you have done each and every step Perfectly. If so, **VOILAA!!** you can start your first project now.

- Open Android studio and select **File > New Flutter Project**

![New_project](/blog/images/studio.png#center)

- Select *Flutter Application* and click Next.

- Enter your Project details and install Flutter SDK if you have not installed it.

- Setup your domain and click **Finish**

![Studio](/blog/images/studio2.png#center)


Congratss!!! You can now start developing your app in Flutter now. I will be talking about **Getting started with Dart** in my next blog! Till then Bye!!!

Hope it has helped you. Thanks for bearing till the end!!

![Thankyou](/blog/images/Thankyou.gif#center)


Want to connect?
 [Github](https://github.com/Kaushl2208) | [LinkedIn](https://www.linkedin.com/in/kaushlendra-pratap-a523b9170/) | [Twitter](https://twitter.com/Kaushl1998) | [Facebook](https://www.facebook.com/kaushlendra.pratap.52)
