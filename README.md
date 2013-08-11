INIT SCRIPT FOR BITMESSAGE
===============================================

# DESCRIPTION
If you want to help the cause and run bitmessage on a server to relay traffic you can use this script to make a Debian service.

# INSTALATION
As root do the following

1) This script uses screen, so first you need to install it if you havn't already

    apt-get install screen

2) install the initscript

    cd /etc/init.d/ && wget 