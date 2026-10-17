# dingdong-opkg

叮咚监听 OpenWrt 软件包下载页。

## 第一次安装，或更新列表提示公钥错误

1. 在电脑或手机浏览器下载[首次安装/签名恢复包](https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main/bootstrap/dingdong-listener_2.2.4-27_all.ipk)，保存为 `.ipk` 文件。
2. 打开路由器管理页面，进入「系统 → 软件包 → 上传软件包」，选中刚下载的文件并点击安装。若已有旧版，按页面提示确认覆盖升级。
3. 安装完成后刷新管理页面，打开「服务 → 叮咚监听」。安装包会自动配置软件源和签名公钥，无需手动导入。

首次安装后，在「系统 → 软件包」点击「更新列表」，再升级 `dingdong-listener`。这一步会自动安装一次运行时依赖；以后的应用更新只下载小包。

2026-10-18 更换了软件源签名密钥。已安装 `dingdong-runtime` 的用户，只需下载并在 LuCI 上传约 1.1 MB 的[应用包](https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main/dingdong-listener_2.2.4-27_all.ipk)，安装新公钥后再更新列表，无需重新下载运行时。首次安装或缺少运行时的设备使用上面的完整恢复包。原始 [2.2.4-7 安装包](https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main/bootstrap/dingdong-listener_2.2.4-7_all.ipk) 留存归档。

适用使用 opkg 的 ARM64 路由器；OpenWrt 25.12 及以后若使用 apk 包管理器，则不能安装此 IPK。
