# 架构设计

## 总体架构

```mermaid
flowchart TD
  A[Markdown 内容 docs/] --> B[MkDocs 构建]
  C[mkdocs.yml / 主题配置] --> B
  B --> D[静态站点站点文件]
  D --> E[Vercel 部署]
```

## 技术栈
- **站点生成:** MkDocs + Material for MkDocs
- **内容:** Markdown
- **部署:** GitHub + Vercel

## 核心流程

```mermaid
sequenceDiagram
  participant U as 作者
  participant G as GitHub Repo
  participant V as Vercel
  U->>G: push 内容与配置
  G->>V: 触发构建
  V->>V: mkdocs build
  V-->>U: 发布静态站点
```

## 重大架构决策

| adr_id | title | date | status | affected_modules | details |
|--------|-------|------|--------|------------------|---------|
| ADR-001 | 以 MkDocs Material 实现博客样式首页与标签体系 | 2026-01-28 | ✅已采纳 | mkdocs-config, content | ../history/2026-01/202601281509_cs_blog_site/how.md#adr-001 |
