# matebook-13/14-2019-OpenCore-EFI 黑苹果 hackintosh 
  
如果你不会安装，需要安装服务，联系微信ske1996
可提供收费安装服务，并且保修1个月  

如果可用请在issues中提交你的机器信息（年份，cpu，matebook13还是14）  
用于构建更好的efi

[English](readme-eng.md) | [中文](readme-cn.md)    


## 更新日志  
20200712:  
已知本efi可同时用于matebook 13/14 2019  
于2020版本测试情况如下：  
除了wifi不能驱动一切同2019版本，原因可能是2020版本采用了第二代9560

20200710:  
添加了配置好的clover的efi文件用于安装，虽然也可以用这个clover文件复制到esr分区用于引导   
但是强烈建议使用oc的efi引导你的hackintosh  

20200709:  
1.更改了三码  
2.添加了保险文件（WRCOVERY.BIN）  
用法：放入esr分区，与EFI文件夹并列即可

下一个版本可能更新bigsur的EFI

## 正常可用的部件：
  
  
1.蓝牙（无需热启动）From IntelBluetoothFirmware @zxystd

2.wifi （需要用propertree注入你自己的ssid跟password）可以做到无违和感使用 From itlwm @zxystd

3.睡眠正常

4.hdmi正常（可音频输出）

5.触摸板正常

6.解锁cfg lock后可完美原生电源管理

7.已注入缓冲帧 核显正常

8.cpu变频正常（补充：此efi内涵cpufriend，设置为：1800mhz，最高性能）

9. usb已定制（通过ssdt定制）

10.键盘快捷键正常

  
  
## 无法正常工作的部件：  


1.摄像头（这个看命，有的人能用）

2.耳机接口（只是需要使用修复进程，这个进程无法集成进efi）

3.mx250独显（这个是废话）

  
## 个人使用版本信息等   
oc版本0.5.8

自用macos版本：10.15.5. 

matebook2019 i7-8565u mx250 sn720

## 安装方法：  


先于此blog下载：10.15.5 19F101 双EFI分区版

这个文章很长，使劲往下翻，或使用网页搜索功能

下载链接
：https://blog.daliansky.net/macOS-Catalina-10.15.5-19F96-Release-version-with-Clover-5118-original-image-Double-EFI-Version-UEFI-and-MBR.html
  
    
      
## 安装视频教程：

https://www.bilibili.com/video/BV1jJ41127YT/?spm_id_from=333.788.videocard.0
  
如果你不会安装，需要安装服务，联系微信ske1996
可提供收费安装服务，并且保修1个月  
## 安装注意点：  


1.安装使用的镜像推荐使用我给的链接下载的那个，不要用他给的，以内有点旧了

2. 视频的【03:57】他说把配置好的clover文件解压到这个文件夹下时，将我的库中的【安装用clover的EFI】放进去  

3.视频的【14:37】开始他开始吧u盘的clover efi复制进ESR（EFI）分区，这一步复制我的oc的efi进去。注意：这一步的efi跟第二步不一样，这一步用oc的

4. 视频的【16:44】开始是使用easyuefi创建efi引导，这一步前面都跟他视频一样，他怎么点你就怎么点，只不过，选择引导文件为：EFI/BOOT/BOOTx64.efi
  
  

## 安装ComboJack实现耳机耳麦切换，改进电流声。

在这里下载由Heporis制作的ComboJack.

https://github.com/hackintosh-stuff/ComboJack


终端运行下面路径的脚本

ComboJack_Installer/install.sh
  
  


## 开启HIDPI：

https://github.com/xzhih/one-key-hidpi
 

我说下我的选择：  
第一步选择 开启HiDPi  
第二步选择 保持原样  
第三步选择 手动输入分辨率  
分辨率输入的是 1600x1066 1343x895 2160x1440  
  
  
## 解锁CFG：

https://zhuanlan.zhihu.com/p/121655468

先去华为官网升级bios至1.27

然后找偏移地址就不用做了，我告诉你，就是0x3E



  
如果你不会安装，需要安装服务，联系微信ske1996，可提供收费安装服务，并且保修1个月
      
      
## 最近在努力解决摄像头问题，要是想打赏小的，请选择一个你喜欢的方式，谢谢！


微信收款码链接：

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E5%BE%AE%E4%BF%A1.jpg?raw=true). 
  
  

支付宝收款码链接：

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%94%AF%E4%BB%98%E5%AE%9D.jpg?raw=true)

  
  
    
    
  
  
如果可用请在issues中提交你的机器信息（年份，cpu，matebook13还是14）  
用于构建更好的efi

## 感谢：

@intel 感谢10年一管牙膏

@apple 感谢创造出macos

@zxystd 感谢创造出wifi以及蓝牙的驱动

@MoZyo 教会了我很多东西

@Edoardo001 我做黑苹果的入门引路人 感谢他在matebook13的clover版efi上的杰出贡献

@Zero-zer0 参考了他的热键修复方法 十分感谢

