NetAidKit
====

Standalone VPN/Tor router for journalists and activists.

Building the firmware image
----

Install dependencies

```bash
sudo apt-get update
sudo apt-get install git-core build-essential libssl-dev libncurses5-dev unzip subversion gawk
```


Create a working directory somewhere and execute the following commands:

```bash
git clone https://github.com/radicallyopensecurity/netaidkit
cd netaidkit && ./build.sh
```

The compiled images will be in the netaidkit/bin folder.

Flashing the GL-iNet:
----

<ol>
    <li>While pressing the reset button on the side of the GL-iNet,
        power on the device. You will see the green LED flashing.
        Hold the reset button until the green LED flashes 5 times.
        When the red light flashes once, release your finger.
        The device is now booting into failsafe mode.</li>
    <li>Connect to the device using an ethernet cable and manually 
        set your IP address to 192.168.1.2.</li>
    <li>Visit 192.168.1.1 in your browser and upload the image called
        openwrt-ar71xx-generic-gl-inet-6416A-v1-squashfs-factory.bin
        to the page and click 'Update firmware'. Wait for the device to
        reboot into the new firmware and do not turn it off.</li>
</ol>
