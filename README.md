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

**一切内容修改请在 Sphinx 源工程进行**。


环境要求：

- Python 3.x
- `sphinx==7.4.7` + `sphinx-press-theme==0.9.1`
- ⚠️ press 主题与 Sphinx 8/9 不兼容，必须钉住 7.4.7