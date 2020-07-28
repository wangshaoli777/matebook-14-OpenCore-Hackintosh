# matebook-13/14-2019-OpenCore-EFI  hackintosh
  
If this EFI could run in your laptop well,  
please create a issues and send info of your device like year,cpu,matebook 13 or 14.  
for helping more people who useing matebook to build their hackintosh.


very much thanks to [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)on test bigsur(beta),and i am so sorry for wasted his time,because of i did a totally wrong EFI ofr testing bigsur,my apology.  



[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)  

## Update log:  

- 20200728:  
added public beta of itlwm.kext and heliport  

- 20200725:  
Support Macos 10.15.6  

- 20200724:  
upgrade opencore to 0.5.9  


- 20200715:  
audio jack fixed,thanks randomprofilename  

- 20200712:  
this efi could be used in matebook 13/14 2019  
and under 2020 version likes:  
except wifi couldnt be load,everything is as same as 2019 version,works fine.  
the reason might be the 2020 version use 2gen ac9560,maybe can be fixed in future.


- 20200710:  
add a clover efi be used to install macos,  
this clover efi could be used to boot your hackintosh,too  
But I strongly recommand to use opencore(oc) efi to boot your device.  


- 20200709:  
1.changed MLB,ROM,Serial number   
2.add a insure file which can save your device from extremely mistake likes cant boot to any OS（WRCOVERY.BIN）  
how to use:copy it to ESR

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/recovery.png?raw=true)   


Next update maybe support Bigsur

## Works fine：
  
  
1.bluetooth（could be used like original）From IntelBluetoothFirmware @zxystd

2.wifi （need to use propertree([click to download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip) ) to inject your own ssid and password） From itlwm @zxystd

3.sleep-wakeup works well

4.hdmi（audio of hdmi,too）

5.TrackPad

6.Could get perfect powermanagement after disable cfg lock  

7.about FB part:igpu(uhd620) works well

8.cpu boost（cpufriend set in：1800mhz，maximum）

9.usb（by using ssdt）

10.FN key(brightness and sound)  

11.audio jack (need to use 【Install ComboJack to fix audio jack】under this page) 


  
  
## Doesnt work：  


1.Camera（UVC Camera VendorID_1480 ProductID_975 is available） 

2.mx250/150/350（hopeless）

  
## Info of my device     
oc version:0.5.9

macos：10.15.6 

matebook2019 i7-8565u mx250 sn720

## How to install：  

A perfect guide in:  

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  

## If you dont have any macos device：  

Download image from:  
https://blog.daliansky.net/macOS-Catalina-10.15.5-19F96-Release-version-with-Clover-5118-original-image-Double-EFI-Version-UEFI-and-MBR.html  
 
Strongly recommand to use chrome translate,if you dont understand Chinese.

Serch this text in your chrome:  

10.15.5 19F101 双EFI分区版
    
      
  
  

## Install ComboJack to fix audio jack

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)  


From Heporis:  

https://github.com/randomprofilename/ComboJack


run install.sh in terminal:  

```bash
ComboJack_Installer/install.sh
```
  
  


## How to enable HIDPI：

https://github.com/xzhih/one-key-hidpi
 

My selection：  
1. enable HiDPi (with patch/inject EDID)ーーーーーーーselete "2" at frist step
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  
  
  
## How to disable CFG lock：


upgrade your bios to 1.28,could be download in HUAWEI's official page  

1.Format a usb memory to fat32  

2.create a new floder named "EFI" at root  

3.create a new floder named "BOOT" At /EFI  

4.download [cfgunlock.zip(click)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)  

5.copy bootx64.efi from cfgunlock.zip to EFI/BOOT in your usb 

Restart and boot with this usb  

After you boot   

Press alt and "+" in same time  

And use ↑and↓ in your keyboard to find "cpusetup"  


And press enter in keyboard to enter "cpusetup"  


You will see this.  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/RU.jpg?raw=true)

  
0030-0E in your computer must be 01  

Use ←→↑↓ key to pick it and press enter  

Then,put "00" in  

Then,press ctrl and w in same time to save setting   

If save successfully,it will tell you like"update written"(i forget it)  

And alt+q to quit  

Btw.DO NOT use opencore to boot what i uploaded  

That is all of how to unlock cfg in matebook13 2019  

And you will get a perfect power management  
      
## fix time issue between windows and macos 

   
  
in windows press WIN+x run CMD with administrator  
  
  input：  
  
```bash
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```  
  
  

If this EFI could run in your laptop well,  
please create a issues and send info of your device like year,cpu,matebook 13 or 14.  
for helping more people who useing matebook to build their hackintosh.

## Thanks：

- @intel make cpu for us

- @apple create macos for us
 
- [@zxystd](https://github.com/OpenIntelWireless/itlwm) create kext of wifi and bluetooth  

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) teached me alot

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)  thanks him done a remarkable job in clover version hackintosh in matebook 13

- [@Zero-zer0](https://github.com/Zero-zer0) learned how to fix brightness key from him
