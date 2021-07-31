# matebook-13/14-2019/2020-OpenCore-EFI  ハッキントッシュ  

  
[![issue](https://img.shields.io/github/issues/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  [![forks](https://img.shields.io/github/forks/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/network/members) [![star](https://img.shields.io/github/stars/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/stargazers) [![Download](https://img.shields.io/badge/OpenCore%20EFI%20files%20download-4.2k-blue)](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  



他言語（readme in other language）：  
[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)   


**HUAWEI社のMateBookシリーズのlaptopでApple社のMacOSをほぼ完璧に稼働させる手順及び必要なBOOTファイルが含まれています。**  



```
このプロジェクトは2018-2020バージョンのMatebook 13&14に対応しています。（intelのみ）
```

このページ右上のStar⭐️をクリックしてくれれば嬉しいです。  


関連プロジェクト:  
[Matebook-x-pro-2019-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-x-pro-2019-Hackintosh-newest/blob/main/readme-en.md)  
[Matebook-D14/D15-2020-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-D14-2020-hackintosh)  
[matebook-x-2020-Hackintosh-OpenCore-黑苹果   ](https://github.com/ske1996/matebook-x-2020-Hackintosh-OpenCore/blob/main/readme-en.md)  



<details>  
<summary>⭐️ここをクリックしてハッキントッシュの稼働状況を確認</summary>  
 
[サンプル動画](https://www.bilibili.com/video/bv18z4y1U7rz)  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/Monterey%20review.png?raw=true)   

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88%202020-11-14%2019.30.41.png?raw=true)    
![image](https://i0.hdslb.com/bfs/article/0d73e23780c4a4a5b80b1e956dc8957bb95f3372.jpg@1320w_880h.webp)  
![image](https://i0.hdslb.com/bfs/article/3c89fd7615510c1b2e9efa1c6024348b4b635abc.jpg@1320w_1760h.webp)  


[サンプル動画](https://www.bilibili.com/video/bv18z4y1U7rz)  

</details>   

Report & Feedback：[![issue](https://img.shields.io/github/issues/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  

  
EFI download：[![Download](https://img.shields.io/badge/OpenCore%20EFI%20files%20download-4.2k-blue)](https://github.com/ske1996/matebook-13-2019-oc-efi/releases) 



## アップデート履歴:  
<details>  
<summary>ここをクリック(⚠️これを先に読んでください)</summary>  


- 20210508:  
changed some value in boot-args and framebuffer，try to optimize drm and sidecar.    

- 20210426:  
OpenCore's version is still in 0.6.5,but I've rebulit all of EFI files,no longer differentiate EFI files for Catalina or BigSur from right now,upgraded Airportitlwm to 1.3 stable,and added a property "force-online 01000000" to framebuffer    

- 20210317:  
I wont upgrade anything until it will be necessary to do(likes apple changed their secure boot policy,so you have to use latest opencore to boot etc.),it still works well on even lastest version of macos(11.2.3 when i wrote this). so,see you in next necessary-upgrade version.  


- 20210130:  
全てのBigSurバージョンのEFIに含まれているOpenCoreを0.6.5にアップグレードしました，一部のkextもアップグレードしました，さらにboot chimeをオンにしました。 

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

</details>  
<details>  
<summary>About booting MacOS 12 Monterey</summary>  

【Yes,we can boot it.】  

Whatever you want to upgrade your hackintosh from BigSur,or new-installing.

need to do:  
upgrade your lilu and replace your airportitlwm and intelbluetoothfirmware to lastest ones,
disable intelbuletoothinjector and add bluetoolfix to oc/kexts/ and config.plist.
then,OTA or new-installing your OS with apple's guide.

Every thing works like in BigSur,but need to replace some kext.

My experience: [click this](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/155)  


   
</details> 


**Supported BigSur and Monterey already**  

## 正常に動作できるもの：

**click "Bluetooth" for more information**    

<details>  
<summary>1.ブルートゥース</summary>   
  
Thanks[@zxystd](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)  
1. HUAWEI bluetooth mouse doesnt work.   
2. Airpods works,but need pairing.    

A list of workable bluetooth mouse:https://github.com/ske1996/matebook-13-2019-oc-efi/issues/156  


</details>   


2. wifi  

3. sleep-wakeup  

4.HDMI  

5. トラックパッド  

6. パワーマネジメント  

7. GPU(UHD 620)  

8. CPU Boost  

9. USB Mapping　　

10. ホットキー(brightness and sound)  

11. audio jack  


  
## 正常に動作できないもの：  


1. 一部の付属カメラ（UVC Camera VendorID_1480 ProductID_975 は稼働できる）  
*If you need a workable webcam,buy Logicool c270,I'm using it,pretty good.  

2. mx250/150/350（どうしても無理です)  
  
3. 指紋認証  




## インストールの手順について：  

**下記の項目の文字をクリックすることで、詳しい内容が見えますよ。**  


<details>  
<summary>⚠️Preprocessing：inject SSN,UUID,ROM,MLB (click for details)</summary>  
There were lots of people who installed MacOS without injecting his "SSN,UUID,ROM,MLB" at frist,and that caused Apple service of his apple id blocked.  
So,I made some changes that if you dont inject your "SSN,UUID,ROM,MLB" at frist,you cant boot your hackintosh or installing-processing.  
Google how to do it by yourself.    
But I provide a config editor:  
  
[ProperTree-windows.zip](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree-windows.zip)  
[Propertree-macos](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip)   


  
  
</details>   

<details>  
<summary>インストールガイド</summary>   
    
    
下の外部ページを参考して下さい：  
（このガイドを読むのには、一定の英語能力が必要です）　　

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  
</details>   
 
<details>  
<summary> Dual bootの作り方：</summary> 

[クリックしてガイドブックをダウンロード](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/A%20guide%20for%20dualBoot%20of%20Matebook13%20from%20%40Francisco%20Novoa.pdf)  

*このガイドブックは英語で作成されたため、読むには一定の英語能力が必要です。  

Thanks [@Francisco Novoa(from Chile🇨🇱)](https://t.me/hackintosh_matebook13/8557) and this dual-boot guide is written by him   


</details>  
 


<details>  
<summary>MacOS 11.0 BigSurを利用したい人へ:</summary> 


1. CatalinaからBigSurへのアップグレードにはOTA方式で実行可能.  
2. BigSurをどうインストールするにもかかわらず、その前にCFG Lockをアンロックすることがおすすめ.  
3. CatalinaからBigSurへのアップグレードしたい人に対して、アップグレードのプロセスを始める前に、ESPのpartitionをmountして、その中のEFIフォルダを私の[release](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)でのBigSurバージョンに対応するものを変える必要がある.  




</details>  



## インストール後  



**下記の項目の文字をクリックすることで、詳しい内容が見えますよ。**  
  
<details>  
<summary>⚠️Warning</summary>  
⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️  
  
1. OpencoreでMacOS以外のOS(Windows,linuxを含む)をbootしないこと.  
純正ライセンスをその操作により失うリスクがある,UUIDなどを正しくconfig.plistに注入するやり方をわかるなら論外.  
上記のリスクが必ず発生するわけではないですが、そうしないのがおすすめです.  
opencoreのOS選択画面でctrl + enterを同時に押すことでMacOSのpartitionを選ぶことより、MacOSをデフォルトbootに設定する.  
その後、MacOSに入ってから、ESPのpartitionをmountして、EFI/OC/config.plistをpropertreeで開き、その中の"showpicker"オプションをOFF(False)に設定する.  
これで、一旦マシンを起動すると、opencoreのOS選択画面を自動的にスキップし、直接的にMACOSに入る.  
Double bootの人に対して、もしMacOS以外のOS(Windows,linuxを含む)に切り替えたい時には、起動ボタンを押した後にすぐにF12を連打することで、オリジナルのuefi boot managerに入ることができ、そこでMacOS以外のOS(Windows,linuxを含む)を選べばいい。

2. daily pcとして使用し始める前に、ESPのpartitionをmountして、EFI/OC/config.plistをpropertreeで開き、MLB/SN/UUIDを独自のものに変えるのを忘れないこと.  

3. MACOSのシステム環境設定のapple idのところで"serch my mac"をオンにしないこと.  

4. MACOSのシステム環境設定の"セキュリティーとプライバシー"のところで"file vault"をオンにしないこと.  


</details>  




<details>  
<summary>ComboJackを用いてaudio jackを修復する方法</summary>   

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)  

From Heporis:  　　

https://github.com/randomprofilename/ComboJack


1.このrepoから[ComboJack-master.zip(クリック)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ComboJack-master.zip)をダウンロード  
2.ターミナルでComboJack_Installer/install.shを実行します  
3.再起動します
  
  
</details>   


<details>  
<summary>HIDPIを有効にする方法：</summary>   
    
⚠️気をつけてください：  
OSのバージョンによって、これから使うプログラムが異なります     
BigSur：[click to download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/Bigsur/%EF%BC%88BigSur%E6%96%B9%E6%A1%882%EF%BC%89hidpi.zip)  
Catalina：https://github.com/xzhih/one-key-hidpi  

 

自分の例：  
1. enable HiDPi (with patch/inject EDID)ーーーーーーー 一番目のステップで"2"を選んで下さい
2. macbook pro   
3. 6番目のオプションを選ぶ    
5. ”1600x1066 1343x895 2160x1440”をこのままに入力  


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
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/cfgunlosk.png?raw=true)  

</details>   

<details>  
<summary>dvmtを64mbに解禁する</summary>  
    
  ⚠️dvmtを64mbに解禁したら、どんなことができる？  
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

At last,dont forget to remove these three properties which are named “framebuffer-fbmem” “framebuffer-stolenmem” “framebuffer-unifiedmem” in framebuffer part of config.plist with [propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip).  
  
このdvmtガイドは[@laozhiang](https://github.com/laozhiang)の発想に基づき、完成したものである  
  


</details>         
      


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
