# Realtek RTL8811CU/RTL8821CU USB Wi-Fi adapter driver version 5.4.1 for Linux 4.4.x up to 5.6.x

A few known wireless cards that use this driver include:
* [Fastoe AC650 USB Wi-Fi Adapter](https://amzn.to/2KR1Lxi)

### Manual installation

To build, you have to retrieve source and run `make`.
If via Git, do following:

```bash
sudo apt-get update
sudo apt-get install build-essential
git clone https://github.com/fastoe/RTL8811CU.git
cd RTL8811CU
make
sudo make install
sudo reboot
```

Plug your USB Wi-Fi adapter into your PC.

### Checking installed driver
If you successfully install the driver, the driver is installed on `/lib/modules/<linux version>/kernel/drivers/net/wireless/realtek/rtl8821cu`. Check the driver with the `ls` command:
```
ls /lib/modules/$(uname -r)/kernel/drivers/net/wireless/realtek/rtl8821cu
```
Make sure `8821cu.ko` file present on that directory

### Monitor mode
Use the tool 'iw', please don't use other tools like 'airmon-ng'
```
iw dev wlan0 set monitor none
```

Enjoy!
