# matebook-13/14-2019/2020-OpenCore-EFI  ハッキントッシュ  

もし、このEFIファイルはあなたのデバイスでうまく動作できるなら、このプロジェクトでissuesを提出して下さい  
件名は：matebook 13か14か、どのyearのバージョンか、CPUは何か。例：matebook 14 2019 I7 8565u  
ハッキントッシュをインストールしたいユーザに対し、いい参考になりますので、ご協力を御願いします。

日本語でokay!  

EFI download：[releases](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  


[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)  

## アップデート履歴:  
  
- 20200814:  
V0814のEFIはcatalinaとbigsurで両方にも使えるようにしました、一部のssdtを作り直しました。  

- 20200806:  
OpenCoreをオフィシャルの0.6.0にアップグレードしました。  


- 20200802:  
updated itlwmx.kext for 2020ver laptop,[click for download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/itlwmx%20beta0802.zip) 

- 20200731:  
  macOS　11　BigSurをインストールするためのEFIをアップロードした。  
    [クリックしてダウンロード](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/Bigsur/EFI%20for%20installing%20bigsur.zip)  
- 20200728:  
itlwm.kextとHeliPort.dmgをpublic betaバージョンに更新しました  
HeliPort.dmgの使い方：macOSでダブルクリックでインストールする  


- 20200725:  
Macos 10.15.6までに対応できることを判明した   

- 20200724:  
opencoreを0.5.9にアップグレードしました。  

- 20200715:  
audio jackを修復しました。方法は下の「ComboJackを用いてaudio jackを修復する方法」に書いてあります。  

- 20200712:  
このEFIファイルは matebook 13/14 2019で動作できるのを判明しました。  
そして、2020 versionでの動作状況は以下となります:  
wifiのkextはload不能,他の部分は 2019 version,と同じでうまう動作できる.  
原因は2020 versionには第二世代のac9560を使用しているらしいです、今後には、修復を期待できると考えています。


- 20200710:  
マックOSをインストールするためのclover EFIを添付しました、    
このclover EFIファイルはマックOSをbootすることにも使えるのですが、  
opencore(oc) efiを使ってマックOSをbootすることをお勧めします.  


- 20200709:  
1.新しい　MLB,ROM,Serial numberをアップデートしました   
2.緊急修復に使うWRCOVERY.BINを添付しました、このファィルはrecoveryから抽出したものです  
使い方:SSDのESRにコピーして下さい

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/recovery.png?raw=true)   


すでにmacos 11 Bigsurにサポートしました  

## 正常に動作できるもの：
  
  
1.bluetooth（完璧に動作できる）From IntelBluetoothFirmware @zxystd

2.wifi （propertreeを使ってssidとpasswordを設定する必要がある） From itlwm @zxystd

3.sleep-wakeup 問題なし

4.hdmi（HDMIの音声も問題なし）

5.TrackPad 問題なし  

6.cfg lockを無効することで、パワーマネジメントが完璧に動作できる  

7.uhd620 問題なし  

8.cpu boost（cpufriend.kextに1800mhz，maximumを設定しました）  

9.usb（ssdtを用いて修復）

10.ホットキー(brightness and sound)  
11.audio jack(下に書いてある「ComboJackを用いてaudio jackを修復する方法」従う必要があります)

  
  
## 正常に動作できないもの：  


1.一部の付属カメラ（UVC Camera VendorID_1480 ProductID_975 は稼働できる） 

2.mx250/150/350（どうしても無理です）

  
## 自分のデバイス情報     
oc version:0.6.0  

macos：11.0 BigSur    

matebook13 2019 i7-8565u mx250 sn720  

## インストールの手順：  

下の外部ページを参考して下さい：  
（このガイドは最高のものですが、一定の英語能力が必要です）　　

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  

## もし手元にはマックOSのデイバスを持っていない場合：  
（上のガイドでは、インストールimgをダウンロードすることにマックOSのデバイス(Hackintosh可)が必要です）  

下のリンクからOSをインストールするに使うimgをダウンロード可能:  
https://blog.daliansky.net/macOS-Catalina-10.15.5-19F96-Release-version-with-Clover-5118-original-image-Double-EFI-Version-UEFI-and-MBR.html  
 
上記の外部ページは中国語で記載されていますので、chromeの翻訳機能をお勧めします.

上記のページでimgをダウンロードするリンクを速く見つかるために以下の文字をそのページでサーチして下さい:  

10.15.5 19F101 双EFI分区版
    
      
  
  

## ComboJackを用いてaudio jackを修復する方法
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)  

From Heporis:  　　

https://github.com/randomprofilename/ComboJack


1.私の倉庫から[ComboJack-master.zip(クリック)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ComboJack-master.zip)をダウンロード  
2.ターミナルでComboJack_Installer/install.shを実行します  
3.再起動します
  
  


## HIDPIを有効にする方法：

https://github.com/xzhih/one-key-hidpi
 

自分の例：  
1. enable HiDPi (with patch/inject EDID)ーーーーーーー 一番目のステップで"2"を選んで下さい
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  
  
  
## CFG lockを無効にする方法：


upgrade your bios to 1.28,could be downloaded in HUAWEI's official page    


1.Format a usb memory to fat32  

2.create a new floder named "EFI" at root  

3.create a new floder named "BOOT" At /EFI  

4.download [cfgunlock.zip(クリック)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)  

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
