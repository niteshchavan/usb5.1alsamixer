# usb_5.1_alsamixer

This is alsamixer configuration for USB soundcard stereo to 5.1 upmix. for raspberry pi 4B+ and Zero

Source https://alsa.opensrc.org/Low-pass_filter_for_subwoofer_channel_(HOWTO)

Install below dependencies for 5.1 surround sound

apt-get install blop

apt-get install cmt

apt-get install alsa-utils

now copy ladspa in /usr/lib/ladspa/

now copy asound.conf in /etc/

nano /usr/share/alsa/alsa.conf and change default sound card to desired
