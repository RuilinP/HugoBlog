+++
title = "STA304A2 github"
date = "2023-11-07T21:24:09-04:00"
author = "Ruilin"
authorTwitter = "ruilin_peng" #do not include @
cover = "/img/j3.png"
tags = ["jupyterhub", "guide",]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++

# 1
第一步首先在uoft的rstudio的terminal裏初始化git

{{< image src="/img/j1.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
需保留雙引號
{{< code language="bash" title="example" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
git config --global user.email "ruilin.peng@mail.utoronto.ca"
git config --global user.name "Ruilin"
{{< /code >}}

# 2
File > New Project > Version Control > Git
{{< image src="/img/j2.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/j3.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 

順便說下已生成的repository的url: https://github.com/RuilinP/STA304


# 3
在commit/push之前需要先pull（簡單來說就是別人之前做的改動） 
兩種方法：
一：Git > commit > 然後點擊右上角的pull
{{< image src="/img/j4.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/j5.png" alt="macopix" position="left" style="border-radius: 8px;" >}}

二：在terminal裏輸入
{{< code language="bash" title="example" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
git pull
{{< /code >}}


# 4
在完成了一些工作後要上傳需要git commit + push
兩種方法：
一：Git > 選中所有要上傳的文件 > commit > 加入批註 > 右上角push
{{< image src="/img/j6.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 
{{< image src="/img/j7.png" alt="macopix" position="left" style="border-radius: 8px;" >}} 

二：在terminal裏輸入
{{< code language="bash" title="example" id="1" expand="Show" collapse="Hide" isCollapsed="false" >}}
git add --all
git commmit -m "<信息>"
git push
{{< /code >}}
然後輸入github的用戶認證完成push操作