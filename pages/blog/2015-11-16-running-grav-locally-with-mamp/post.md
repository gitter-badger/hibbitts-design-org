---
title: 'Running Grav Locally with MAMP'
slug: running-grav-locally-with-mamp
date: '15-11-2015 00:00'
comments: true
metadata:
    'twitter:card': summary
    'twitter:site': '@hibbittsdesign'
    'twitter:title': 'Running Grav Locally with MAMP'
    'twitter:description': 'Step-by-step instructions to run Grav on your Mac/PC.'
taxonomy:
    tags:
        - Grav
        - MAMP
---

One of the (many) great things about [Grav](http://getgrav.org) is that no database setup is required, which makes running a local copy of Grav on your computer for development or testing purposes a straightforward process. In this brief article we will look at how to use [MAMP](https://www.mamp.info/en/), a tool to safely run PHP server on your computer, to run Grav locally on your Mac or Windows PC.

**Step-by-step Instructions**

1. Download MAMP (https://www.mamp.info/en/downloads/) and install the application
2. Download Grav (http://getgrav.org/downloads/) and extract downloaded archive file
3. Copy the entire extracted Grav folder to '/Applications/MAMP/htdocs/' on a Mac or 'C:/MAMP/htdocs' on a Windows PC
4. Launch the MAMP application
5. Press the MAMP button 'Start Servers' (see Figure 1)
6. Launch your Web Browser, enter the URL http://localhost:8888 and then press the RETURN key
7. In your Web Browser you should now see the htdocs directory listing - press on the displayed Grav folder name
8. You're done!

![MAMP Welcome Screen](../2015-11-16-running-grav-locally-with-mamp/MAMP.png)  
_Figure 1. MAMP startup screen._

If you would prefer to only need to enter 'http://localhost' in your Web Browser to access your MAMP htdocs directory listing, then do the following:

1. Launch the MAMP application. If MAMP is already running, press the 'Stop Servers' button
2. Press the MAMP 'Preferences' button (see Figure 2)
3. Press the 'Ports' tab in the 'Preferences' dialog
4. Change the value in the 'Appache Port' field to '80' (no quotes)
5. Press the 'OK' button  

![MAMP Preferences Dialog](../2015-11-16-running-grav-locally-with-mamp/MAMP-preferences.png)  
_Figure 2. MAMP Preferences dialog._

Remember, once you've got your Grav site working as you want locally all you need to do is copy/FTP the files over to your server! No database (worries) required.
