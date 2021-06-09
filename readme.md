# matebook-13/14-2019/2020-OpenCore 黑苹果 hackintosh 
  
[![issue](https://img.shields.io/github/issues/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  [![forks](https://img.shields.io/github/forks/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/network/members) [![star](https://img.shields.io/github/stars/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/stargazers) [![Download](https://img.shields.io/badge/OpenCore%20EFI下载-4.2k-blue)](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  


  
readme in other language：  
[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)   
  
  
  
   

**在华为的MateBook系列笔记本上做到基本完美的稳定运行MacOS**     
  

```diff
此repo可通用于2018-2020款的matebook13/14的intel版本
```  

**⭐️如果你不会安装，需要安装服务，可以解决PM981问题** [点击进入我的淘宝店铺](https://item.taobao.com/item.htm?spm=a2oq0.12575281.0.0.45e51debf0yJ4n&ft=t&id=638314994173)  


<details>  
<summary>⭐️点击查看使用效果</summary>  
  
[点进这里查看演示视频](https://www.bilibili.com/video/bv18z4y1U7rz)  


![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/Monterey%20review.png?raw=true)   
  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88%202020-11-14%2019.30.41.png?raw=true)   

![image](https://i0.hdslb.com/bfs/article/0d73e23780c4a4a5b80b1e956dc8957bb95f3372.jpg@1320w_880h.webp)  
![image](https://i0.hdslb.com/bfs/article/3c89fd7615510c1b2e9efa1c6024348b4b635abc.jpg@1320w_1760h.webp)  
[点进这里查看演示视频](https://www.bilibili.com/video/bv18z4y1U7rz)  

</details>   



姐妹项目:  
[Matebook-x-pro-2019-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-x-pro-2019-Hackintosh-newest)  
[Matebook-D14/D15-2020-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-D14-2020-hackintosh)  
[matebook-x-2020-Hackintosh-OpenCore-黑苹果   ](https://github.com/ske1996/matebook-x-2020-Hackintosh-OpenCore)  
   

如果你遇到了什么问题,有可能在这里找到答案：[![issue](https://img.shields.io/github/issues/ske1996/matebook-13-2019-oc-efi?style=plastic)](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)    

<details>  
<summary>关于引导MacOS 12 Monterey</summary>  
先说结论：可，无论是OTA升级，或者是全新安装。  
微调一下config就行，不需要更新东西。
编辑config，给boot-args加上-lilubetaall，然后在kernel/add里禁用wifi驱动以及两个蓝牙驱动，做完后记得reset nvram。  
就可以去按照apple所要求的流程去OTA了。  

蓝牙Wi-Fi暂时没法用，其他都还好。  

具体参考：[我更新的经验以及效果](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/155)  


   
</details> 


**请在这个网页的最右上角帮我点颗小星星⭐️哟**  

## 更新日志（⚠️一定先看这个）  
<details>  
<summary>点击以查看详细信息</summary>  
  

- 20210508:  
oc版本为0.6.5，微调缓冲帧以及boot-args，尝试优化drm以及sidecar问题。  

- 20210426:  
oc版本依旧0.6.5，重新整合了一下各个efi，从现在开始不再去区分Catalina和BigSur，更新Airportitlwm至1.3 stable，另外缓冲帧加上了force-online参数   

- 20210317:  
这个不是【更新梗概】，0.6.5在我看来目前已经可以满足bigsur的引导需求（写下此日志时至11.2.3），苹果如果在secure或者是boot上没有做更改的话，oc的核心组件感觉没有更新的必要了。0.6.6开始默认直接跳过，直到有必要更新为止   
  
- 20210130:  
更新了所有efi的BigSur版本的oc至0.6.5，以及更新了一些驱动，并且打开了boot chime   

- 20201113:  
更新了所有efi的BigSur版本的oc至0.6.4，支持11.0.1正式版    

- 20201106:  
更新了MB13/14的2018-2019的BigSur版本的oc至0.6.3    
  
- 20201031:  
更新了MB13/14的2018-2019的BigSur版本的oc至0.6.2  


- 20200926:  
姑且做了一个分类，你可以根据自己的机器下载对应efi了，oc版本姑且是0.6.1，但是日后我主要维护的是matebook 13&14 2019版的  

- 20200918:  
删除了两个fakepcid的驱动和一些其他东西，目前的efi非常的干净，另外尝试修复wifi与蓝牙冲突的问题  

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



</details>


## 正常可用的部件：
  
**以下的【蓝牙】【WIFI】【HDMI】的文字可点击后查看详情**  

 
 
<details>  
<summary>1.蓝牙</summary>   
  
驱动作者[@zxystd](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)  
1. 华为的蓝牙鼠标不可用！！！  
2. 苹果的妙控2可用   
3. 亲眼所见，微软设计师鼠标可用[淘宝链接](https://detail.tmall.com/item.htm?id=575557854943&spm=a1z09.2.0.0.119c2e8dUqx3iI&_u=bkg3nm2911&sku_properties=5919063:6536025)  
4. 亲眼所见，型号为thinkpad 0a36193（SMB）的蓝牙鼠标可用，购买选“蓝牙无线激光”，[京东链接-移动端](https://item.m.jd.com/product/748175.html?utm_campaign=t_1001328990)  
5. Airpods可以用，但是你得配对一次，我们又不是白苹果，不能开盖就用  
6. 以下几个蓝牙鼠标根据群友测试说可用，但是我没亲眼所见，要是买了发现不能用别怪我  
----雷柏m200g/刺鳞树蝰/罗技m336/微软sculpt/英菲克/飞利浦spk7355  

</details>   

  
<details>  
<summary>2.WIFI</summary>  
  
1. 使用了Z大的最新AirportItlwm的wifi驱动，跟heliport说拜拜啦  


2. 驱动作者[@zxystd](https://github.com/OpenIntelWireless/itlwm)  

3. Airdrop和无线的随航不可用，随航需要插线用，handoff可用但有时不太稳定，可以用apple watch解锁mac，但是有时不稳定  
4. Wi-Fi觉得不好使的去上面我写出来的作者的repo里更新驱动
5. Wi-Fi连接要尽可能的去连5ghz的
6. 从Windows切换过来MacOS发现wifi没法用就关机，10s后再开机

</details>   

3.睡眠正常

<details>  
<summary>4.HDMI </summary>   
  
⭕️MataBook 13 2018-2020 什么都不用改  
❌MataBook 14 2019-2020 需要修改缓冲帧 点击右侧查看需要修改的内容：[Plan A](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/49) |  [Plan B](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/121)   
但是不是100%都需要改，我也见过一些没有更改缓冲帧部分就能很好驱动的案例，按需吧，不一定  

 </details>   

5.触摸板正常

6.完美原生电源管理

7.核显

8.CPU变频

9.USB定制

10.键盘快捷键正常  

11.耳机接口以及声卡扬声器正常 layout:21  
  
## 无法正常工作的部件：  


1. 摄像头（UVC Camera VendorID_1480 ProductID_975这个可用）  
*如果你无论如何都需要一个在mac下工作的摄像头，吐血推荐罗技c270，我天天用  


2. mx250独显（这个是废话）

3. 指纹不能用（这个也是废话）  


 

## 有关安装：  



⚠️事前准备1：f2进bios，调成中文，然后关闭一切带有“安全”的东西，保存，退出  

<details>  
<summary>⚠️事前准备2：安装前先定制三码（点击查看详情）</summary>  
因为很多人都不替换自己的三码就用，所以导致苹果账号服务受限的情况比比皆是，因此，我把config设置为“如果不改三码就用，那直接无法启动”  
具体修改三码的教程自己百度，自己编辑config。（p.s.其实应该四码，包含：SSN，MLB，ROM，UUID） 
  
windows下编辑config的工具：[ProperTree-windows.zip](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree-windows.zip)  
  
  
</details>  

[![Download](https://img.shields.io/badge/OpenCore%20EFI下载-4.2k-blue)](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  

镜像下载链接：https://blog.daliansky.net/  

OC官方教程:https://dortania.github.io/OpenCore-Install-Guide/  
  


**⭐️如果你不会安装，需要安装服务，** [点击进入我的淘宝店铺](https://item.taobao.com/item.htm?spm=a2oq0.12575281.0.0.45e51debf0yJ4n&ft=t&id=638314994173)  




## 安装后：  

**以下的文字可点击后查看详情**  


<details>  
<summary>⚠️注意事项</summary>  
⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️  
  
1. 不要用oc引导windows，因为你弄不好你的正版软件许可证就全没了  
直接oc的选择系统界面里通过ctrl+回车选择mac的引导磁盘  
设置mac为默认引导磁盘，关闭config里的showpicker  
引导windows的话在windows下用easyuefi在原生的uefi bootloader中创建一个windows boot manager的入口，这个操作在上面贴出来的视频教程里有  
然后开机后按f12选windows即可  
我在[这个issue](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/87)里写明了为什么  
oc的图形化os选择页面无用的理由也同上  
因为你不用oc去引导windows并且直接省略选择页面，所以图形化的oc界面也就没用  



2. 一定要先改三码再用，具体的教程自己百度  

3. icloud中的查找我的mac不要打开  

4. 安全与隐私中的文件保险箱不要打开  

5. 再任何系统，任何OS下都要杜绝热启动，意思是重启的话一律先选关机再用开机键开机  
无论是单个系统下的重启需求或者是想要重启切换系统，都不要选重启选项，一律先选关机再用开机键开机  
不然有可能会导致蓝牙，触控板，Wi-Fi失灵问题。  

6. 如果你出现睡眠无法唤醒or唤醒黑屏问题，参考：[#108issue](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/108)  


</details>  

<details>  
<summary>开启安装所有来源的应用（为了运行一些必要的脚本以及一些“你懂得”软件）</summary>   
·······················································  
  
在【终端】中输入以下内容回车并输密码（密码不明文显示）  

```
sudo spctl --master-disable
```

</details>  

<details>  
<summary>安装ComboJack实现耳机耳麦切换，改进电流声。（修复耳机接口）</summary>   
  
参考： 

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)



在这里下载由Heporis制作的ComboJack.

https://github.com/randomprofilename/ComboJack


终端运行下面路径的脚本
```bash
ComboJack_Installer/install.sh
```
  
</details>

  
  
<details>  
<summary>开启HIDPI</summary>  
  
⚠️注意：  
根据你的系统版本去下载（获得）开启hidpi的脚本哈   

BigSur：[点击下载](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/Bigsur/%EF%BC%88BigSur%E6%96%B9%E6%A1%882%EF%BC%89hidpi.zip)  
Catalina：https://github.com/xzhih/one-key-hidpi  
对于Catalina用户：你需要对EFI/OC/config.plist进行更改，具体是使用propertree打开后找到：NVRAM/add/7C436110..../csr-active-config的值改为E7030000，然后reset nvram后才可以进行接下去的步骤  


我说下我的选择：  
第一步选择 开启HiDPi（注入EDID）  
第二步选择 保持原样  
第三步选择 手动输入分辨率  
分辨率输入的是 1600x1066 1343x895 2160x1440  
（这三个不是让你选，是都要输进去，两两之间要有空格） 

- 最后说一句，开启了hidpi之后，在设置→显示器里不要让分辨率超过1343x895，最大只能到这个，因为超过这个会引发一些唤醒后屏幕显示的问题（比如唤醒后屏幕只显示到四分之三），而且不要觉得这个分辨率小，因为这个是hipdi分辨率，跟你理解的分辨率不一样，1343×895实际上等于你理解的一般分辨率的2686×1790，是超过2k的，如下图所示  

*注意⚠️你的1343x895这个分辨率的设置位置不一定是在【更大空间】  

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/HIDPI.png?raw=true)  

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
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/RU.jpg?raw=true)  
4. 一看，确实是0x01，那么回车，输入0 就可以看到它变成了0  
5. 使用'crtl' + 'w' 来保存 保存的时候屏幕上会直接显示update written 的，这说明已经写入了  
6. 使用'alt' + 'q' 来退出，然后即可回到引导进入系统了，CFG已经解锁  

修改完成后可以再用那个u盘引导启动一次，查看是否修改成功  
然后我建议使用[propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip)修改EFI分区中的EFI/OC/config.plist的kernel/add/quirks为下图所示  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/cfgunlosk.png?raw=true)  


</details> 


<details>  
<summary>修改dvmt至64mb</summary>  
    
  ⚠️关于修改dvmt后能做到什么？  
  可以hdmi/dp输出4k60p的信号了  
  
  
  ⚠️以下教程的dvmt偏移地址提取自matebook13/14 2019/2018款  
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
2. 用pageup/pagedown/上下方向键找到 SaSetup  
3. 进入SaSetup后，然后用crtl加pagedown翻到下一页找到左侧横坐标0100，如下图所示，注意左侧横坐标第一项就是0100  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/%E6%9D%82%E9%A1%B9/dvmt64.bmp)  
4. 横坐标0100纵坐标07改成02，横坐标0100纵坐标08改成03（就是我圈出来的位置修改的跟上图一样就行了）  
5. Crtl加w保存就行了  


修改完成后可以再用那个u盘引导启动一次，查看是否修改成功  
最后记得用propertree去修改一下config，移除里面缓冲帧的“framebuffer-fbmem”，“framebuffer-stolenmem”，“framebuffer-unifiedmem”这三个条目。  


  
  
[本教程灵感来源@laozhiang](https://github.com/laozhiang)  
  


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


<details>  
<summary>关于我认为的一些可以给你更好体验的软件</summary>  
  
  
  
1. Mos：保证鼠标的顺畅滑动，以及滚轮方向的调整 官网：[https://mos.caldis.me/](https://mos.caldis.me/)  
2. Rectangle:还给你windows的拖动分屏逻辑 官网：[https://rectangleapp.com/](https://rectangleapp.com/)  
3. Stats：状态栏监控插件 主页：[https://github.com/exelban/stats](https://github.com/exelban/stats)  
4. Keka：强大好用的压缩软件 官网：[https://www.keka.io/en/](https://www.keka.io/en/)  
5. IINA：万能播放器 官网：[https://iina.io/](https://iina.io/)  
6. Motrix：万能下载器 官网：[https://motrix.app/](https://motrix.app/)  
7. Hackintool：黑苹果的瑞士军刀 主页：[https://github.com/headkaze/Hackintool](https://github.com/headkaze/Hackintool)  
8. Propertree：我最推荐的config编辑软件 主页：[https://github.com/corpnewt/ProperTree](https://github.com/corpnewt/ProperTree)  
9. Wormhole：mac上的huawei share,治好了我的颈椎病，上班狗的福音 官网：[https://er.run/](https://er.run/)  
10. 超级右键：恢复windows的右键新建txt，新建word/excel等操作 官网:[https://www.better365.cn/](https://www.better365.cn/)  


</details>  

## 如果想打赏小的，请选择一个你喜欢的方式打赏五块钱，谢谢！
  
  ⭐️打赏附言请留下自己的github的ID，用于公示感谢  
  

  
[看不到图片请点击](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5vhyua0NyktT47EDwPAfhtuBceWLK5.5V40I*6lQE5rORR7qbWTf9Eovur4ifsHKECewZxvEqi.ZfhaQ4ObpAl8!/b&bo=DQWcAw0FnAMBCS4!&rf=viewer_4)  



![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/payment.jpeg?raw=true)  



  
[看不到图片请点击](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5vhyua0NyktT47EDwPAfhtuBceWLK5.5V40I*6lQE5rORR7qbWTf9Eovur4ifsHKECewZxvEqi.ZfhaQ4ObpAl8!/b&bo=DQWcAw0FnAMBCS4!&rf=viewer_4)  

    
    
 

## 感谢：

- [@intel](https://www.intel.com/content/www/us/en/homepage.html) 感谢10年一管牙膏（AMD,YES!）

- [@apple](https://www.apple.com/) 感谢创造出macos

- [@zxystd](https://github.com/OpenIntelWireless/itlwm) 感谢创造出wifi以及蓝牙的驱动

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) 教会了我很多东西

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh) 我做黑苹果的入门引路人 感谢他在matebook13的clover版efi上的杰出贡献

- [@Zero-zer0](https://github.com/Zero-zer0) 参考了他的热键修复方法 十分感谢

