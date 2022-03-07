# SpotiPi
## Raspberry Pi Zero w Spotify Player


Uses this repo
https://github.com/dtcooper/raspotify

Support for ARMv6 (Pi v1 and Pi Zero v1.x) has been dropped.
0.31.8.1 was the last version to be built with ARMv6 support.

You can install and run that version on an ARMv6 device, but you will never get updates and doing so is completely unsupported.
https://github.com/dtcooper/raspotify/releases/tag/0.31.8.1

Then did:
dpkg -i https://github.com/dtcooper/raspotify/releases/download/0.31.8.1/raspotify_0.31.8.1.librespot.v0.3.1-54-gf4be9bb_armhf.deb

## Then Setup Audio:
https://www.raspberrypi-spy.co.uk/2019/06/using-a-usb-audio-device-with-the-raspberry-pi/

Set USB Audio as Default Audio Device
The USB sound device can be made the default audio device by editing a system file “alsa.conf” :

sudo nano /usr/share/alsa/alsa.conf
Scroll and find the following two lines:

defaults.ctl.card 0
defaults.pcm.card 0
Change the 0 to a 1 to match the card number of the USB device :

defaults.ctl.card 1
defaults.pcm.card 1


