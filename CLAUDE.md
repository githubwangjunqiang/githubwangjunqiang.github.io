# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是「罗盘壁纸」Android App 的官方网站，托管于 GitHub Pages。纯静态 HTML/CSS/JS 实现，无构建工具依赖。

## 自定义域名

域名配置：`finger-t.online`（通过 CNAME 文件配置）

## 文件结构

| 文件 | 说明 |
|------|------|
| `index.html` | 首页，含双语切换、时间罗盘 Canvas 动画 |
| `privacy_policy.html` | 隐私政策 |
| `user_agreement.html` | 用户协议 |
| `CNAME` | GitHub Pages 自定义域名配置 |
| `app-ads.txt` | Google AdMob 验证文件 |
| `assets/icon.svg` | App 图标 |

## 开发说明

### 本地预览

直接用浏览器打开 `index.html` 即可预览。时间罗盘 Canvas 动画依赖 `requestAnimationFrame` 和系统时间实时渲染。

### 语言切换

通过 URL 参数 `?lang=en` 或 `?lang=zh-CN` 控制。默认根据浏览器语言自动选择。

### 时间罗盘动画

`index.html` 内嵌 JavaScript 实现，核心逻辑：
- 5 圈环状文字（月/日/时/分/秒）逆时针排列
- 当前时间项高亮显示（蓝色 `#00C2FF`）
- 红色指示线指向当前值

### 设计风格

暗色主题，配色变量定义在 `:root`：
- 主背景：`#0A1921`
- 强调色：`#00C2FF`
- 卡片背景：`#1A2A33`

### 发布更新

推送至 GitHub `main` 分支后自动部署到 GitHub Pages。

## 相关 App 信息

- App 名称：罗盘壁纸 / Compass Wallpaper
- Google Play：`com.xq.app.luo.pan.bizhi`
- 开发者邮箱：`19901021qiang@gmail.com`