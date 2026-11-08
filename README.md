# 签名助手（SignHelper）

让被 hook 的应用在通过 `PackageManager` 读取其他应用签名时，拿到模块里为该应用设置的伪造签名，用于绕过简单的签名校验。

- **源码地址**：https://github.com/xiangfa-test/com.xiang.signhelper
- **问题反馈**：https://github.com/xiangfa-test/com.xiang.signhelper/issues
- **原版作者**：xihan（`cn.xihan.sign`）；当前维护：xiangfa
- 基于 **libxposed API 102**；默认作用域：微信、QQ（可在 LSPosed 中勾选任意应用）

## 使用

1. 在 LSPosed 中启用本模块，并勾选需要被 hook 的应用
2. 打开「签名助手」→ 应用目录 → 选择已安装应用 / 选择 APK
3. 点击条目填入伪造签名（十六进制）并打开开关
4. 强制停止被 hook 的应用，再重新打开

## 说明

- 只替换 `PackageInfo.signatures`，不处理 `signingInfo` / `checkSignatures`
- 部分系统（MIUI / HyperOS 等）需要允许「获取应用列表」权限，否则列表可能不完整（应用内会提示）
- 修改配置后需要重新启动被 hook 的应用