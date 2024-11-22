
# How to Compile  

## Prerequisites  
Before compiling, ensure the following packages are installed:  
```bash  
sudo apt-get install pv openssl libssl-dev bison flex git make u-boot-tools libmpc-dev libgmp-dev python3-pip mtd-utils libncurses* mtools  
pip install pycryptodomex pyelftools Crypto  
```  

## Download the Source Code  
Clone the repository and initialize submodules:  
```bash  
git clone https://github.com/sunplus-plus1/Q654.git  
cd Q654  
git submodule update --init --recursive  
git submodule foreach git checkout master  
```  

## Configure the Build  
Run the following command to configure the build:  
```bash  
make config  
```  
**Note:** After completing `make config`, if you want to adjust the kernel configuration, use:  
```bash  
make kconfig  
```  
Do **not** manually enter the `linux/kernel` folder to run `make menuconfig`.  

## Build the Project  
To build all components, execute:  
```bash  
make  
```  
If your local `LANG` environment variable is not set to English, use:  
```bash  
LANG=C make  
```  

When the build completes, the output image file will be located in the `out` folder.  

## Additional Resources  

### Downloading and Compiling Code  
Refer to the detailed guide:  
[Downloading and Compiling Code](https://sunplus.atlassian.net/wiki/spaces/C3/pages/1988034774/Downloading+and+Compiling+Code)  

### Release Details  
Find information about release versions:  
[Releases](https://sunplus.atlassian.net/wiki/spaces/C3/pages/2263875587/Releases)  

### SP7350 References  
- [SP7350 Hardware](https://sunplus.atlassian.net/wiki/spaces/C3/pages/2037121029/SP7350+Hardware)  
- [SP7350 Software](https://sunplus.atlassian.net/wiki/spaces/C3/pages/2003271700/SP7350+Software)  
- [SP7350 Application Notes](https://sunplus.atlassian.net/wiki/spaces/C3/pages/1984233474/SP7350+Application+Notes)  
