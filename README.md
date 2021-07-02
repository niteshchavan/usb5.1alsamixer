# usb_5.1_alsamixer

This is alsamixer configuration for USB soundcard stereo to 5.1 upmix. for raspberry pi 4B+ and Zero

Source https://alsa.opensrc.org/Low-pass_filter_for_subwoofer_channel_(HOWTO)

Install below dependencies for 5.1 surround sound

apt-get install blop

apt-get install cmt

apt-get install alsa-utils

now copy ladspa in /usr/lib/ladspa/

now copy asound.conf in /etc/

nano /usr/share/alsa/alsa.conf and change default sound card to desired mine is 2 so..


defaults.ctl.card 2
defaults.pcm.card 2
defaults.pcm.device 0


you can find the card number with aplay -l command

 root@Home:~# aplay -l
 
 card 0: b1 [bcm2835 HDMI 1], device 0: bcm2835 HDMI 1 [bcm2835 HDMI 1]
  Subdevices: 4/4
  Subdevice #0: subdevice #0
  Subdevice #1: subdevice #1
  Subdevice #2: subdevice #2
  Subdevice #3: subdevice #3
card 1: Headphones [bcm2835 Headphones], device 0: bcm2835 Headphones [bcm2835 Headphones]
  Subdevices: 4/4
  Subdevice #0: subdevice #0
  Subdevice #1: subdevice #1
  Subdevice #2: subdevice #2
  Subdevice #3: subdevice #3
card 2: ICUSBAUDIO7D [ICUSBAUDIO7D], device 0: USB Audio [USB Audio]
  Subdevices: 0/1
  Subdevice #0: subdevice #0
root@Home:~#
