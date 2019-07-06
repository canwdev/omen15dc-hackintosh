# 暗影精灵4 i5-8300H + GTX1050Ti 黑苹果 EFI

[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)

[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

OMEN 15dc Hackintosh Clover EFI

暗影精灵4 i5-8300H + GTX1050Ti 黑苹果 EFI

## 说明

本人黑苹果小白，这是我从网上收集各种资源整合并修复的 EFI 配置，适用用于`暗影精灵4 i5-8300H` + `GTX1050Ti`

使用的系统镜像是 [macOS Mojave 10.14.4(18E226) Installer with Clover 4903](https://blog.daliansky.net/macOS-Mojave-10.14.4-18E226-official-version-with-Clover-4903-original-image.html#more)

安装过程可参考 [macOS安装教程兼小米Pro安装过程记录](https://blog.daliansky.net/MacOS-installation-tutorial-XiaoMi-Pro-installation-process-records.html)

建议安装时直接使用【黑果小兵】大神的镜像，安装完成后再替换此 EFI



### 可用功能：

- UHD630 集成显卡驱动
- 可调节亮度、内置键盘、触摸板
- 音频、录音，可接耳机
- 有线上网、USB接口功能
- 电池
- 温度传感器
- 睡眠
- 开机不再黑屏
- 亮度保存正常（教程在下面）

### 无效功能：

- 无线网卡（只能换网卡）
- HDMI、DP输出（无法解决，因为走的是独显）
- 键盘灯无法在系统内配置,FN+F4为睡眠(可以在刚开机时配置)

## 截图

![初次安装完成效果](https://ws3.sinaimg.cn/large/005BYqpgly1g1s3fbr5igj31hc0u0u0x.jpg)

![完成效果](https://ws3.sinaimg.cn/large/005BYqpgly1g1s3japa5zj31hc0u0u0x.jpg)

![完成效果](https://spxg.me/wp-content/uploads/2019/06/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7-2019-06-21-%E4%B8%8B%E5%8D%881.35.43.png)
![电池与传感器](https://spxg.me/wp-content/uploads/2019/06/QQ20190621-134227.png)

下面配置已经写入`config.plist`，仅供参考

![显卡配置](https://ws3.sinaimg.cn/large/005BYqpgly1g1s3mcfnxsj30j80kidk7.jpg)

![显示器配置](https://ws3.sinaimg.cn/large/005BYqpgly1g1s3n6ca0aj30j80ki0wo.jpg)

![声音配置](https://ws3.sinaimg.cn/large/005BYqpgly1g1s44mcri7j30j80kijv9.jpg)

## 显示器补丁（可选）

显示器配置可在系统安装后自行添加，增加了之后即可支持缩放和夜览等功能，[说明文档](./DisplayPatch/README.md)

## 常用命令

```sh
# 显示磁盘列表
diskutil list
# 挂载分区
sudo diskutil mount disk3s1
```
## 修复亮度保存
因为不能利用原生nvram来储存亮度，所以利用RC scripts来保存，安装Clover时选择RC scripts即可
![亮度保存](https://spxg.me/wp-content/uploads/2019/07/QQ20190706-141105.png)

## 参考教程

- [【黑果小兵】macOS Mojave 10.14.4 18E226 正式版 with Clover 4903原版镜像](https://blog.daliansky.net/macOS-Mojave-10.14.4-18E226-official-version-with-Clover-4903-original-image.html)
- [macOS安装教程兼小米Pro安装过程记录](https://blog.daliansky.net/MacOS-installation-tutorial-XiaoMi-Pro-installation-process-records.html)
- [Hackintool(原Intel FB-Patcher)使用教程及插入姿势](https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html)
- [【黑果小兵】CoffeeLake UHD 630黑屏、直接亮屏及亮度调整的正确插入姿势](https://blog.daliansky.net/CoffeeLake-UHD-630-black-screen-direct-bright-screen-and-correct-adjustment-of-brightness-adjustment.html)
- [教程：利用Hackintool打开第8代核显HDMI/DVI输出的正确姿势](https://blog.daliansky.net/Tutorial-Using-Hackintool-to-open-the-correct-pose-of-the-8th-generation-core-display-HDMI-or-DVI-output.html)
