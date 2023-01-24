# remove-old-kernels
Mageia removal tool for old kernels using urpme.
Once installed it may be left to do it's job without user intervention.

It is run by cron.weekly to retain a minimum number of installed kernels
of each flavour. (Default is three)
This may be adjusted or disabled using simple command line options if desired.

There is also an advanced mode, offering features for power users.

It may also be run manually in interactive mode from the desktop menu,
under Tools -> System tools.

Running as normal user from the command line will display the current status
of installed kernels but will not allow removal.

For more information see: 'man remove-old-kernels' or 'man rok' in a terminal.

# Authors
 * Pierre Jarillon 2018 - 2022.
 * Jean-Baptiste Biernacki 2021
 * Barry C Jackson 2022 - 2023
 * Johnny A Solbu 2023 

# History
Following a long running bug report about failing systems with sometimes over 50 installed kernels and
disk space exhausted, I decided that unless I did something myself this would just drag on ad infinitum.  
A basic package had already been created by Bruno Cornec using the original script, but there was no automatic integration into
regular systems at install time, which would be essential for non-tech users.  
It was apparent that more advanced users would need greater flexibility and control.  
So, whilst keeping 'no user intervention needed' by default, command line options were added to suit most needs, along with
the optional use of alternative configuration files (an idea from Pierre Jarillon).  
Mageia QA team requested more advanced features to avoid certain kernels being removed that may be required during testing,
so these can now be protected using the Q option.  
A .desktop file was added into the Mageia main system menu using policykit based login for root access.  
A log file was added for the automatic runs controlled by cron.weekly with fixed log rotation at 1000 lines approx.  
Internationalization support has been added for the main bash script and thanks to the translatiors listed below we now have several langauages
catered for.  

# Tranlsators
 * ajunior (Brazilian Portugese)
 * Philippe Didier (French)
 * Johnny A. Solbu (Norwegian Bokmål)
 * psyca (German)
 * aguador (Spanish)
 * umeaboy (Swedish)  

If you would like to help with other languages, then please read TRANSLATIONS.md

## Screen shot in Konsole under KDE plasma5

![Screenshot](./Screenshot_20230124.png?raw=true)
This image demonstrates the use of an alternative configuration file as indicated top right by F:1. It is using a blue header background rather than the default green. F:1 is highlighted in red as a warning that the alternative configuration is in use.   
Likewise the AUTO setting of "0" (OFF) is highlighted in red to warn that the program will not be working automatically to keep the number of kernels to 3 as it is turned off.  
"Q" on the header indicates that the program is in QA or expert mode, although no expert features have been triggered in this system as it's a fairly basic test machine.  
Read the man page and -h help for full details of options. Otherwise just install and forget as by default it will avoid old kernels accumulating. 
