# Personal Steam Signature Generator

> I created this script a long time ago. Please don't use it, unless you're just curious. Maybe someday, if I feel like playing with PHP again, I'll improve it and adapt it to the newer versions of PHP. However, that might never happen. I created second branch with improvements, [you can see it here](https://github.com/Avaray/personal-steam-signature/tree/making-it-modern). Feel invited to contribute in that branch.

This PHP script generates image (PNG) with Steam status.  
This is personal script for just one user.  
Use CRON to execute this script.

Important steps:

- Set Your Steam API key in line 12 // try to dont use mine because I will delete it soon
- Set Your Steam Community ID in line 13
- If you will put this script into your webhosting remember to set CHMOD 0770 for .php file (to prevent random people from executing this file)

Would be nice to change this (if you planning to run this script from address bar in your browser):

- checkk lines 120, 125, 193

You can remove it if you want (if you dont work with Valve's Hammer Editor):

- lines from 156 to 164

## From Author:

I created this script as first (or second) PHP project ever. This was my start with programming (Thanks Simon for all your help). I cant give you a word that everything will work for you. It worked for me pretty well, but you might encounter problems, with Paths maybe (it depends on your host machine; check line 90).  
This is not complete project. I abandoned this project long time ago and I will not work with it anymore.
