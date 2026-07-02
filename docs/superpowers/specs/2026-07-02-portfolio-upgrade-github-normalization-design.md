# 个人网站升级 + GitHub 规范化 设计文档

## 项目 A：个人网站升级 (portfolio-remote)

### 架构
纯静态 HTML/CSS/JS，零框架依赖。引入 marked.js CDN 做 Markdown 渲染。

### 文件结构
```
portfolio-remote/
  index.html              # 首页（单页增强：筛选标签 + 搜索）
  projects/
    pccp.html             # PCCP-E 环向变形预测
    badao-weiyi.html      # 坝道微医
    smart-water.html      # 智慧水利预测系统
    thermal-peak.html     # 火电调峰+抽蓄优化
    huazhong-cup.html     # 华中杯 VRP
    corn-modeling.html    # 统计建模·玉米产量
    pumped-carbon.html    # 抽蓄碳减排
    piezoelectric.html    # 压电换能器仿真
    energy-conservation.html # 节能减排竞赛
  blog/
    index.html            # 博客列表（从 articles.json 渲染）
    article.html          # 文章详情（?id=xxx 参数加载）
  articles.json           # 文章元数据索引
  assets/articles/        # Markdown 文章文件
  projects.html           # 保留，跳转到 /#projects
```

### 改动清单

| # | 模块 | 说明 |
|---|------|------|
| 1 | 首页增强 | 项目卡片区加标签筛选按钮 + 搜索框 |
| 2 | 项目详情页 x9 | 每页：背景、架构图 SVG、技术栈、成果指标、GitHub 链接 |
| 3 | 博客列表 | /blog/index.html 卡片式列表，标签筛选 |
| 4 | 文章详情 | /blog/article.html?id=xxx 用 marked.js 渲染 |
| 5 | 导航更新 | 加"博客"入口 |
| 6 | 文章筛选 | blog-files 选 4-5 篇高质量→assets/articles/ |

### 入选文章
1. 智慧水利项目实战（六）：GRU模型部署与实时预测系统 (5/5)
2. 智慧水利项目实战（五）：LSTM vs GRU模型对比实验 (5/5)
3. Python在水利工程数据处理中的应用 (3/5)
4. 智慧水利项目实战：从零搭建GitHub开源项目 (3.5/5)

---

## 项目 B：GitHub 仓库规范化

### 操作矩阵

| 仓库 | Topics | CI Badge | Release |
|------|--------|----------|---------|
| PCCP | deep-learning, structural-health-monitoring, pipeline, tensorflow | 补 badge | v1.0.0 |
| smart-water-demo | flood-prediction, lstm, streamlit, water-resources | 补 badge | v1.0.0 |
| smart-water-projects | awesome-list, water-resources, smart-water | - | v1.0.0 |
| blog-files | blog, csdn, markdown | - | v1.0.0 |
| thermal-peak-shaving-pumped-storage | optimization, pumped-storage, carbon-reduction, nsga-ii | 已有 | 已有 |
| huazhong-cup-vrp | vehicle-routing, optimization, logistics, hybrid-ils | 补 badge | v1.0.0 |
| statistical-modeling-corn | remote-sensing, crop-yield, lstm, xgboost | - | v1.0.0 |
| badao-weiyi | dam-safety, ai-diagnosis, water-engineering | - | v1.0.0 |
| pumped-storage-carbon | pumped-storage, lstm, carbon-reduction, energy | 补 badge | v1.0.0 |
| LY-muyanshiqi | github-profile | - | v1.0.0 |

### 执行方式
- Topics: GitHub API `gh api repos/LY-muyanshiqi/<repo> -X PATCH`
- CI Badge: 本地编辑 README.md + commit + push
- Release: `git tag v1.0.0 && git push --tags`
