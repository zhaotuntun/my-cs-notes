# 任务清单: 计算机学习博客站点（MkDocs Material）

> **状态:** 已执行（开发实施）

目录: `helloagents/history/2026-01/202601281509_cs_blog_site/`

---

## 1. 信息架构与导航
- [√] 1.1 更新 `mkdocs.yml` 顶部导航为「主页/公开课/工具/语言/杂项/其他」，并确保所有 nav 指向的 Markdown 文件存在，验证 why.md#需求-结构化导航与栏目框架-场景-新增内容后仍可快速定位
- [√] 1.2 为每个栏目创建 index 页（作为目录入口与后续扩展锚点），验证 why.md#需求-结构化导航与栏目框架-场景-新增内容后仍可快速定位

## 2. 首页体验（欢迎区 + 入口卡片 + 最近更新入口）
- [√] 2.1 设计 `docs/index.md` 的首页结构：欢迎区、精选入口卡片、最近更新入口，验证 why.md#需求-首页清晰入口与最近更新入口-场景-首次访问能知道从哪里开始
- [√] 2.2 新增 `docs/assets/stylesheets/extra.css`，实现轻量视觉增强（不做模板覆盖），验证 why.md#需求-首页清晰入口与最近更新入口-场景-首次访问能知道从哪里开始

## 3. 标签/分类与搜索
- [√] 3.1 在 `mkdocs.yml` 启用 `plugins: [search, tags]` 并新增 `docs/tags.md` 作为标签索引页，验证 why.md#需求-全文搜索--标签分类入口-场景-通过关键词找到知识点
- [√] 3.2 定义“分类式标签”约定（标签前缀）并在示例页面中落地，验证 why.md#需求-全文搜索--标签分类入口-场景-通过关键词找到知识点
- [√] 3.3 配置暗/亮主题切换（palette），并确保搜索提示/高亮等体验项可用

## 4. 安全检查
- [√] 4.1 执行安全检查（按G9: 不提交密钥/令牌、不引入未授权外部服务、避免追踪脚本默认开启）

## 5. 文档更新
- [√] 5.1 同步更新知识库：`helloagents/wiki/modules/mkdocs-config.md`、`helloagents/wiki/modules/content.md`、`helloagents/wiki/modules/deploy.md`
- [√] 5.2 更新 `helloagents/CHANGELOG.md` 与 `helloagents/history/index.md`（执行完成后）

## 6. 质量验证
- [X] 6.1 本地/CI 执行 `mkdocs build --strict` 并修复 nav/链接错误
  > 备注: 当前环境无法从 PyPI 安装依赖（SSL 证书校验失败），且系统未检测到可用的 mkdocs 命令，无法在此处完成构建验证。
- [?] 6.2 抽查：首页布局、标签页、搜索、暗亮主题切换
  > 备注: 需要在本机浏览器预览（`mkdocs serve`）后确认。
