# matebook-13/14-2019-OpenCore-EFI  ハッキントッシュ  

もし、このEFIファイルはあなたのデバイスでうまく動作できるなら、このプロジェクトでissuesを提出して下さい  
件名は：matebook 13か14か、どのyearのバージョンか、CPUは何か。例：matebook 14 2019 I7 8565u  
ハッキントッシュをインストールしたいユーザに対し、いい参考になりますので、ご協力を御願いします。

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

5.TrackPad 問題なし  

6.cfg lockを無効することで、パワーマネジメントが完璧に動作できる  

7. uhd620 問題なし  

8.cpu boost（cpufriend.kextに1800mhz，maximumを設定しました）  

9. usb（ssdtを用いて修復）

10.ホットキー(brightness and sound)

  
  
## 動作するのには問題のあるもの：  


1.一部の付属カメラ（1480 typeが動作できる（全体の5%ぐらい）,幸運をお祈りします） 

2.一部のaudio jack（カメラと同じような状況,幸運をお祈りします）  
このページの下の部分にはaudio jackを修復するガイドがあるのですが、必ず修復できると保証できません。

3.mx250/150/350（どうしても無理です）

  
## 自分のデバイス情報     
oc version:0.5.8

macos：10.15.5 

matebook13 2019 i7-8565u mx250 sn720

## インストールの手順：  

下の外部ページを参考して下さい：  
（このガイドは最高のものですが、一定の英語能力が必要です）　　

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  

## もし手元にはマックOSのデイバスを持っていない場合：  
（上のガイドにはマックOSをインストールするに使うimgをダウンロードするにはマックOSを稼働するデバイスが必要です）  

下のリンクからOSをインストールするに使うimgをダウンロード可能:  
https://blog.daliansky.net/macOS-Catalina-10.15.5-19F96-Release-version-with-Clover-5118-original-image-Double-EFI-Version-UEFI-and-MBR.html  
 
上記の外部ページは中国語で記載されていますので、chromeの翻訳機能をお勧めします.

上記のページでimgをダウンロードするリンクを速く見つかるために以下の文字をそのページでサーチして下さい:  

10.15.5 19F101 双EFI分区版
    
      
  
  

## ComboJackを用いてaudio jackを修復する方法

From Heporis:  

https://github.com/hackintosh-stuff/ComboJack  


上記のリングで記載している.shファイルをterminalで実行させるためのコード:  

```bash
ComboJack_Installer/install.sh
```
  
  


## HIDPIを有効にする方法：

https://github.com/xzhih/one-key-hidpi
 

自分の例：  
1. enable HiDPi (with patch/inject EDID)     一つ目には"2"を選んで下さい
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  
  
  
## CFG lockを無効にする方法：


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
      
      

もし、このEFIファイルはあなたのデバイスでうまく動作できるなら、このプロジェクトでissuesを提出して下さい  
件名は：matebook 13か14か、どのyearのバージョンか、CPUは何か。例：matebook 14 2019 I7 8565u  
自分のデバイスでハッキントッシュをインストールしたい他のユーザに対し、いい参考になりますので、ご協力を御願いします。

## Thanks：

- @intel make cpu for us

- @apple create macos for us
 
- [@zxystd](https://github.com/OpenIntelWireless/itlwm) create kext of wifi and bluetooth  

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) teached me alot

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)  thanks him done a remarkable job in clover version hackintosh in matebook 13

- [@Zero-zer0](https://github.com/Zero-zer0) learned how to fix brightness key from him
