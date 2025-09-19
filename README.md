Download Debian (https://www.debian.org). Netinst image is enough.

Get the image to a usbkey or other bootable medium (hint: usb external ssd with ventoy is much faster, and in some cases cheaper).

Install Debian. To make it headless (no desktop environment etc.), uncheck all the desktop options in the installer at when prompted (uncheck Gnome, kde and all those). 
Check the option for SSH server. Finish install and reboot.
Make sure you remember the passwords you created during the install.

Login as root is not best practice, so make your user sudo:
Login as your user. 
If you installed as headless, you won't have a desktop. So in the terminal type:
su -
<enter your root password>
Type: EDITOR=nano visudo  OR (if you like vi) type: visudo
add this line: USER_NAME   ALL=(ALL:ALL) ALL
where USER_NAME is the user you created, or another user you want to have sudo.
To add the memebers of the usergroup "wheel" to sudo add the line: %wheel  ALL=(ALL:ALL) ALL
Save and exit the editor.
[refrence: https://wiki.archlinux.org/title/Sudo and https://wiki.debian.org/sudo/]

