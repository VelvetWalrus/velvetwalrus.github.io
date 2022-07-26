---
layout: post
title: (IntelliJ) Cause: invalid source release: 17
---

https://github.com/VelvetWalrus/velvetwalrus.github.io/blob/master/images/Cause_invalid%20source%20release%2017.png

1) Java versions are conflicted on somewhere (setting in IntelliJ problem)
2) Java (17) is uninstalled.   
    (My case) : Java 17 is installed on IntelliJ, but not on the hardware.
                    Solution -> Install the Java 17 on Oracle Page.

BUT
it failed...

new solution -> downgrade Java version to 1.8 ; 
1) File - Project Structure - Project
2) File - Project Structure - Modules (Automatically modified following Project setting.)
3) build.gradle ; sourceCompatibility = '1.8'

and it is solved.

https://github.com/VelvetWalrus/velvetwalrus.github.io/blob/master/images/test%20success.png


Error category : #configuration, #JavaVersion, #IntelliJ 
Search Keyword : #error 
