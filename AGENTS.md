# 我们的婚礼故事

## 项目入口

- 本项目的故事采集入口使用 https://hertz001cg.github.io/our-wedding-story/ 。
- 源码仓库为 https://github.com/Hertz001Cg/our-wedding-story 。
- 网站文件位于 `docs/`；GitHub Pages 发布源为远端 `main` 分支的 `/docs`。
- 当前本地开发分支为 `codex/wedding-story-homepage`，跟踪 `origin/main`。发布前检查远端是否有新提交，不强制推送。

## 婚礼制作约定

- 沿用 `wedding-video-guided-wizard` 的 14 步与各阶段确认条件。
- 第 1 步包含采集卡信息录入、事实整理、人物照片映射和关键缺项核实。不能把发出链接等同于完成采集。
- 按用户要求，第 2 步由 GPT6 在当前 Codex 对话中写作、审稿和修改，不再要求转交 Kimi。
- 已填写清楚的信息不重复询问；生图仍由制作方在外部 GPT 对话完成。
- 新人资料、照片和生产文件放在独立订单目录（例如 `orders/`），不得提交到网站仓库或发布目录。
- 网站仅在填写者浏览器保存草稿；完整文字和照片通过聊天回传，不假称有自动提交或后台收件功能。

## 验证

- 本地预览：`python -X utf8 -m http.server 8734 --bind 127.0.0.1 --directory docs`。
- 浏览器检查：`tests/browser-smoke.cjs`、`tests/browser-language.cjs`；需要 Playwright，可通过 `PLAYWRIGHT_MODULE` 指定已有模块路径，通过 `BROWSER_BIN` 指定浏览器路径，通过 `CARD_URL` 指定测试网站。
- 使用合成资料测试，发布后核对实际网址及静态文件内容。不要把本地通过等同于线上通过。
