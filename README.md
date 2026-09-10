# 我们的婚礼故事

面向新人的婚礼视频故事采集主页。保留五幕采集结构，支持电脑和手机、中文与英文、本地草稿、填写进度、完整复制和复制失败后的手动备选。

## 本站地址

- 采集主页：https://hertz001cg.github.io/our-wedding-story/
- 源码仓库：https://github.com/Hertz001Cg/our-wedding-story
- 发布配置：`main` 分支的 `/docs` 目录。

发送采集链接给新人即可，不需要让新人安装 Codex 或登录 GitHub。

## 本地预览

在仓库目录执行 `python -X utf8 -m http.server 8734 --bind 127.0.0.1 --directory docs`，打开 http://127.0.0.1:8734/ 。也可以直接打开 `docs/index.html`；HTTP 预览更适合检查浏览器草稿与复制功能。

## GitHub Pages

1. 用 GitHub Desktop 添加本地仓库并发布，或用 Git / GitHub CLI 推送。
2. 打开仓库 Settings → Pages，选择 Deploy from a branch。
3. 选择包含这些文件的分支，目录选择 `/docs` 并保存。
4. 等待部署成功，访问 GitHub Pages 显示的实际网址。

官方说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 新人怎么使用

填写 → 复制完整故事卡 → 通过微信等聊天工具发给制作方 → 人物照片原图另发。网站不会自动向制作方提交故事；草稿仅保存在填写者当前浏览器。清空功能会请求确认。更换设备不会同步草稿。

## Codex 接入

制作方将完整故事卡与原始照片交回婚礼制作对话。Codex 将信息录入对应项目，整理事实、制作要求与照片映射，核实关键缺项。第 2 步由 GPT6 在当前 Codex 对话完成文案写作与修改，后续沿用 wedding-video-guided-wizard 的 14 步流程。不要把新人资料或照片提交到这个网站仓库。

## 文件

- `docs/index.html`：采集主页、问题定义与功能逻辑。
- `docs/theme.css`：品牌视觉及手机适配。
- `docs/favicon.svg`：站点图标。
- `docs/LICENSE.txt`：原作者 MIT 授权声明。
- `tests/`：本地浏览器功能验证。

本项目基于 aaronyi97/wedding-video-guided-wizard 的故事采集卡改编，保留原作者及贡献者版权声明。页面装饰为 CSS 图形，没有使用新人素材或虚构案例。
