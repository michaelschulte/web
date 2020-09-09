---
id: 163
title: resinstalling packages in R after update
date: 2011-04-14T23:15:45-07:00
author: Michael
layout: post
guid: http://www.schulte-mecklenbeck.com/?p=163
permalink: /2011/04/resinstalling-packages-in-r-after-update/
categories:
  - R
---
The new version 2.13.0 of [R](http://www.r-project.org/ "R") has just been released and with the update comes the pain of re-installing all the packages from the old installation on the new one.

[Stackoverflow](http://stackoverflow.com/ "Stackoverflow") to the rescue! This [posting](http://stackoverflow.com/questions/1401904/painless-way-to-install-a-new-version-of-r) provides a simple two step process of first writing a list of packages into a file on the disk in the old version, installing the new version and then comparing the exported list to the currently installed packages in the new version with setdiff. I just went through the process and have to say that it is deadeasy! Below the code &#8230;

`#--run in the old version of R <br />
setwd("C:/Temp/") <br />
packages <- installed.packages()[,"Package"] <br />
save(packages, file="Rpackages") `

`INSTALL NEW R VERSION`

`<code>#--run in the new version <br />
setwd("C:/Temp/") <br />
load("Rpackages") <br />
for (p in setdiff(packages, installed.packages()[,"Package"])) <br />
install.packages(p) <br />
` </code>

``