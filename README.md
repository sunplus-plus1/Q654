# How to compile 
Before you compile, please make sure these packages are installed:
```bashl
sudo apt-get install pv openssl libssl-dev bison flex git make u-boot-tools libmpc-dev libgmp-dev python3-pip mtd-utils
pip install pycryptodomex pyelftools Crypto 
```
Fetch the source code:
```bash
git clone https://github.com/sunplus-plus1/Q654.git
cd Q654
git submodule update --init --recursive
git submodule foreach git checkout master
```
Configure the build:
```bash
make config
```
>Following the selection of script options, If you want to change the kernel configuration, run:
```
make kconfig
```
>after make config has completed. 
>
>**Note 1:** Please don't enter the `linux/kernel` folder and run "`make menuconfig`"
>
>**Note 2:** For USB gadget support, please refer to [here](https://github.com/sunplus-plus1/usb_gadget)

Build the kernel:
```
make
```
If your local LANG is not english, please run
```
LANG=c make
```
When the build completes, you will find the image file in the `out` folder.
