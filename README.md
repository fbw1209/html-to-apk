## HTML 打包 APK 工具

一个图形化工具，帮助您将 HTML 文件、ZIP 包或网址快速打包为 Android APK。  
支持自定义应用名称、包名、图标、权限，并使用 `apksigner` 对 APK 进行签名。

![License](https://img.shields.io/badge/license-MIT-green) ![Python](https://img.shields.io/badge/python-3.7%2B-blue) ![Platform](https://img.shields.io/badge/platform-Windows-blue)

---

## ✨ 功能特性

- 🧩 **多种输入源** – 支持单个 HTML 文件、ZIP 压缩包或网页网址
- 🏷️ **自定义应用信息** – 修改包名、应用名称、版本号、版本代码
- 🖼️ **更换图标** – 支持 PNG / JPG / ICO 格式图标
- 🔐 **签名证书** – 必须使用自己的 `.keystore` / `.jks` 证书进行签名（apksigner）
- 🔧 **权限管理** – 可视化编辑权限列表（完全替换原 APK 权限）
- 🎨 **个性化界面** – 内置主题切换 + 自定义背景/文字颜色
- ⚡ **自动优化** – 集成 `zipalign` 对齐优化（可选）
- 🗂️ **路径友好** – 自动处理 Windows 路径，但**禁止路径包含空格**

---

## 🛠️ 依赖文件


- **Java** 环境（JDK 8 或更高版本）
- **Python 3.7+** 
- 签名证书`.keystore`

---

## 🚀 使用方法

1. 运行 `html-to-apk.py`
2. 填写应用参数（版本号、应用名称、包名等）
3. 选择输入源（本地 HTML/ZIP 或网址）
4. 选择输出 APK 路径
5. 点击 **权限设置** 调整所需权限
6. 填写证书信息（密钥库、密码、别名等）
7. 点击 **打包为 APK** 等待完成

> **注意**：所有文件路径（输入源、图标、输出 APK、证书）**不能包含空格**，否则会导致打包失败。

---

## 📝 证书要求

- 密钥库文件`.keystore` 
- 密钥库密码
- 密钥别名
- 密钥密码（通常与密钥库密码相同）

如无现有证书，可点击界面中的 **生成证书** 按钮跳转至在线生成页面。

---

## ⚙️ 支持的权限列表

程序内置了常用的 Android 权限，您也可以手动输入自定义权限名称（完整格式，如 `android.permission.CAMERA`）。  
勾选或取消勾选后，最终 APK 的 `AndroidManifest.xml` 中将**只包含您选中的权限**。

---

## ⚠️ 注意事项

- 打包过程会在系统临时目录创建 `html_to_apk_temp` 文件夹，退出后自动清理。
- 签名后的 APK 会覆盖临时文件，最终输出到您指定的路径。
- 若缺少 `zipalign.exe`，将自动跳过对齐优化，不影响正常打包。

---


## 👨‍💻 作者

**fbw111209**  
反馈邮箱：fbw111209@qq.com  

---

## 📄 开源协议

本项目基于 MIT 协议开源，详情见 [LICENSE](LICENSE) 文件。
