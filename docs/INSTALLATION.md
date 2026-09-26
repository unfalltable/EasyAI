# CloseAI 安装指南

正式渠道为 [GitHub Releases](https://github.com/unfalltable/closeai/releases)；[closeai.shop](https://closeai.shop) 只提供跳转下载。下载后请核对同一 Release 中的 SHA-256 文件。

## Windows

1. 下载 `CloseAI-*-Windows-x64.exe` 和对应 `.sha256` 文件。
2. 使用 `Get-FileHash .\CloseAI-*-Windows-x64.exe -Algorithm SHA256` 核对哈希。
3. 双击安装并选择安装目录。
4. 当前 Beta 尚未接入 Windows 代码签名。SmartScreen 提示时，请先确认下载来源和哈希，再选择“更多信息”继续。

## macOS

当前 Beta 提供 Apple 芯片和 Intel 两种未签名 `.app.zip` 测试包，尚未完成 Developer ID 签名、公证和 Mac 实机验证。

1. 下载与机器架构对应的 `.app.zip`，核对同名 `.sha256`。
2. 解压并把 `CloseAI.app` 拖入 Applications。
3. 核对来源后，在终端执行 `xattr -cr /Applications/CloseAI.app`，然后右键选择“打开”。

正式 DMG 仍需要 macOS 构建机和 Apple 开发者资质。

## Linux

便携包：

```bash
tar -xzf CloseAI-*-Linux-x86_64.tar.gz
cd CloseAI-*
chmod +x CloseAI
./CloseAI
```

Debian 或 Ubuntu：

```bash
sudo apt install ./CloseAI-*-Linux-amd64.deb
```

使用 `sha256sum <文件名>` 和 `SHA256SUMS-closeai-linux.txt` 核对文件。

## Android

当前 APK 使用测试签名，适合侧载验证，尚不是 Google Play 正式包。

1. 下载 `CloseAI-*-Android-debug.apk` 和对应 `.sha256` 文件。
2. 核对哈希后，仅对当前文件管理器临时允许“安装未知应用”。
3. 完成安装后关闭该临时权限。

Android 客户端用于控制任务，不能代替工作电脑执行本地开发命令。

## iPhone / iPad 与 PWA

普通真机 IPA 和 TestFlight 需要 Apple Developer 证书、Provisioning Profile 和 Xcode 签名环境。当前请使用 Safari 打开 [closeai.shop](https://closeai.shop)，通过“添加到主屏幕”安装为 PWA。需要操作本地项目时，工作电脑或自己的服务器必须在线运行 CloseAI 连接器。