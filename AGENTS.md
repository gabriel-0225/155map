# Project Instructions

禁止批量删除文件或目录。

不要使用：

- `del /s`
- `rd /s`
- `rmdir /s`
- `Remove-Item -Recurse`
- `rm -rf`

需要删除文件时，只能一次删除一个明确路径的文件。

正确示例：

```powershell
Remove-Item "C:\path\to\file.txt"
```

如果需要批量删除文件，应停止操作，并询问用户，让用户手动删除。

## 修改保存要求

后续每次修改本项目文件后，默认执行本地检查并提交到 Git，作为本地保存点。

每次保存 Git 时，提交信息必须用中文说明本次修改；在 `git log --oneline` 中，提交编号后面的修改说明要用中文表达。

默认不自动推送 GitHub、不自动部署 Netlify。

## 发布要求

只有当用户明确要求“提交 GitHub”“发布”“部署 Netlify”或同等含义时，才执行以下流程：

1. 本地检查网页可访问。
2. 确认最新修改已提交到 Git。
3. 推送 `main` 到 GitHub 仓库 `gabriel-0225/155map`。
4. 部署到 Netlify 项目 `155map`。

Netlify 站点信息：

- Site ID: `5aaed50b-04dd-4d65-b501-2b6abb16532c`
- URL: `https://155map.netlify.app/`
