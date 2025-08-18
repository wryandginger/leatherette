# Leatherette - A gracenote/zap2it scraper
<div align=center> <img src=https://github.com/user-attachments/assets/1d86904b-5873-4709-8d37-542f1294cce0 alt="Image of Grace Jones" width="200"></div>

Leatherette is a vibe-coded adaptation of zap2xml.py 
(which is a fork of zap2xml.pl, which is a fork of an EXE once used on Windows Media Center PCs....)

This file produces an xmltv.xml file containing about 7 days worth of US TV guide information, image urls, and other metadata.
This shouldn't require anything special other than python to run, but you must follow the rules:

* To download NYC DirecTV: python3 zap2xml.py -c USA --device X --aid tribnyc2dl -z 10101 --headend-id DITV501
* To download local OTA: python3 zap2xml.py -c USA --device X --aid orbebb -z 80918

Raw data that is collected is stored in a cache folder for future use. 
Sometimes the server goes down or is unavailable, so you may not always be able to get the full guide data you want.
Making a bash script that runs your command every 6-12 ideas is a good idea, this will give you a file that always has roughly 6-7 days worth of data using one of the examples above.
Once you have your xml file you can load it into Jellyfin, Emby, Plex, Xteve, Threadfin, TVHeadend, or whatever you're using to manage your TV streaming.
<b>Again, make sure you follow the rules</b>

# The Rules:
1. Do not hammer the servers. Run it once every 6 hours <b>AT MOST.</b>
2. Abusing this will ruin things for everyone.
3. Make sure you keep your cache directoery, so you don't unnecessarily ping the server (see Rule 1)
4. In the event the output is blank, try changing your affiliate id (--aid). Other examples are listed in --help
