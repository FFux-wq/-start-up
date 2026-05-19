# 多平台整蛊下载引导页

一个基于「自动下载原神」梗的朋友间整蛊工具。通过微信发送链接给朋友，页面自动检测设备——桌面端触发 .exe 下载，手机端触发 APK 下载，1.5 秒后均跳转原神官网。

## 使用方法

1. 通过微信将链接发给朋友
2. 对方点击链接后，页面会根据设备自动跳转

> 部署链接：`https://ffux-wq.github.io/YS_Start_up/`

## 用户流程

| 环境 | 行为 |
| :--- | :--- |
| 微信内置浏览器 | 显示引导页，提示用户点击右上角 ··· 选择「在浏览器中打开」 |
| 系统浏览器（Android） | APK 下载直链 → 1.5s 后跳转原神官网 |
| 系统浏览器（iOS） | APK 下载直链 → 1.5s 后跳转原神官网 |
| 桌面浏览器 | .exe 下载直链 → 1.5s 后跳转原神官网 |

## 部署

- **平台**：GitHub Pages
- **仓库**：[FFux-wq/YS_Start_up](https://github.com/FFux-wq/YS_Start_up)
- **链接**：[ffux-wq.github.io/YS_Start_up](https://ffux-wq.github.io/YS_Start_up/)

更新部署：推送至 `YS_Start_up` 分支，GitHub Pages 自动构建。

## 技术说明

- 单文件 HTML，零外部依赖
- UserAgent 检测设备类型、操作系统和微信环境
- CSS 动画引导箭头，纯 CSS 实现
- Android：APK 下载直链 → 1.5s 后跳转原神官网
- iOS：APK 下载直链 → 1.5s 后跳转原神官网
- 桌面端：.exe 下载直链 → 1.5s 后跳转原神官网
- iPad 检测：通过 `maxTouchPoints` 识别 iPadOS 13+ 设备

## 注意事项

- 页面标题和文案刻意中性化（「链接跳转」），跳转前不暴露原神关键词
- 整蛊仅限朋友间玩笑，请勿用于恶意用途
- 微信可能对非白名单域名标记「已停止访问」，建议同时部署备用链接
