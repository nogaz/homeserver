Download Debian (https://www.debian.org). Netinst image is enough.<br>

Get the image to a usbkey or other bootable medium (hint: usb external ssd with ventoy is much faster, and in some cases cheaper).

Install Debian. To make it headless (no desktop environment etc.), uncheck all the desktop options in the installer at when prompted (uncheck Gnome, kde and all those). <br>
Check the option for SSH server. Finish install and reboot.
Make sure you remember the passwords you created during the install.

Login as root is not best practice, so make your user sudo:<br>
Login as your user. <br>
If you installed as headless, you won't have a desktop. So in the terminal type:<br>
su -<br>
enter your root password<br>
Type: EDITOR=nano visudo  OR (if you like vi) type: visudo<br>
add this line: USER_NAME   ALL=(ALL:ALL) ALL<br>
where USER_NAME is the user you created, or another user you want to have sudo.<br>
To add the memebers of the usergroup "wheel" to sudo add the line: %wheel  ALL=(ALL:ALL) ALL<br>
Save and exit the editor.<br>
[refrence: https://wiki.archlinux.org/title/Sudo and https://wiki.debian.org/sudo/]<br>

