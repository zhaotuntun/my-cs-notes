# 项目技术约定

---

## 技术栈
- **文档站点生成:** MkDocs + Material for MkDocs
- **内容格式:** Markdown（UTF-8）
- **部署:** GitHub 仓库 + Vercel 构建部署

---

## 目录约定
- `docs/`: 站点内容（Markdown）
- `mkdocs.yml`: 站点配置（导航、主题、插件）
- `docs/assets/`: 自定义静态资源（CSS/JS/图片）
- `helloagents/`: 项目知识库（SSOT），包含 wiki/、plan/、history/

---

## 内容组织约定
- **优先:** 按课程/专题组织（例如“公开课/语言/工具”）
- **兼容:** 以“文章/随记”形式补充（例如“杂项/其他”）
- **标签体系:** 以 tags 作为统一的“标签/分类”入口（分类以约定的标签前缀实现）

---

## 发布与构建
- **本地预览:** `mkdocs serve`
- **构建检查:** `mkdocs build --strict`
- **Vercel:** 以仓库内容构建输出静态站点

