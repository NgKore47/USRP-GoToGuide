# Getting started with USRP's

The Universal Software Radio Peripheral(USRP) is a flexible software-defined radio platform used in 5G for prototyping, testing, and developing new technologies. It enables real-time experimentation with 5G protocols and network simulations, offering high performance and adaptability for advancing wireless communications.

## Install UHD in system


## USRP B210
Official Documentaion: [Link](https://kb.ettus.com/B200/B210/B200mini/B205mini)

### Firmware/UHD version management
Just plug it into USB 3.0 or above port, and uhd version will be automatically caliberated as per system requirement.

## USRP N310
- Official Documentation: [Link](https://kb.ettus.com/USRP_N300/N310/N320/N321_Getting_Started_Guide)
- Filesystem Update: `SSH` or `SD-Card`
- 

### Access your USRP N310

#### via TerraTerm(Compulsary for 1st time)
- Connect usrp via usb cable to your laptop with windows(terraterm installed)
- Check COM PORT in Device Manager
<Insert Image of COM port>
- Open TerraTerm
- Set Boud rate to 3210000
- 

#### via SSH (if you know ip addr)


### Firmware/UHD version management

#### Via SD-Card

- Download USRP filesystem in local system
```
uhd_images_downloader -t n3xx_common_sdimg_default
```
- Load the image in SD-Card
```
sudo dd if=<YOUR_IMAGE> of=/dev/<YOUR_SD_CARD> bs=1M status=progress
```
- Insert the SD-Card in USRP and power ON.
- Filesystem update completed.

#### Via SSH remote fs update