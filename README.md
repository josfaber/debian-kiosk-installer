# Kiosk installer for Debian based Linux distros
Small installer script to setup a minimal kiosk with Chromium for Debian based Linux distros. This installer is heavily based on the excellent [instructions by Will Haley](http://willhaley.com/blog/debian-fullscreen-gui-kiosk/).

## Usage
* Setup a minimal Debian without display manager, e.g. Kali netboot cd [i386](http://http.kali.org/dists/kali-rolling/main/installer-amd64/current/images/netboot/mini.iso) / [amd64](http://http.kali.org/dists/kali-rolling/main/installer-i386/current/images/netboot/mini.iso)
* Login as root or with root permissions
* Download this installer, make it executable and run it

  `wget https://raw.githubusercontent.com/josfaber/debian-kiosk-installer/master/kiosk-installer.sh; chmod +x kiosk-installer.sh; ./kiosk-installer.sh`

If you are installing to a Raspberry Pi, change chromium to chromium-browser in the install script (both in apt line and startup command)

## What will it do?
It will create a normal user `kiosk`, install software (check the script) and setup configs (it will backup existing) so that on reboot the kiosk user will login automaticaly and run chromium in kiosk mode with one url. It will also hide the mouse. 

## Change the url
Change the url at the bottom of the script, where it sais https://neave.tv/

## Is it secure?
No. Although it will run as a normal user (and I suggest you don't leave a keyboard and mouse hanging around), there will be the possibility of plugin' in a mini keyboard, opening a terminal and opening some nasty things. Security is your thing ;-) 
