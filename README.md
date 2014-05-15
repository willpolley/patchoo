junki
=====

[https://github.com/munkiforjamf/junki](https://github.com/munkiforjamf/junki)


Junki somewhat emulates [munki](https://code.google.com/p/munki/) workflows and user experience for JAMF Software's [Casper Suite](http://www.jamfsoftware.com/products/casper-suite/).  

**Casper** is the best all round management platform for all things Apple. It's incredibly powerful and the JSS has no competition, but the fact it started it's life a few years a go when Mac admins were using image based deployment workflows has meant there is a gap in functionality when it comes to post deployment patching. You can deploy patches via different built in triggers and policies but  there is no built-in GUI for user interaction, there is no cohesive way to deploy Apple and 3rd party updates and the user experience is lacking.

**Munki** is the absolute best way to deploy and install software on many Macs at once. It does one thing, and it does it amazingly well. It can install software and ensure Macs are patched better than any other system. It provides a great end user GUI, unifies Apple and 3rd party software installations and allows installations to be deferred. Junki is munki inspired, and *hopefully* brings some of munki's greatness to (the already great) Casper.

A lot of people have built different solutions on JAMFnation, but I think junki is the best and most complete way to deploy and patch your Macs *in the wild*. It provides a great workflow for admins and an excellent user experience.

### Why not just use munki? ###

That's certainly an option, and many people do use munki and Casper. It does mean administering another tool and there is no formal training or certification track for munki, which is important to some organisations. I hope some of these methods one day become part of Casper.

### Junki isn't just a script... ###
  
...it's a patching and deployment methodology that;  

* allows munki style deployment groups (*dev / beta / production / etc*) based on JSS computer group membership.
* will write your Apple Software Update catalogURL dynamically so these deployment groups can be pointed at [NetSUS](https://jamfnation.jamfsoftware.com/viewProduct.html?id=180&view=info) / [reposado](https://github.com/wdas/reposado) branches.
* can chain incremental updaters intelligently (*eg. MS Office 2011 14.3.7, 14.3.8, 14.3.9*)
* leverages existing and familiar Casper frameworks and methods (triggers, policies, smart groups) 

From a user experience perspective it;   

* provides Casper with a much needed a GUI for software installation.
* unifies Casper and Apple Software Update installations.
* allows installations to be deferred, allows flexibiliy but maintaining compliance.
* ensures users are logged out during installations.
* integrates nicely with Self Service.

### Demonstration ###

##### User Prompt Screenshot #####

![User Prompt](https://raw.githubusercontent.com/munkiforjamf/junki/master/docs/images/prompt.png)

##### Overview Video #####
	
[![junkiDemo Video](http://img.youtube.com/vi/aeOOPHH3-NY/0.jpg)](http://www.youtube.com/watch?v=aeOOPHH3-NY)

##### Sample [jamf.log](https://github.com/munkiforjamf/junki/blob/master/docs/jamf_junki.log.txt) from the video 


### DISCLAIMER: USE AT YOUR OWN RISK! ###

*The documentation needs work, the code isn't pretty and it shouldn't be written in bash but it (mostly) works! I am not a programmer, I'm just a lowly systems engineer that's kludged a few scripts in his time. I do think I have nailed the workflow and user experience though. It's here on GitHub so you can help make it great!*


Requirements
------------
* CocoaDialog 3.x
* JAMF Casper (developed & tested on 9.22 - might work on 8.x)
* http enabled dist points or JDS (policy within policy doesn't play nice with fileshare based CDPs)
* OSX (10.6-10.9)
* *A big bunch of Macs!*


Documentation
-------------
     
[https://github.com/munkiforjamf/junki/blob/master/docs/_index.md](https://github.com/munkiforjamf/junki/blob/master/docs/_index.md )


Help out!
---------


If you want to help in anyway please reach out via email or jump onto GitHub.

If you find it useful and want to say thank you, link up on LinkedIn, tell me how and where you are using it, and write me a recommendation whilst you are there! [http://au.linkedin.com/in/lachlanstewart](http://au.linkedin.com/in/lachlanstewart)

  
###Enjoy junki responsibly!###

Lachlan.

