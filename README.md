# meego-launcher

一个仿 MeeGo / 诺基亚 N9 桌面视觉与交互风格的 Android 第三方桌面。

## 应用特点

> **后台主页、应用抽屉页、小部件页左右滑动循环显示**

### 卡片式后台主页
- 最近任务以卡片形式平铺，下拉进入菜单，长按卡片进入清理模式，单击叉号结束对应应用的后台进程，下拉可一键清理后台。
![主页](https://github.com/kouxiaofang/meego-launcher/blob/91ee6184716ad63e2596ec3b54a31760a2b2843a/%E4%B8%BB%E9%A1%B5.jpg?raw=true)

### 应用抽屉页
- 支持4/5列布局切换、隐藏/显示文字、文件夹显示在最前/最后、隐藏/显示通知角标，下拉进入菜单操作。
![应用抽屉页](https://github.com/kouxiaofang/meego-launcher/blob/91ee6184716ad63e2596ec3b54a31760a2b2843a/%E5%BA%94%E7%94%A8%E6%8A%BD%E5%B1%89.jpg?raw=true)

### 小部件页
- 因hyperos不暴漏时钟和天气内置小部件，所以自己给时钟、天气各做了2个小部件。支持关闭小部件页，看个人操作习惯。
![小部件页](https://github.com/kouxiaofang/meego-launcher/blob/91ee6184716ad63e2596ec3b54a31760a2b2843a/%E5%B0%8F%E9%83%A8%E4%BB%B6.jpg?raw=true)

### 其他
- 双击桌面空白处锁屏（需要 Shizuku 或 Root）。
- 备份 / 恢复：可以将应用抽屉布局与小部件布局导出到 `Download/MeegoBackup`，换机或重装后可一键恢复。
- 全部 UI 为毛玻璃风格，代码绘制，无图片资源依赖。


## 运行依赖

> **后台任务显示与管理依赖root权限或最新版本的 Shizuku，并保持 Shizuku 服务处于运行状态。**

- 桌面本身可以启动并展示，但以下核心能力依赖 Shizuku（或 Root）授权：
  - 卡片页结束其他应用的后台进程；
  - 双击锁屏；
  - 读取应用使用记录（也可单独授予"查看使用情况"权限）。
- Shizuku 版本过旧或不处于运行状态时，相关功能会降级或不可用，并在页面上给出提示。
- 无 Root、无 Shizuku、也无"使用情况访问"权限时，卡片页可能显示为空并附带权限提示卡。


## 兼容性声明

本项目**仅在 HyperOS 4 的小米真机上做过测试**，未在其他品牌、其他系统版本或其他机型上验证。

由于大量依赖系统私有的窗口 inset 行为、`AppWidgetHost` 实现细节与 Shizuku 授权流程，**不保证在其他品牌或其他系统的手机上能正常运行**（可能出现布局偏移、小部件无法添加、进程结束后台失败、闪退等问题）。

在非 HyperOS 4 设备上使用前请自行评估，出现问题时欢迎反馈，但不承诺修复。


## 声明

- 本项目为个人学习与非商业用途的仿制实现，视觉风格致敬 MeeGo / 诺基亚 N9。
- MeeGo、Nokia 及相关商标、界面设计的权利归其各自权利人所有，本项目与其无任何隶属或授权关系。
- 项目中的图标、名称等素材如有侵权，请通过项目 Issue 或仓库主页联系作者，作者会在收到通知后立即删除相关内容。


## 致谢

- [Shizuku](https://github.com/RikkaApps/Shizuku)（RikkaApps）—— 免 Root 的特权调用方案。
- [Open-Meteo](https://open-meteo.com/) 与 [ip-api](https://ip-api.com/) —— 免费天气与地理数据。


## 打赏
- 如喜欢此应用并支持作者继续开发完善，可以微信打赏，钞能力将有效提升作者的开发效率。
![打赏二维码](https://github.com/kouxiaofang/meego-launcher/blob/09d942cd11d8ce29e3d064a3ee6bab4fa01dde3d/wechatpay.png?raw=true)
