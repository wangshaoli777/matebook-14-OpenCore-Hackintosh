# matebook-13/14-2019-OpenCore-EFI  ハッキングトッシュ  

もしこのEFI　ファイルはあなたのデバイスでうまく動作できるなら、このプロジェクトでissuesを提出して下さい  
件名は：matebook 13か14か、どのyearのバージョンか、CPUは何か。例：matebook 14 2019 I7 8565u  
自分のデバイスでハッキングトッシュをインストールしたい他のユーザに対し、いい参考になりますので、ご協力を御願いします。

[中文](readme.md) | [日本語](readme-jp.md) | [English](readme-en.md) 

## Update log:  
20200712:  
このEFIファイルは matebook 13/14 2019で動作できるのを判明しました。  
そして、2020 versionでの動作状況は以下となります:  
wifiのkextはload不能,他の部分は 2019 version,と同じでうまう動作できる.  
原因は2020 versionには第二世代のac9560を使用しているらしいです、今後には、修復を期待できると考えています。


20200710:  
マックOSをインストールするためのclover EFIを添付しました、    
このclover EFIファイルはマックOSをbootすることにも使えるのですが、  
opencore(oc) efiを使ってマックOSをbootすることをお勧めします.  


20200709:  
1.新しい　MLB,ROM,Serial numberをアップデートしました   
2.緊急修復に使うWRCOVERY.BINを添付しました、このファィルはrecoveryから抽出したものです  
使い方:SSDのESRにコピーして下さい

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%88%AA%E5%B1%8F0002-07-12%2023.29.34.png?raw=true)   


今後のアップデートには macos 11 Bigsurにサポートするかもしれません。

## 正常に動作できるもの：
  
  
1.bluetooth（完璧に動作できる）From IntelBluetoothFirmware @zxystd

2.wifi （propertreeを使ってssidとpasswordを設定する必要がある） From itlwm @zxystd

3.sleep-wakeup 問題なし

4.hdmi（HDMIの音声も問題なし）

5.TrackPad

6.cfg lockをアンロックすることで、パワーマネジメントが完璧に動作できる  

7. done the FB,igpu(uhd620) works well

8.cpu boost（cpufriend set in：1800mhz，maximum）

9. usb（by using ssdt）

10.FN key(brightness and sound)

  
  
## Doesnt work：  


1.Camera（5% in 1480 type could works fine,hope you luck） 

2.audio jack works not perfectly（like Camera,hope you luck）  
there is guide to fix audio jack under this guide

3.mx250/150/350（hopeless）

  
## Info of my device     
oc version:0.5.8

macos：10.15.5. 

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

From Heporis:  

https://github.com/hackintosh-stuff/ComboJack  


run this .sh in terminal:  

```bash
ComboJack_Installer/install.sh
```
  
  


## How to enable HIDPI：

https://github.com/xzhih/one-key-hidpi
 

My selection：  
1. enable HiDPi (with patch)     selete "2" at frist step
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  
  
  
## How to disable CFG lock：


upgrade your bios to 1.27,could be download in HUAWEI's official page  

1. Format a usb memory to fat32  

2.create a new floder named "EFI" at root  

3.create a new floder named "BOOT" At /EFI  

4.download cfgunlock.zip  

5.copy bootx64.efi from cfgunlock.zip to EFI/BOOT in your usb 

Restart and boot with this usb  

After you boot   

Press alt and "+" in same time  

And use ↑and↓ in your keyboard to find "cpusetup"  


And press enter in keyboard to enter "cpusetup"  


You will see this.  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/IMAGE%200002-07-12%2023:20:39.jpg?raw=true)

  
0030-0E in your computer must be 01  

Use ←→↑↓ key to pick it and press enter  

Then,put "00" in  

Then,press ctrl and w in same time to save setting   

If save successfully,it will tell you like"update written"(i forget it)  

And alt+q to quit  

Btw.DO NOT use opencore to boot what i uploaded  

That is all of how to unlock cfg in matebook13 2019  

And you will get a perfect power management  
      
      

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
