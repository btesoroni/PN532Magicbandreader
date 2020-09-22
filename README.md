# PN532Magicbandreader

1. Open SPI of the Raspberry Pi:

sudo raspi-config
Select 9 Advanced Options -> SPI -> yes.
2. Install some dependent packages

sudo apt-get update
sudo apt-get install libusb-dev libpcsclite-dev i2c-tools
3. Download and unzip the source code package of libnfc

cd ~
wget http://dl.bintray.com/nfc-tools/sources/libnfc-1.7.1.tar.bz2
tar -xf libnfc-1.7.1.tar.bz2  
4. Compile and install

cd libnfc-1.7.1
./configure --prefix=/usr --sysconfdir=/etc
make
sudo make install 
5. Write the configuration file for NFC communication

cd /etc
sudo mkdir nfc
sudo nano /etc/nfc/libnfc.conf
add infor from libnfc.conf
