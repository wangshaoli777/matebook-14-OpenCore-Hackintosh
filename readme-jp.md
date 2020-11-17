# matebook-13/14-2019/2020-OpenCore-EFI  ハッキントッシュ  

他言語（readme in other language）：  
[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)   

issueなどの提出には日本語でokay!  

```
このプロジェクトは2018-2020バージョンのMatebook 13&14に対応しています。（intelのみ）
```

このページ右上のStar⭐️をクリックしてくれれば嬉しいです。  

このプロジェクトはcatalinaとbigsurに対応しています。  

Report & Feedback：[issues](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  


EFI download：[releases](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  



関連プロジェクト:[Matebook-D14-2020-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-D14-2020-hackintosh)  

<details>  
<summary>⭐️クリックしてハッキントッシュの稼働状況を確認</summary>  
  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88%202020-11-14%2019.30.41.png?raw=true)    
![image](https://i0.hdslb.com/bfs/article/0d73e23780c4a4a5b80b1e956dc8957bb95f3372.jpg@1320w_880h.webp)  
![image](https://i0.hdslb.com/bfs/article/3c89fd7615510c1b2e9efa1c6024348b4b635abc.jpg@1320w_1760h.webp)  

</details>   

       

## アップデート履歴:  
<details>  
<summary>クリック(⚠️これを先に読んでください)</summary>  
  
- 20201113:  
全てのBigSurバージョンのEFIに含まれているOpenCoreを0.6.4にアップグレードしました、正式版のBigSur 11.0.1まで対応します。  

- 20201106:  
MB13&14 2018-2019(bigsur ver)に含まれているOpenCoreを0.6.3にアップフレンドしました。  

  
- 20200918:  
二つのfakepcidのkextと一部の無意味のものを削除し、さらにwifiとbluetoothの衝突issueの解決を試しましたが、100％の解決とは言えないかもしれません。    

- 20200917:  
最新のAirportItlwmを使用していますので、これからheliportは必要なくなります、さらにOCを0.6.1にアップグレードしました  
bigsurとcatalinaのEFIファイルを分けましたので、自分のOSバージョンに応じてダウンロードする必要があります。  




- 20200916:  
delete more useless kext and ssdt,this version will take less ram,and upgrade opencore to 0.6.1  

 
- 20200905:   
イースター・エッグが含まれています+SMCLightSensor.kext  

 
 
- 20200822:  
一部の無意味のssdtを削除しました。  

  
- 20200814:  
V0814のEFIはcatalinaとbigsur両方をbootできるようにしました、一部のssdtを作り直しました。  

- 20200806:  
OpenCoreをオフィシャルの0.6.0にアップグレードしました。  


- 20200802:  
updated itlwmx.kext for 2020ver laptop,[click for download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/itlwmx%20beta0802.zip) 

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

</details>  
すでにmacos 11 Bigsurにサポートしました  

## 正常に動作できるもの：

1.bluetooth（完璧に動作できる）From IntelBluetoothFirmware @zxystd

2.wifi  From [@zxystd](https://github.com/OpenIntelWireless/itlwm)  

3.sleep-wakeup 問題なし

<details>  
<summary>4.hdmi（HDMIの音声も問題なし）*クリック</summary>   
  
⭕️MataBook 13 2018-2020 そのまま使えます。  
❌MataBook 14 2019-2020 config.plistのFramebuffer部分を [この内容に変更する必要があり](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/49)  
ただし、MataBook 14ではそのままに使えるケースもありますので、もしHDMIに問題がなければ、config.plistを編集しないのがおすすめです。  

 </details>   
 
5.TrackPad 問題なし  

6.cfg lockを無効することで、パワーマネジメントが完璧に動作できる  

7.uhd620 問題なし  

8.cpu boost（cpufriend.kextに1800mhz，maximumを設定しました）  

9.usb（ssdtを用いて修復）

10.ホットキー(brightness and sound)  

11.audio jack(下に書いてある「ComboJackを用いてaudio jackを修復する方法」従う必要があります)


  
## 正常に動作できないもの：  


1. 一部の付属カメラ（UVC Camera VendorID_1480 ProductID_975 は稼働できる）  
*If you need a workable webcam,buy Logicool c270,I'm using it,pretty good.  

2. mx250/150/350（どうしても無理です)  
  
3. 指紋認証  


  
## 自分のデバイス情報     

oc version:0.6.4  

macos: BigSur 11.0.1 Public Release  

matebook13 2019 i7-8565u mx250 sn720  



## インストールの手順について：  
<details>  
<summary>インストールガイド</summary>   
    
    
下の外部ページを参考して下さい：  
（このガイドは最高のものですが、一定の英語能力が必要です）　　

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  
</details>   
 
<details>  
<summary> How to create dual boot：</summary> 

[click to download the guide](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/A%20guide%20for%20dualBoot%20of%20Matebook13%20from%20%40Francisco%20Novoa.pdf)  

Thanks [@Francisco Novoa(from Chile🇨🇱)](https://t.me/hackintosh_matebook13/8557) and this dual-boot guide is written by him   


</details>  
 


<details>  
<summary>For someone wants to run BigSur on his/her device</summary> 


1. OTA works for upgrading to BigSur from Catalina  
2. However you get BigSur install on your device,I recommand you to unlock CFG at frist for avoiding some problem you maybe get.  
3. Before you upgrade your osx to BigSur from Catalina,you should remove your EFI in you ESP partition and switch to BigSur version EFI which is publiced in my [release](https://github.com/ske1996/matebook-13-2019-oc-efi/releases).  




</details>  


## インストール後

  
<details>  
<summary>⚠️Warning</summary>  
⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️  
  
1.DO NOT BOOT YOUR WINDOWS OR OTHER OS WITH OpneCore.  
you may lose your Genuine license,except you know how to inject your own correct UUID/MLB/SN(which is written at your bios or some other parts of motherboard,and it is unique)in config.plist.  
it is not 100% happen,but it is still risky.  
you should just set Macos as defaul boot at OpenCore with pressing ctrl + enter to choose Mac partition.  
and edit config to disable "showpicker" which is at EFI/OC.  
then press F12 immediately after you press power button,and choose the option named like "windows xxxx" to boot windows with original uefi bootloader.  
Or follow that guide "how to create dual boot" upper this page.  
In my opinion,i dont think GUI of choosing os is necessary,i set it just boot macos as default with ctrl + enter to choose mac partition and disabled showpicker at config.  
F12 in just when you need to switch os.  
I think there is no one will switch os like over than 10 times per day.  
You dont have to use the boot menu everytime,is it great that it automaticlly enter to the os which you always use,and just in you need to switch os to see the boot menu？ 

2.You should edit the config.plist to customize MLB/SN/UUID which is unique before you start to use your laptop as daily pc.  

3.Do not enable "serch my mac" in setting.  

</details>  




<details>  
<summary>ComboJackを用いてaudio jackを修復する方法</summary>   

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)  

From Heporis:  　　

https://github.com/randomprofilename/ComboJack


1.私の倉庫から[ComboJack-master.zip(クリック)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ComboJack-master.zip)をダウンロード  
2.ターミナルでComboJack_Installer/install.shを実行します  
3.再起動します
  
  
</details>   


<details>  
<summary>HIDPIを有効にする方法：</summary>   
    
⚠️気をつけてください：  
OSのバージョンに応じて、使うプログラムが異なります     
BigSur：[click to download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/Bigsur/%EF%BC%88BigSur%E6%96%B9%E6%A1%882%EF%BC%89hidpi.zip)  
Catalina：https://github.com/xzhih/one-key-hidpi  

 

自分の例：  
1. enable HiDPi (with patch/inject EDID)ーーーーーーー 一番目のステップで"2"を選んで下さい
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  


HiDPIをオンにしてから、システム環境設定/ディスプレイで解析度を1343x895に設定し、永遠にこの解析度に固定してくだい、他の解析度に設定しますと、BUGが出てきます。

*注意⚠️画像の左の部分を見てください、その1343x895が正しいです。しかし、右の選択肢に関しては、必ず画像と同じ位置ではありませんので注意してください。  


![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAlT4PiIkTwV7VOQNDBpBB7OkqG1Id2.r35y0gnRAtugvhPBj1i6J0*cx1bGL996lhQ!/b&bo=NAV8AwAAAAADB2w!&rf=viewer_4)  

*注意⚠️画像の左の部分を見てください、その1343x895が正しいです。しかし、右の選択肢に関しては、必ず画像と同じ位置ではありませんので注意してください。 




</details>   
  
  

<details>  
<summary>CFG lockを無効にする方法：</summary>   
  
⚠️CFG lockを無効にしたら、どんなことができる？  

完璧なパワー管理  
バッテリーライフがある程度長くなる  
スリープでの電力消費がさらに減少する  
  
  
⚠️  

まずはHUAWEIの公式サイトでBIOSを1.28にアップグレードするためのパッケージをダウンロードし、BIOSをアップグレードします。   


1.USBメモリ（容量には最低制限なし）をfat32にフォーマットする

2.USBメモリのルートで名前が"EFI"のフォルダを作る  

3.EFIフォルダ内に名前が"BOOT"のフォルダを作る  

4.[cfgunlock.zip(クリック)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)をダウンロード  

5.cfgunlock.zip内のbootx64.efiをEFI/BOOTにコピー 

そして、そのusbメモリーを用い、BOOT（起動）する  

usbメモリーを用いて起動後   

altと＝を同時に押す  
(異なる言語のキーボード間では、キーの配置が異なる。私のキーボードは標準USA英語のものなので、このガイドも私のキーボードに基づいて書いたもので、日本語キーボードバージョンのPCを利用している人は外付けのUSA英語のキーボードを使ってください)  

ACPI Variable の画面で↑/↓の矢印キーを用いて"cpusetup"のオプションを探す（大体3ページ目にある）  


見つかったら、enterキーで"cpusetup"に入る  

そちらの画面は以下の画像と同じはず  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/RU.jpg?raw=true)

  
0030-0E（縦0030、横0E）は01のはず  

←→↑↓の矢印キーを使い、0030-0Eをピックして"00"を入れ替える  

ctrl+wでチェンジを保存  

保存に問題がなければ,"update written"のようなことが提示する  

alt+qで退出してOSに切り替える  

このあとはもう一度そのUSBメモリで起動し、修正した部分がちゃんとできたどうかをチェックする。  
そして[propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip)を利用し、ESP partitionでEFI/OC/config.plistのkernel/add/quirksを以下のようにチェンジすることをおすすめ：  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5mhOVTuQ0sSbBPmet1ZSU1zDz7zUBccaFytwrKxAqPz4ygQph98Mo9E5.JjYf6DFuuWhDZs8DFFN1ujnFI9OIz4!/b&bo=wASKAwAAAAADB28!&rf=viewer_4)  

</details>   

<details>  
<summary>dvmtを64mbに拡大する</summary>  
    
  ⚠️dvmtを64mbに拡大したら、どんなことができる？  
  hdmi/dpで4k60pまでに対応できる  
  p.s.　デフォルトは4k30p
  
  
 基本的には前のCFGのガイドと同じ  

[cfgunlock.zip](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)内のbootx64.efiを含むusbメモリーを用いて起動後   

altと＝を同時に押す  
(異なる言語のキーボード間では、キーの配置が異なる。私のキーボードは標準USA英語のものなので、このガイドも私のキーボードに基づいて書いたもので、日本語キーボードバージョンのPCを利用している人は外付けのUSA英語のキーボードを使ってください)  

ACPI Variable の画面で↑/↓の矢印キーを用いて"Sasetup"のオプションを探す  


見つかったら、enterキーで"SaSetup"に入る  

crtl+pagedownで次のページに変更する  
この時の画面は下の画像と同じはず（縦の1番目の座標は0100）  
  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/%E6%9D%82%E9%A1%B9/dvmt64.bmp)  

4. 縦0100横07を02に，縦0100横08を03に変更する（矢印キーでオプションをピック、enterを押す、数字を入力）  

5. Crtl+wで保存  

このあとはもう一度そのUSBメモリで起動し、修正した部分がちゃんとできたどうかをチェックする。  
そして[propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip)を利用し、ESP partitionでEFI/OC/config.plistのDeviceProperties/Add/PciRoot(0x0)/Pci(0x2,0x0)を以下のようにチェンジすることをおすすめ：  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/45NBuzDIW489QBoVep5mcbvyqMw5*Y0jP8mcu7Ee3hom9v.4vLrclVXlW1qZQR3tuWj.fDrSEOF5cBubLM5p6joREA5a6pqrLmFG0msz5yg!/b&bo=0AQsAgAAAAADJ*g!&rf=viewer_4)  
  
  
このdvmtガイドは[@laozhiang](https://github.com/laozhiang)の発想に基づき、完成したものである  
  


</details>         
      

もし、このEFIファイルはあなたのデバイスでうまく動作できるなら、このプロジェクトでissuesを提出して下さい  
件名は：matebook 13か14か、2019か2020か、CPUは何か。例：matebook 14 2019 I7 8565u  
自分のデバイスでハッキントッシュをしたい他のユーザに対し、いい参考になりますので、ご協力を御願いします。



## If you want to support my work：

Please donate in paypal  

[click to donate](https://paypal.me/ske1996)  

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/paypal.png?raw=true)  

[click to donate](https://paypal.me/ske1996)  



## Thanks：

- [@intel](https://www.intel.com/content/www/us/en/homepage.html) 素晴らしいCPUを生産してくれてありがとう（AMD,YES!）

- [@apple](https://www.apple.com/) この素晴らしいMACOSにご褒美を！
 
- [@zxystd](https://github.com/OpenIntelWireless/itlwm) WIFI＆Bluetoothのドライブソフトの開発者、感謝！  

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) 色々OpenCoreのことを教えてくれて、感謝！

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)  MateBook 13のCloverバージョンのhackintoshで素晴らしいものを完成した、感謝！  

- [@Zero-zer0](https://github.com/Zero-zer0) 彼に輝度と音量のホットキーの修復方法を参考した、感謝！
