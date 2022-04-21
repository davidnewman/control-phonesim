# control-phonesim

This is a set of simple utility scripts that make it easier to enable/disable the phonesim modem.

They are not overly adaptable, and line up with my article about [Getting Apple Airpods working on Debian 11](https://dasnewman.com/2022/04/21/airpods-on-debian-11.html) so may be making some assumptions. Feel free to modify them if you need.

## Requirements

You will need to have [ofono](https://git.kernel.org/pub/scm/network/ofono/ofono.git) cloned to `/opt/ofono`.

For example:

``` shell
sudo git clone git://git.kernel.org/pub/scm/network/ofono/ofono.git /opt/ofono
```

At that point you can clone this repository and distribute the files:

``` shell
git clone https://
cd control-phonesim

sudo cp control-phonesim restart-pulseaudio /usr/local/bin
cp restart-pulseaudio.desktop ~/.config/autostart
```

**NOTE:** You may not need `restart-pulseaudio.desktop` but I couldn't figure how to get my headset working on reboots without it...
