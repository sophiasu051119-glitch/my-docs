# my-docs

这是苏可在开源软件课程中完成的个人 MkDocs 文档网站。仓库使用 GitHub Actions 自动构建，并通过 GitHub Pages 公开发布。

- 网站地址：<https://sophiasu051119-glitch.github.io/my-docs/>
- [个人实验报告](report/README.md)
- 文档源码位于 [`docs/`](docs/)
- 自动部署配置位于 [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)

## 本地预览

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m mkdocs build --strict
python -m mkdocs serve
```

网站由四个页面组成，包含表格、代码块和页面间链接。推送相关文件到 `main` 后，工作流会自动完成构建与部署。
