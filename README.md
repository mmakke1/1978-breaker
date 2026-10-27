# 《1978：破局者》

一款无需框架、无需后端、无需安装依赖的中文互动历史叙事网站。

## 直接试玩

打开 `index.html` 即可游玩。使用 HTTP/HTTPS 访问时还支持离线缓存和“添加到主屏幕”。

## 内容与路线

- 五个历史节点：1977 恢复高考、1978 农村改革、1980 经济特区、1984 城市改革、1992 南方谈话。
- 每个节点有三种带有不同取舍的方案。不存在 Game Over；路线会影响后续叙述、能力取向和结局。
- 结尾可生成并下载包含玩家姓名与路线印章的 PNG 见证卡。
- 使用原创 Canvas 档案版画，无外部图片、字体、音频、API 或第三方运行时依赖。
- 部分选项是用来讨论改革取舍的假设情境，并非历史人物真实决策的还原；详见游戏内历史档案。

## 发布到公开网站（GitHub Pages，免费）

本项目已经带有 `.github/workflows/pages.yml` 发布工作流。发布一次后，任何人都可以通过 GitHub Pages 链接访问。

1. 在 GitHub 新建一个 **Public** 仓库，例如 `1978-breaker`。
2. 将本目录（`outputs`）的全部内容，包括隐藏的 `.github` 文件夹，作为仓库根目录内容上传。建议用 GitHub Desktop，或在本目录终端运行：

   ```powershell
   git init
   git add .
   git commit -m "Publish 1978 Breaker game"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/1978-breaker.git
   git push -u origin main
   ```

3. 在仓库的 **Settings → Pages** 中，把构建来源设为 **GitHub Actions**。
4. 等仓库 **Actions** 页面的 `Publish 1978 Breaker` 完成。公开地址通常为 `https://<你的用户名>.github.io/1978-breaker/`。

仓库所有者的 GitHub 登录和公开仓库创建需要由你本人完成；本项目不需要 API 密钥、服务器或数据库。也可以把本目录拖入支持静态站点托管的平台，上传后即可获得公开链接。

## 文件

- `index.html`：页面结构与游戏模板
- `styles.css`：复古视觉、动画和响应式样式
- `app.js`：章节、分支、路线反馈、结局和海报
- `service-worker.js`、`manifest.webmanifest`、`icon.svg`：离线缓存与可安装网页支持
- `.github/workflows/pages.yml`：GitHub Pages 自动发布配置
