+++
title = "CSC301 flutter setup"
date = "2023-11-07T21:24:09-04:00"
author = "Ruilin"
authorTwitter = "ruilin_peng" #do not include @
cover = "/img/flutter1.png"
tags = ["flutter", "guide",]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++

# Crash course I recommend

https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0

# 1 Install Flutter

https://docs.flutter.dev/get-started/install


To check dependencies
{{< code language="bash" title="example" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
flutter doctor -v
{{< /code >}}  
{{< image src="/img/flutter1.png" alt="macopix" position="left" style="border-radius: 8px;" >}}

# 2 Devices

Well, of course, there are two types of devices that can be used for debugging, actual device and virtual device. By default we have the computer which can be used, if we have the option of the OS:
{{< image src="/img/flutterpc.png" alt="macopix" position="left" style="border-radius: 8px;" >}}   
  
  
As for mobile(Let's say android, cause I only have android). It could be either a mobile connected through adb(USB or tcp) or an emulator on our computer(which is actually also connected through adb)
{{< image src="/img/flutter4.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
^ Actual phone, screen copy can be seen in other sections of this post.  
{{< image src="/img/flutter6.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
^ Emulator, has to be running in order to be detected


# 3 Run in VScode
Install this plugin. It should also prompts you to install dart and sdks:
{{< image src="/img/flutterplugin.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 

To create one:
F1 > type "Flutter" > select "Flutter: New Project"

{{< image src="/img/flutter2.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/flutter3.png" alt="macopix" position="left" style="border-radius: 8px; width: 200px" >}} 

# 4 Run in Android Emulator
{{< image src="/img/flutter5.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 

