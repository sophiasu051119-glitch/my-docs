# 使用指南

这个页面记录我实际使用的检查和更新方式。以后如果网站内容有变化，按同一套步骤操作即可。

## 1. 本地构建

在仓库根目录创建虚拟环境并安装依赖：

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m mkdocs build --strict
```

`--strict` 会把警告当作错误处理。我会先在本地解决链接、导航或配置问题，再推送到 GitHub。

## 2. 本地预览

```powershell
python -m mkdocs serve
```

浏览器打开终端显示的地址（通常是 `http://127.0.0.1:8000/`），依次检查首页、关于、使用指南和 API 参考。检查完按 `Ctrl+C` 停止服务。

## 3. 提交和自动部署

1. 用 `git status` 查看本次修改，确认没有把 `.venv/` 和 `site/` 加入提交。
2. 提交并推送到 `main`。
3. 在仓库的 Actions 页面打开本次运行，确认 `build` 和 `deploy` 都成功。
4. 刷新 GitHub Pages 网站，核对新内容是否出现。

工作流只监听 `docs/**`、`mkdocs.yml`、`requirements.txt` 和部署文件。只修改实验报告不会触发部署，这样可以避免与网站无关的重复构建。

[返回首页](index.md) · [查看 API 示例](api.md)

