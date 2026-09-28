# nctidSensoryManual · 乳业国创感官体验中心说明书

[在线阅读](https://qukoyk.github.io/nctidSensoryManual/)

伊利国家乳业技术创新中心「感官体验中心」的在线操作手册，覆盖开闭馆与日常流程、远程桌面使用，以及蝶舞、飞花、超脑、止水、幻境、镜心等互动展项的操作方法与常见问题排查。

> 仅限内部使用。

## 仓库说明

本仓库只保存 **Sphinx 构建产物**，推送到 `main` 后由 `.github/workflows/static.yml` 自动发布到 GitHub Pages。

| 路径 | 内容 |
|---|---|
| `index.html` 及各章节 `.html` | 站点页面（勿手改） |
| `_sources/` | 各页面 rst 源文备份 |
| `_static/`、`_images/` | 样式与图片资源 |

**一切内容修改请在 Sphinx 源工程进行**，构建后拷入本仓库。

## 源工程与构建方法

Sphinx 源工程位于本地 OneDrive(含 conf.py、rst 原稿、图片与《复现指南.md》):

```
D:\OneDrive - Noldus Information Technology\4 - 定制开发\伊利国创感官厅说明书
```

环境要求（miniconda base，已装好）：

- Python 3.x
- `sphinx==7.4.7` + `sphinx-press-theme==0.9.1`
- ⚠️ press 主题与 Sphinx 8/9 不兼容，必须钉住 7.4.7

构建:

```bash
cd "/d/OneDrive - Noldus Information Technology/4 - 定制开发/伊利国创感官厅说明书"
C:/Users/Qukoyk/miniconda3/python.exe -m sphinx -b html . _build/html
```

本地预览：浏览器打开 `_build/html/index.html`。

## 发布方法

```bash
# 1. 拷贝构建产物（保留 .git 与 .github，勿删）
cp -r "/d/OneDrive - Noldus Information Technology/4 - 定制开发/伊利国创感官厅说明书/_build/html/"* /d/Codes/nctidSensoryManual/

# 2. 提交并推送
cd /d/Codes/nctidSensoryManual
git add -A && git commit -m "更新说明书" && git push
```

推送后 GitHub Actions 自动部署，约 1–2 分钟生效；页面强刷（Ctrl+F5）可见更新。

## 相关文档

- 源工程目录下的《复现指南.md》：完整的考古结论、环境重建与排障说明
