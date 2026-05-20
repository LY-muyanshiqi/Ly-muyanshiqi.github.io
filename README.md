# 暮烟十七 | 个人网站

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-在线演示-222222?style=flat-square&logo=github)](https://ly-muyanshiqi.xyz)
[![HTML5](https://img.shields.io/badge/HTML5-语义化-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/zh-CN/docs/Web/HTML)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

> 我的个人作品集网站，展示智慧水利 + AI 项目成果与研究经历。

在线访问：[**ly-muyanshiqi.xyz**](https://ly-muyanshiqi.xyz)

---

## 页面结构

- **Hero** — 头像、一句话介绍、CTA 按钮
- **关于我** — 个人简介 + 数据统计（GPA、项目数、专利）
- **技能栈** — 6 大技能分类标签云（Python · ML · 建模 · 工程 · 水利 · 学术）
- **项目 & 竞赛** — 8 张项目卡片，展示研究成果
- **成就 & 规划** — 时间线展示成长轨迹
- **联系我** — 邮箱 + GitHub + CSDN 联系方式

## 技术栈

- 纯静态 HTML5 + CSS3 + Vanilla JS（零依赖框架）
- Font Awesome 6.5 图标（bootcdn.net CDN 国内加速）
- CSS 自定义属性（变量）+ Flexbox/Grid 响应式布局
- IntersectionObserver 滚动动画 + CountUp 数字动画
- JSON-LD 结构化数据 + Open Graph + Twitter Card（SEO 最佳实践）
- GitHub Pages + 自定义域名（CNAME）

## 本地运行

```bash
# 方式 1：直接打开
open index.html

# 方式 2：本地服务器
python -m http.server 8080
# 浏览器访问 http://localhost:8080
```

## 部署

推送到 `main` 分支即自动部署到 GitHub Pages。
