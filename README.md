# dingdong-opkg

叮咚监听 OpenWrt 软件包下载页。

## 第一次安装，或更新列表提示公钥错误

1. 在电脑或手机浏览器下载[完整安装包](https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main/dingdong-listener_2.2.2-103_all.ipk)，保存为 `.ipk` 文件。
2. 打开路由器管理页面，进入「系统 → 软件包 → 上传软件包」，选中刚下载的文件并点击安装。若已有旧版，按页面提示确认覆盖升级。
3. 安装完成后刷新管理页面，打开「服务 → 叮咚监听」。安装包会自动配置软件源和签名公钥，无需手动导入。

之后可在「系统 → 软件包」点击「更新列表」，再升级 `dingdong-listener`。

适用使用 opkg 的 ARM64 路由器；OpenWrt 25.12 及以后若使用 apk 包管理器，则不能安装此 IPK。
