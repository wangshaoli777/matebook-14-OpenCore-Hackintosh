# matebook-13/14-2019/2020-OpenCore 黑苹果 hackintosh 
  
  


其他语言（other luanguage version of readme）：  
[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)   
  
  
  
   
   
  
  
  
⭐️如果你不会安装，需要安装服务，联系微信ske1996  
可提供收费安装服务，帮你弄好一切可以弄好的驱动，并且保修1个月，非诚勿扰  
  
  
⭐️有问题只在github免费答疑，不在微信进行答疑，想白嫖请在github提交issue  
【想白嫖请在github提交issue】  
  

```diff
【此EFI可通用于2018-2020款的matebook13/14的intel版本。】
```  




姐妹项目:[Matebook-D14-2020-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-D14-2020-hackintosh)  
  
EFI下载地址：[releases](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  

如果你遇到了什么问题（与安装无关的），有可能在这里找到答案：[issues](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  

请在这个网页的最右上角帮我点颗小星星⭐️哟  




<details>  
<summary>⭐️点击查看使用效果</summary>  
  
![image](https://i0.hdslb.com/bfs/article/0d73e23780c4a4a5b80b1e956dc8957bb95f3372.jpg@1320w_880h.webp)  
![image](https://i0.hdslb.com/bfs/article/3c89fd7615510c1b2e9efa1c6024348b4b635abc.jpg@1320w_1760h.webp)  

</details>   



<details>  
<summary>⭐️点击查看如何在黑苹果下玩所有3A大作（matebook13/14的黑苹果🉑️）</summary>  
    
  
  
  
 ⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
       
      
我自己用的一个云电脑服务  
挺好用的能玩游戏（包括3A） 
也就是说在matebook13/14的黑苹果上也可以无硬件限制的玩任何游戏了  
直接4K全画质的开  
没啥延迟，就跟在本地玩一样  
我自己用的，推荐使用这个，这样在mac玩游戏也解决了  
  
⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
  
  
[点击进入它的官网](https://www.haixingcloud.com/#/Home)  
  

</details>   



       
<details>  
<summary>⭐️扫码进微信群(点击以查看二维码)</summary>  
⚠️点击以下链接，两个小问题全答对即可获得入群二维码  
  
注意:在国内的可能需要挂vpn才能访问  



[点击进入小问答](https://docs.google.com/forms/d/e/1FAIpQLSfNI8Zy9pfb6cASnH7yUk4QVuKxZWVobU9C_p7Vas2EXjVfEQ/viewform?usp=sf_link)  


</details>   
  
   



## 更新日志（⚠️一定先看这个）  
<details>  
<summary>点击以查看详细信息</summary>  
  

- 20200918:  
删除了两个fakepcid的驱动和一些其他东西，目前的efi非常的干净，另外修复了wifi与蓝牙冲突的问题  

- 20200917:  
使用了Z大的最新AirportItlwm的wifi驱动，跟heliport说拜拜啦，今后可以原生切换wifi了，另将oc升级至0.6.1  
bigsur跟catalina需要对号入座，不可串着用  


- 20200916:  
精简了很多kext跟ssdt，应该资源消耗会更少了，然后规范了一下config，并升级oc至官方0.6.1  


- 20200905:  
更新了一个小彩蛋进去，加了自动亮度的传感器驱动  



- 20200822:  
删除了一些没用的ssdt，精简了一下efi  
  
  
- 20200814:  
重做了一些ssdt，升级了一些驱动，然后对bigsur做了配适，0814的efi可以同时稳定引导bigsur跟catalina  

- 20200811:  
修复了0806的触摸板跟alc的问题  


- 20200806:  
更新oc至官方稳定版0.6.0  

    
- 20200728:  
添加了public beta的itlwm.kext和HeliPort.dmg  
在macOS下双击安装HeliPort.dmg  

- 20200725:  
已知本EFI可用于ota直升macos10.15.6，工作状况良好，因此本EFI可用于10.15.6

- 20200724:  
1.重新拆包分析了最新的1.28的bios，cfglock的偏移地址依旧是0x3E，因此教程依旧可用  
2.更新了关于HIDPI的注意事项  
3.更新oc至0.5.9  



- 20200715:  
耳机接口修复成功，已更新耳机接口修复教程，在下面就可以找到  

- 20200712:  
已知本efi可同时用于matebook 13/14 2019  
于2020版本测试情况如下：  
2020版本采用了第二代9560可以驱动，使用的驱动不同于2019版  

- 20200710:  
添加了配置好的clover的efi文件用于安装，虽然也可以用这个clover文件复制到esp分区用于引导   
但是强烈建议使用oc的efi引导你的hackintosh  

- 20200709:  
1.更改了三码  
2.添加了保险文件（WRCOVERY.BIN）  
用法：放入esr分区，与EFI文件夹并列即可

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/recovery.png?raw=true)
</details>


## 正常可用的部件：
  
 
<details>  
<summary>1.蓝牙（无需热启动）*点击查看详细说明</summary>   
  
驱动作者[@zxystd](https://github.com/OpenIntelWireless/itlwm)  
1. 华为的蓝牙鼠标不可用！！！  
2. 苹果的妙控2可用  
3. 有个可爱的小哥哥@Baiyu0124发现了一款可用的没什么牌子的鼠标[淘宝链接](https://m.tb.cn/h.VtTxb0H?sm=bfed64)   
4. 微软设计师鼠标可用[淘宝链接](https://detail.tmall.com/item.htm?id=575557854943&spm=a1z09.2.0.0.119c2e8dUqx3iI&_u=bkg3nm2911&sku_properties=5919063:6536025)  
</details>   

  
<details>  
<summary>2.wifi可用 *点击查看详细说明</summary>  
  
1. 使用了Z大的最新AirportItlwm的wifi驱动，跟heliport说拜拜啦  


2. 驱动作者[@zxystd](https://github.com/OpenIntelWireless/itlwm)  

</details>   

3.睡眠正常

<details>  
<summary>4.hdmi正常（可音频输出）*点击查看详细说明</summary>   
  
  [x]MataBook 13 2018-2020 什么都不用改  
  [o]MataBook 14 2019-2020 需要修改缓冲帧 [点击查看需要修改的内容](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/49)  
 </details>   

5.触摸板正常

6.[解锁cfg lock](https://github.com/ske1996/matebook-13-2019-oc-efi#%E8%A7%A3%E9%94%81cfg)后可完美原生电源管理

7.已注入缓冲帧 核显正常

8.cpu变频正常（补充：此efi内涵cpufriend，设置为：1800mhz，最高性能）

9.usb已定制（通过ssdt定制）

10.键盘快捷键正常  

11.耳机接口正常（需要使用下面的[【安装ComboJack实现耳机耳麦切换，改进电流声】](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/readme.md#%E5%AE%89%E8%A3%85combojack%E5%AE%9E%E7%8E%B0%E8%80%B3%E6%9C%BA%E8%80%B3%E9%BA%A6%E5%88%87%E6%8D%A2%E6%94%B9%E8%BF%9B%E7%94%B5%E6%B5%81%E5%A3%B0%E4%BF%AE%E5%A4%8D%E8%80%B3%E6%9C%BA%E6%8E%A5%E5%8F%A3)）

  
  
## 无法正常工作的部件：  


1.摄像头（UVC Camera VendorID_1480 ProductID_975这个可用）

2.mx250独显（这个是废话）

3.指纹不能用（这个也是废话）  


  
## 个人使用版本信息等   
<details>  
<summary>点击以查看详细信息</summary>  
oc版本0.6.0

自用macos版本：11.0 BigSur    

matebook2019 i7-8565u mx250 sn720
</details>  

## 安装方法&镜像下载&视频教程：  

<details>  
<summary>点击查看镜像下载</summary>  
先于此blog下载：10.15.5 19F101 双EFI分区版

这个文章很长，使劲往下翻，或使用网页搜索功能

下载链接
：https://blog.daliansky.net/macOS-Catalina-10.15.5-19F96-Release-version-with-Clover-5118-original-image-Double-EFI-Version-UEFI-and-MBR.html
  
</details>  

      
<details>  
<summary>点击查看安装视频教程</summary>

https://www.bilibili.com/video/BV1jJ41127YT/?spm_id_from=333.788.videocard.0
  
⭐️如果你不会安装，需要安装服务，联系微信ske1996
可提供收费安装服务，并且保修1个月  

有问题只在github免费答疑，不在微信进行答疑，想白嫖请在github提交issue，微信勿扰  
</details>  
  
  

<details>  
<summary>安装注意点</summary>  
⚠️事前准备：f2进bios，调成中文，然后关闭一切带有“安全”的东西，保存，退出  
  
1.安装使用的镜像推荐使用我给的链接下载的那个，不要用他给的，因为有点旧了  

2.视频的【03:57】他说把配置好的clover文件解压到这个文件夹下时，将我的库中的【安装用clover的EFI】放进去  

3.视频的【14:37】开始他开始吧u盘的clover efi复制进ESR（EFI）分区，这一步复制我的oc的efi进去。注意：这一步的efi跟第二步不一样，这一步用oc的

4.视频的【16:44】开始是使用easyuefi创建efi引导，这一步前面都跟他视频一样，他怎么点你就怎么点，只不过，选择引导文件为：EFI/BOOT/BOOTx64.efi
  
⭐️如果你不会安装，需要安装服务，联系微信ske1996  
可提供收费安装服务，帮你弄好一切可以弄好的驱动，并且保修1个月，收费200，非诚勿扰    
</details>

## 安装后：  


<details>  
<summary>安装ComboJack实现耳机耳麦切换，改进电流声。（修复耳机接口）</summary>   
  
参考： 

![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAk2FSNjwQUoIN0*GZw*WPuJGXoFx6QKbikJBN0lMTsBAB*.2jRAK8HeEs9KtxTHRjs!/b&bo=SAdMAgAAAAADByM!&rf=viewer_4)



在这里下载由Heporis制作的ComboJack.

https://github.com/randomprofilename/ComboJack


终端运行下面路径的脚本
```bash
ComboJack_Installer/install.sh
```
  
</details>

  
  
<details>  
<summary>开启HIDPI</summary>  
https://github.com/xzhih/one-key-hidpi
 

我说下我的选择：  
第一步选择 开启HiDPi（注入EDID）  
第二步选择 保持原样  
第三步选择 手动输入分辨率  
分辨率输入的是 1600x1066 1343x895 2160x1440  

- 最后说一句，开启了hidpi之后，在设置→显示器里不要让分辨率超过1343x895，最大只能到这个，因为超过这个会引发一些唤醒后屏幕显示的问题（比如唤醒后屏幕只显示到四分之三），而且不要觉得这个分辨率小，因为这个是hipdi分辨率，跟你理解的分辨率不一样，1343×895实际上等于你理解的一般分辨率的2686×1790，是超过2k的，如下图所示  

*注意⚠️你的1343x895这个分辨率的设置位置不一定是在【更大空间】  

![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAlT4PiIkTwV7VOQNDBpBB7OkqG1Id2.r35y0gnRAtugvhPBj1i6J0*cx1bGL996lhQ!/b&bo=NAV8AwAAAAADB2w!&rf=viewer_4)  

*注意⚠️你的1343x895这个分辨率的设置位置不一定是在【更大空间】

</details> 

  
  
<details>  
<summary>解锁CFG</summary>  

⚠️关于解锁cfg后能做到什么？  
完美的电源管理  
CPU完美变频  
完美睡眠（我个人经验：睡眠6H只掉了1%的电）  
⚠️以下教程的cfg lock偏移地址提取自matebook13/14 2019/2018款  
2020款的需要自行提取bios并自行分析，核对偏移地址  
如因以下教程修改导致的一切后果，本人不予承担责任，下载本repo中任何一个文件视为同意以上条款  


以下教程来自：  
https://zhuanlan.zhihu.com/p/121655468

先去华为官网升级bios至1.28

然后找偏移地址就不用做了，我告诉你，就是0x3E  

【⚠️千万不要用oc去引导ru！！】懂得人自然懂，收起那个想法，老老实实按我下面写的来  
⚠️以下教程的cfg lock偏移地址提取自matebook13/14 2019/2018款  
2020款的需要自行提取bios并自行分析，核对偏移地址  
如因以下教程修改导致的一切后果，本人不予承担责任，下载本repo中任何一个文件视为同意以上条款  

- U盘准备阶段：  
（大小无所谓）  

1.先准备一个u盘，格式化为fat32  
2.u盘里创建文件夹：EFI  
3.打开EFI文件夹，在里面创建文件夹BOOT  
4.复制[cfgunlock.zip(点击下载)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)里面的bootx64.efi进U盘的EFI/BOOT下  
5.关机后开机按F12使用这个U盘去引导，然后进入修改bios底层阶段  

- 以下为修改bios底层阶段：  
1. 进入后 ‘alt’ + ’=‘ 切换进 ACPI Variable  
2. 用pageup/pagedown/上下方向键找到 CPUSetup  
3. 回车进入然后用上下左右方向键找到对应的地址（也就是0x3e，那么就是纵坐标03，横坐标0e的位置）  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAl40wvQBwENCvcC8AXw3U9pLndZFaQGhnrwveoEM7FzByVHyIsV*u1nI.1JoXvOXOA!/b&bo=0AIQAgAAAAABB.A!&rf=viewer_4)  
4. 一看，确实是0x01，那么回车，输入0 就可以看到它变成了0  
5. 使用'crtl' + 'w' 来保存 保存的时候屏幕上会直接显示update written 的，这说明已经写入了  
6. 使用'alt' + 'q' 来退出，然后即可回到引导进入系统了，CFG已经解锁  

</details> 

      

<details>  
<summary>解决window与macos时间不同步/显示不正确</summary>  
  
  
  
在windows下面WIN+x 选择管理员模式进入CMD  
  
  执行以下命令：  
  
```bash
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```  
</details>   
  
   

<details>  
<summary>关于如何在黑苹果下玩游戏（打破平台/硬件限制，黑苹果也能玩所有PC游戏）</summary>  
    
  
  
  
 ⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
       
      
我自己用的一个云电脑服务  
挺好用的能玩游戏（包括3A） 
也就是说在matebook13/14的黑苹果上也可以无硬件限制的玩任何游戏了  
直接4K全画质的开  
没啥延迟，就跟在本地玩一样  
我自己用的，推荐使用这个，这样在mac玩游戏也解决了  
  
⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
  
  
[点击进入它的官网](https://www.haixingcloud.com/#/Home)  
  


</details>   




## 如果想打赏小的，请选择一个你喜欢的方式打赏五块钱，谢谢！
  
  ⭐️打赏附言请留下自己的github的ID，用于公示感谢  
  



![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5vhyua0NyktT47EDwPAfhtuBceWLK5.5V40I*6lQE5rORR7qbWTf9Eovur4ifsHKECewZxvEqi.ZfhaQ4ObpAl8!/b&bo=DQWcAw0FnAMBCS4!&rf=viewer_4)  


  
[看不到图片请点击](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5vhyua0NyktT47EDwPAfhtuBceWLK5.5V40I*6lQE5rORR7qbWTf9Eovur4ifsHKECewZxvEqi.ZfhaQ4ObpAl8!/b&bo=DQWcAw0FnAMBCS4!&rf=viewer_4)  

    
    
  
  
如果可用请在issues中提交你的机器信息（年份，cpu，matebook13还是14）  
用于构建更好的efi

## 感谢：

- @intel 感谢10年一管牙膏

- @apple 感谢创造出macos

- [@zxystd](https://github.com/OpenIntelWireless/itlwm) 感谢创造出wifi以及蓝牙的驱动

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) 教会了我很多东西

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh) 我做黑苹果的入门引路人 感谢他在matebook13的clover版efi上的杰出贡献

- [@Zero-zer0](https://github.com/Zero-zer0) 参考了他的热键修复方法 十分感谢

