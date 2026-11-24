# 第三方许可证与参考资料

本项目以 MIT 许可证发布（见根目录 `LICENSE`）。以下列出运行/构建依赖及研究参考项目。

## 1. 运行时依赖（被打包进 `main.js`）

| 组件 | 版本 | 许可证 | 用途 |
|---|---|---|---|
| Lit | 3.3.2 | BSD-3-Clause | Web Components / 响应式模板 |
| @sun-panel/micro-app | 1.0.19 | MIT | Sun-Panel 官方微应用 SDK（基类、i18n、网络/定时器/数据节点 API 类型） |

`lit` 的 BSD-3-Clause 文本随 npm 包分发；`@sun-panel/micro-app` 的 MIT 文本随包分发。
本项目的 `main.js` 打包了两者；再分发时请保留其版权与许可证声明。

## 2. 构建/测试依赖（不进入安装包）

| 组件 | 版本 | 许可证 |
|---|---|---|
| Vite | 6.3.6 | MIT |
| TypeScript | 5.9.3 | Apache-2.0 |
| Vitest | 3.2.4 | MIT |
| jsdom | 26.1.0 | MIT |
| adm-zip | 0.5.16 | MIT |
| @types/node | 22.15.3 | MIT |
| @types/adm-zip | 0.5.5 | MIT |

## 3. 研究与设计参考（未复制代码）

以下项目用于理解 UniFi API 字段、WAN 速率计算、版本兼容与异常恢复。**本项目没有复制其源代码**；
仅参考公开接口/字段/设计思路。许可证为各仓库当前 `LICENSE`（查询时间 2026-11-24）：

| 项目 | 许可证 | 参考点 |
|---|---|---|
| [unpoller/unpoller](https://github.com/unpoller/unpoller) | MIT | UniFi 传统 API 字段、设备/客户端统计、站点结构 |
| [Kane610/aiounifi](https://github.com/Kane610/aiounifi) | MIT | 设备/客户端/WAN 字段与版本差异处理 |
| [holdestmade/Unifi-WAN](https://github.com/holdestmade/Unifi-WAN) | MIT | 轻量 WAN 查询、速率展示思路 |
| [LayerTM/unifi-ucg-fiber-ha](https://github.com/LayerTM/unifi-ucg-fiber-ha) | MIT | UCG Fiber 字段/能力参考 |
| [home-assistant/core · unifi](https://github.com/home-assistant/core/tree/dev/homeassistant/components/unifi) | Apache-2.0 | 设备/客户端模型与兼容策略 |
| [Art-of-WiFi/UniFi-API-browser](https://github.com/Art-of-WiFi/UniFi-API-browser) | MIT | 只读 API 端点/字段参考 |
| [Art-of-WiFi/UniFi-API-client](https://github.com/Art-of-WiFi/UniFi-API-client) | MIT | 传统 API 认证与端点参考 |
| [Sun-Panel](https://github.com/hslr-s/sun-panel) | MIT | 微应用规范/宿主行为参考 |
| [Sun-Panel 官方文档](https://doc.sun-panel.top/zh_cn/micro_app_dev/index.html) | 文档 | 微应用开发规范 |
| [UniFi 官方 API 文档](https://developer.ui.com/) | Ubiquiti 条款 | Integration API/字段 |

## 4. 图标与图片

- 应用图标 `public/icon.svg` / `public/icon.png`：本项目原创绘制。
- 界面图标：项目内原创的单色内联 SVG 路径，未从 Simple Icons/cib 等库复制。
- 截图：本项目在真实环境拍摄；桌面截图含本机/网络信息，仅保存在本地 `evidence/`。

## 5. 商标

UniFi、UCG Fiber、U7、USW 等是 Ubiquiti Inc. 的商标；Sun-Panel 是其作者的商标。
本项目为第三方独立监控工具，与 Ubiquiti/Sun-Panel 官方无隶属关系。
