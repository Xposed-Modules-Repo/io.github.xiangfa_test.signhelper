# 签名助手（SignHelper）

<p align="center">
  <a href="https://github.com/xiangfa-test/com.xiang.signhelper/releases"><img src="https://img.shields.io/github/v/release/xiangfa-test/com.xiang.signhelper?label=release&color=0aa1dd" alt="Release"></a>
  <a href="https://github.com/xiangfa-test/com.xiang.signhelper/releases"><img src="https://img.shields.io/github/downloads/xiangfa-test/com.xiang.signhelper/total?label=downloads&color=2ea44f" alt="Downloads"></a>
  <a href="https://github.com/xiangfa-test/com.xiang.signhelper/stargazers"><img src="https://img.shields.io/github/stars/xiangfa-test/com.xiang.signhelper?label=stars&color=e3b341" alt="Stars"></a>
  <img src="https://img.shields.io/badge/license-GPL--3.0--only-8957e5" alt="License">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-13%2B-3ddc84?logo=android&logoColor=white" alt="Android 13+">
  <img src="https://img.shields.io/badge/LSPosed-module-6f42c1" alt="LSPosed module">
  <a href="https://t.me/onelazyfish"><img src="https://img.shields.io/badge/Telegram-MIKU%E7%9A%84%E5%B0%8F%E7%AA%9D-26A5E4?logo=telegram&logoColor=white" alt="Telegram 发布频道：MIKU的小窝"></a>
  <a href="https://t.me/xiangfa_channel"><img src="https://img.shields.io/badge/Telegram-%E6%83%B3%E6%B3%95%E3%81%AE%E7%AA%9D-26A5E4?logo=telegram&logoColor=white" alt="Telegram 发布频道：想法の窝"></a>
</p>

让被 hook 的应用在通过 `PackageManager` 读取其他应用签名时，拿到模块里为该应用设置的伪造签名，用于绕过简单的签名校验。

- **源码地址**：https://github.com/xiangfa-test/com.xiang.signhelper
- **问题反馈**：https://github.com/xiangfa-test/com.xiang.signhelper/issues
- **原版作者**：xihan（`cn.xihan.sign`）；当前维护：xiangfa
- 基于 **libxposed API 102**；默认作用域：微信、QQ（可在 LSPosed 中勾选任意应用）

> **注意**：从 0.1.1 起安装包名为 `io.github.xiangfa_test.signhelper`，与旧的 `com.xiang.signhelper` 是两个应用；升级请先卸载旧版，再在 LSPosed 里重新启用并勾选作用域。

## 使用

1. 在 LSPosed 中启用本模块，并勾选需要被 hook 的应用
2. 打开「签名助手」→ 应用目录 → 选择已安装应用 / 选择 APK
3. 点击条目填入伪造签名（十六进制）并打开开关
4. 强制停止被 hook 的应用，再重新打开

## 说明

- 只替换 `PackageInfo.signatures`，不处理 `signingInfo` / `checkSignatures`
- 部分系统（MIUI / HyperOS 等）需要允许「获取应用列表」权限，否则列表可能不完整（应用内会提示）
- 修改配置后需要重新启动被 hook 的应用

## 发布频道

- Telegram 发布频道：https://t.me/onelazyfish（MIKU的小窝）
- Telegram 发布频道：https://t.me/xiangfa_channel（想法の窝\[SFW\]）
