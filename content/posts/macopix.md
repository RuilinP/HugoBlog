+++
title = "MaCoPiX-mascot constructive for X & how to make custom ones"
date = "2023-09-01T11:24:09-04:00"
author = "Ruilin"
authorTwitter = "ruilin_peng" #do not include @
cover = "/img/macopix1.jpg"
tags = ["MaCoPiX", "guide","X"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++
# Introduction
[Official website](http://rosegray.sakura.ne.jp/macopix/index-e.html "MaCoPiX")  
MaCoPiX, Mascot Constructive Pilot for X, is a desktop mascot application for UNIX / X Window system and Microsoft Windows / macOS.  

Personally, I first got to know this amazing application when I tried out the [Mangaka](https://animesoft.wordpress.com/linux/ "Mangaka") distributions which comes with this application by default.  

In Debian-based distributions, 
{{< code language="bash" title="Installation in Debian-based distros" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
sudo apt install macopix
{{< /code >}}

And as for other distros, where the package might not be available in package manager, we could make install instead.
[Github](https://github.com/chimari/MaCoPiX "MaCoPiX") 
{{< code language="bash" title="Installation in other distros" id="2" expand="Show" collapse="Hide" isCollapsed="false" >}}
./configure (or ./configure --with-gtk2 for Gtk+2)
make
su
make install 
{{< /code >}}

And then to launch,
{{< code language="bash" title="Launch" id="3" expand="Show" collapse="Hide" isCollapsed="false" >}}
macopix
{{< /code >}}
where we can select to install official mascots from the menu.
{{< image src="/img/macopix2.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
Then in order to select a launcher-a menu we can select from a series of mascots,
{{< image src="/img/macopix3.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
After that, click on "Mascot launcher" to launch a specific mascot
{{< image src="/img/macopix4.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 


# Make custom mascots
To start with, we need to have some prictures ready for creating one. A practical idea I think would be some sprites from 2d games.
[This one for example](https://www.spriters-resource.com/pc_computer/meltybloodtypelumina/sheet/182999/ "MaCoPiX") (crop and resize if necessary)
{{< image src="/img/macopix5.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
First, I would recommend saving the sprites in the .macopix/pixmap, to easily launch/create launcher later. Then right click an opened mascot to open the menu and select 
{{< image src="/img/image.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
Then, click "New" -> "Create New Mascot"
{{< image src="/img/image2.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/image3.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/image4.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
Then follow the prompts to create .mcpx file, the first sprite for the animation(yes, you could create still mascot by stopping there).
{{< image src="/img/image5.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
Right click the still mascot and select "Config"
{{< image src="/img/image6.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
Add rest of the sprites needed in "Mascot" -> "Images"
{{< image src="/img/image7.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
In "Mascot" -> "Animation" (Base by default), append the frames and edit the "Image No." to the corresponding frame indexes in "Images" and then "Test Anime" to see the smoothness of the animation and click ok.   
{{< image src="/img/image8.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
Right click the mascot, "Save" -> "Save All", don't forget this one or you might LOSE ALL THE PROGRESS.  

Now we have a basic desktop with animation we can drag around in our desktop environment. Next I'll try to explain how to create click event(other animation/sound effect)  
{{< image src="/img/image9.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
{{< image src="/img/image10.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
Go back to "Config", click "Append Pattern" and add frames(for new animation or copy the base one) to create the animation when clicked. The "Message" is where the text box pops up when the mascot is clicked and the "Sound File" is for the audio of the mascot "speaks". For Linux, make sure we have some command line application to play the audio files and put the command in "Resources" -> "Misc." -> "Sound Command". 
{{< image src="/img/image11.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
{{< image src="/img/setuparm2.png" alt="macopix" position="left" style="border-radius: 8px;" >}}
Here is another example where I had Amiya as a siiting mascot(always somewhere above a window). To make a window sitter, in "mascot" -> "Move",adjust the coordinates and choose "Focus Follow". And by the way, in order for other languages to work in "Message", I believe we need to change system locale to the corresponding language.  
{{< youtube uafp7kDSUos>}}

