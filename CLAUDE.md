# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

个人主页项目，单文件静态页面（`index.html`），纯 HTML + CSS + JS，无构建工具。

## 技术要点

- 深色科技风主题，CSS 变量统一管理配色，定义在 `:root` 中（`--primary: #00d4aa`, `--bg: #0a0e17` 等）
- 背景装饰：CSS 网格纹理 + 两个模糊光晕圆，固定定位、不可交互
- 外部依赖：Google Fonts（JetBrains Mono + Noto Sans SC）、qrcodejs CDN（二维码生成）
- 响应式：640px 断点，单列布局切换
- 交互：卡片 hover 边框发光、按钮上浮阴影、锚点平滑滚动
- 二维码使用 qrcodejs 库动态渲染到 `#qrcode` 容器，目标链接在 `<script>` 中配置

## 修改指南

- 个人信息（姓名、邮箱、职位、公司名、技能标签、履历等）直接替换 HTML 中对应文本
- 配色调整只需修改 `:root` 中的 CSS 变量
- 二维码目标链接修改第 547 行 `text` 字段的值
- 头像目前是纯 CSS 文字占位，替换为真实照片时修改 `.avatar` 样式为背景图
