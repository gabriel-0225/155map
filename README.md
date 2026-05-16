# 十五五产业地图静态网站

这个目录就是可分享的网站发布包。

线上地址：

```text
https://155map.netlify.app/
```

## 文件

- `index.html`：网站首页，包含规划学习板块、思维导图入口、股票池走势。
- `fifteenth-five-year-mindmap.html`：交互式思维导图页面，被首页嵌入，也可单独打开。

## 本地预览

在本目录运行：

```bash
python3 -m http.server 4173
```

然后打开：

```text
http://127.0.0.1:4173/
```

## 分享部署方式

任选一种：

1. GitHub Pages  
   新建一个 GitHub 仓库，把本目录里的文件上传到仓库根目录，然后在仓库 `Settings -> Pages` 中选择 `Deploy from a branch`，分支选 `main`，目录选 `/root`。

2. Vercel  
   登录 Vercel，新建项目，导入包含这些文件的仓库。框架选择 `Other`，无需构建命令，输出目录留空或使用根目录。

3. Netlify  
   当前项目已部署到 Netlify 项目 `155map`。后续修改完成后，提交并推送到 GitHub，再部署到同一个 Netlify 站点，即可让访问者看到最新版网页。

4. 普通网站空间  
   把 `index.html` 和 `fifteenth-five-year-mindmap.html` 上传到同一个目录，访问该目录对应的网址即可。

## 后续更新流程

1. 修改本目录中的静态文件。
2. 本地检查页面可访问。
3. 提交到 Git，并推送 `main` 到 GitHub 仓库 `gabriel-0225/155map`。
4. 部署到 Netlify 站点 `155map`，站点 ID：`5aaed50b-04dd-4d65-b501-2b6abb16532c`。

以后由 Codex 修改本项目时，默认按以上流程同步线上版本。

## 注意

股票池行情图表通过浏览器请求东方财富公开接口生成。若访问者所在网络限制该接口，页面仍能展示网站主体和股票池列表，但走势图可能需要稍后刷新。
