# Darksimpson Root Hack

1. Converted dropbear to SSH server (in theory, it should consume less resources). 
2. During installation, the start script is deleted from the old sshd, if it was already there (so that one does not interfere with the other). 
3. More gentle interference with the printer system: group, passwd and shadow files are not copied stupidly and head-on. When installed, the root password is changed to "root" automatically by passwd. Then, after logging in via passwd, you can manually change it to your own. 
4. The installation is the same: unpack into the root of the flash drive, flash drive into the printer, restart the printer.
