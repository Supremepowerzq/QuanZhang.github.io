# 个人主页（GitHub Pages）

这是一个极简、可直接部署到 GitHub Pages 的静态个人主页模板，已预填示例内容（Wenye Yu）。你可在本地修改后推送到你的 `<用户名>.github.io` 仓库，即可在线访问。

## 目录结构

```
./
├─ index.html         # 页面主体
└─ assets/
   └─ style.css       # 页面样式
   └─ profile.jpg     # 你的头像（请自行替换，同名放这里）
```

> 如无头像，可删除 `index.html` 中相关 `<img>`，或改为你的远程图片地址。

## 使用步骤（发布到 GitHub Pages）

1) 在 GitHub 上新建一个公开仓库，名称必须为：
   - `<你的GitHub用户名>.github.io`

2) 将本项目文件上传到该仓库根目录（包含 `index.html` 与 `assets/`）。
   - 方式A：直接在 GitHub 网页端「Add file → Upload files」。
   - 方式B：本地 Git 推送：

```bash
# 在本项目目录中初始化并推送（将 USERNAME 改为你的GitHub用户名）
git init
git add .
git commit -m "init: personal homepage"
git branch -M main
git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
git push -u origin main
```

3) 打开仓库的 Settings → Pages：
   - Source 选择 `Deploy from a branch`
   - Branch 选择 `main` 与根目录 `/`，保存。
   - 数十秒后访问：`https://<你的GitHub用户名>.github.io/`

> 若你需要自定义域名，在同一页面绑定域名并在仓库根目录添加 `CNAME` 文件（内容为你的域名）。

## 如何个性化

- 修改 `index.html` 顶部的个人信息、链接（Email/Scholar/Twitter/GitHub）。
- 替换头像：将你的头像命名为 `profile.jpg` 放入 `assets/`。
- 更新 News / Research / Awards / Service / Misc 文本为你的内容。
- 样式：在 `assets/style.css` 中微调配色、间距、字体等。

## 常见问题

- 页面未更新：确认是否推送到 `main` 分支且在 Settings → Pages 中选择了正确分支与目录。
- 样式未生效：检查 `index.html` 中 `<link rel="stylesheet" href="assets/style.css" />` 路径是否正确。
- 需要禁用 Jekyll：若使用了以下划线开头的文件夹，可在仓库根目录创建空文件 `.nojekyll`。

## 致谢

本页样式灵感与学术主页结构参考学术社区常见模板；你提供的参考仓库示例见：

- QuanZhang.github.io（GitHub Pages 示例仓库）：https://github.com/Supremepowerzq/QuanZhang.github.io


