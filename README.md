INIT SCRIPT FOR BITMESSAGE
===============================================

# DESCRIPTION
If you want to help the cause and run bitmessage on a server to relay traffic you can use this script to make a Debian service.

# INSTALATION
As root do the following

1) This script uses screen, so first you need to install it if you havn't already

    apt-get install screen

2) Install the initscript and make it executable

    cd /etc/init.d/ && wget https://raw.github.com/super-nathan/bitmessage-init/master/bitmessage && chmod +x bitmessage

3) In order to run as a daemon, you must have the option set in the the keys.dat file. You should add on a seperate line "daemon = true"

    $EDITOR /BITMESSAGEUSER/.config/Pybitmessage/keys.dat

4) Edit the script to use your install folder by changing "PBM_LOCATION". 

    $EDITOR /etc/init.d/bitmessage

5) You *really* should have bitmessage run as an upriveledged user so change "USERNAME" to your bitmessage user

    $EDITOR /etc/init.d/bitmessage

6) Have it autostart (optional)

    update-rc.d enable bitmessage

7) Start bitmessage

    service bitmessage start