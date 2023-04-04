# BgInfo scripts

[BGInfo](https://learn.microsoft.com/en-us/sysinternals/downloads/bginfo) is a free tool that can show relevant system information right on the Windows desktop. In addition to built-in fields it allows to add custom fields with a wide variety of information sources, not least of them - custom scripts in everyone's "favorite" scripting language - VB Script.  

This repository is a collection of scripts that can be used as sources for BgInfo custom fields and some automation. This is probably the second time in my life when I've been exposed to VB Script so they very likely don't follow best practices of VB Script, if there are any.  
The scripts are provided as-is without a warranty of any kind, only with the hope that they might be useful. Inspect the scripts before use and use at your own risk.  
PRs are welcome!  

## bginfo.bat

A quick and dirty way to run BGInfo on a schedule. Be vary that running it too often might get you blocked from one or more of the services.
Running it once a minute appears to be OK.

## getip.vbs

Gets your public IP address from https://ifconfig.me/ip. ifconfig.me returns the IP address in plain text and there don't seem to be any limits or things like CloudFlare protection - which is great if you want to periodically refresh the information.  

## getgeoip.vbs

Gets IP address location from https://seeip.org. seeip.org doesn't seem to have any real rate limit which is great if you want to periodically refresh the information.  
NB! Through trial and error it became apparent that their data (https://dev.maxmind.com/geoip) is not up to date and for some IP addresses shows entirely different locations.  
The script also contains the code for getting the data from https://ifconfig.co which in my experience provided much more accurate results even though they appear to use the same source - [www.maxmind.com](https://www.maxmind.com). https://ifconfig.co uses CloudFlare protection so it might not work.  