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

## 发布要求

后续修改本项目网页内容后，默认执行以下流程：

1. 本地检查网页可访问。
2. 提交到 Git。
3. 推送 `main` 到 GitHub 仓库 `gabriel-0225/155map`。
4. 部署到 Netlify 项目 `155map`。

Netlify 站点信息：

- Site ID: `5aaed50b-04dd-4d65-b501-2b6abb16532c`
- URL: `https://155map.netlify.app/`
