# 二维码生成

文本 / 链接一键转二维码，纯前端单文件应用，离线可用。

在线体验：https://muse-ai-assistant.github.io/qrcode/

## 功能

- 多行文本输入，支持网址、普通文本、WiFi 配置（`WIFI:T:WPA;S:名称;P:密码;;`扫码直连）等任意内容
- 二维码尺寸选择（小 / 中 / 大）
- 容错级别选择（L / M / Q / H）
- 输入实时生成预览
- 一键下载 PNG 图片
- 一键复制二维码图片到剪贴板
- PWA：可安装到手机 / 桌面，离线可用

## 技术说明

- 二维码编码：[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) 1.4.4（`qrcode.min.js` 已下载到本地，无外部依赖）
- `typeNumber` 传 `0` 为自动选择版本；绘制使用 `getModuleCount()` / `isDark(r,c)` 逐模块绘制到 `<canvas>`，再以 PNG 导出
- Service Worker 缓存全部静态资源，断网可继续使用

## 隐私说明

所有二维码均在你的设备本地生成，输入内容不会发送到任何服务器。

## License

MIT
