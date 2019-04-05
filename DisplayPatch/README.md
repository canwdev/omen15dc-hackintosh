# 显示器补丁使用方式（转载）

原文链接：https://blog.daliansky.net/Intel-FB-Patcher-tutorial-and-insertion-pose.html

安装
安装EDID补丁有两种方法：1. 显示覆盖 2. 扩展库(L/E) 请二选一


1. 显示覆盖 (Display Overrides):
```
• 将 DisplayVendorID-x 文件夹复制到 /System/Library/Displays/Contents/Resources/Overrides (或者 /System/Library/Displays/Overrides El Capitan 及以前版本)

• 将 Icons.plist 复制到 /System/Library/Displays/Contents/Resources/Overrides (或者 /System/Library/Displays/Overrides El Capitan 及以前版本)
```
2. 扩展库 (Library Extensions):
```
• 将 DisplayEDID-x-x.kext 复制到 /Library/Extensions 或者 EFI/Clover/kexts/Other (取决于您的配置，建议使用 Clover 的方法)
```

## 系统完整性保护 (SIP)

您需要禁用SIP (sudo spctl --master-disable) 才能将文件复制到方法1所述位置。