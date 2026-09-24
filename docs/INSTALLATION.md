# CloseAI 安装指南

正式渠道为 [GitHub Releases](https://github.com/unfalltable/closeai/releases) 与 [CloseAI 官方下载页](https://closeai.shop)。下载后请核对同一 Release 中的 SHA-256 文件。

## Windows

1. 下载 `CloseAI-*-Windows-x64.exe` 和对应 `.sha256` 文件。
2. 使用 `Get-FileHash .\CloseAI-*-Windows-x64.exe -Algorithm SHA256` 核对哈希。
3. 双击安装并选择安装目录。
4. 当前 Beta 尚未接入 Windows 代码签名。SmartScreen 提示时，请先确认下载来源和哈希，再选择“更多信息”继续。
5. 打开 CloseAI，登录并使用一次性配对码连接工作电脑。

## Linux

AppImage：

```bash
chmod +x CloseAI-*-Linux-x86_64.AppImage
./CloseAI-*-Linux-x86_64.AppImage
```

Debian 或 Ubuntu：

```bash
sudo apt install ./CloseAI-*-Linux-amd64.deb
```

使用 `sha256sum <文件名>` 核对下载文件。

## Android

当前 APK 使用测试签名，适合侧载验证，尚不是 Google Play 正式包。

1. 下载 `CloseAI-*-Android-debug.apk` 和对应 `.sha256` 文件。
2. 核对哈希后，仅对当前文件管理器临时允许“安装未知应用”。
3. 完成安装后关闭该临时权限。

Android 客户端用于控制任务，不能代替工作电脑执行本地开发命令。

## 浏览器与 PWA

打开 [https://closeai.shop](https://closeai.shop) 登录即可使用。可以通过浏览器菜单将 CloseAI 添加到手机主屏幕。需要操作本地项目时，工作电脑必须开机并运行 CloseAI 客户端。

## macOS 与 iOS

当前公开 Release 尚未提供经过 Developer ID、Apple 公证或 App Store 签名的安装包。正式包会在 Apple 开发者账号和发布资质配置完成后提供。
