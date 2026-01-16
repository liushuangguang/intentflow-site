# 如何将此网站发布到公网 (完全免费)

本网站采用纯静态 HTML 架构，可以利用 **GitHub Pages** 服务进行**永久免费**托管，并自动获得 HTTPS 安全证书。

## 步骤 1：准备 GitHub 仓库

1.  登录您的 GitHub 账号。
2.  创建一个新仓库 (New Repository)，例如命名为 `intentflow-site`。
3.  **不要**勾选 "Initialize with README"（如果你是新建空项目）。

## 步骤 2：上传代码

您可以使用 Git 命令行或直接在网页上传。

### 方法 A: 网页上传 (最简单)
1.  在 GitHub 仓库页面，点击 **"Add file"** -> **"Upload files"**。
2.  将本地的 `website` 文件夹中的**所有文件**（`index.html`, `privacy.html` 等）拖入上传区域。
    *   **注意**：请确保 `index.html` 在仓库的**根目录**，或者在某个子目录下（如 `/website`）。
    *   *建议*：为了方便，您可以直接把 `website` 文件夹里的内容上传到仓库根目录。
3.  点击底部的 **"Commit changes"**。

### 方法 B: 命令行 (推荐)
```bash
cd i:/下载/google_AI_studio_download_liulanqichajian/website
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/您的用户名/intentflow-site.git
git push -u origin main
```

## 步骤 3：开启 GitHub Pages 服务

1.  进入仓库的 **Settings (设置)** 页面。
2.  在左侧菜单栏找到 **Pages** (位于 "Code and automation" 区域)。
3.  在 **Build and deployment** -> **Source** 中选择 **Delay from a branch**。
4.  在 **Branch** 选项中：
    *   选择 `main` (或 `master`) 分支。
    *   文件夹选择 `/(root)` (如果您把文件放在了根目录)。
5.  点击 **Save (保存)**。

## 步骤 4：等待发布

1.  保存后，GitHub 会自动开始构建（通常只需 1 分钟）。
2.  刷新页面，您会在顶部看到一个绿色的提示框：
    > "Your site is live at https://您的用户名.github.io/intentflow-site/"
3.  点击该链接，您的官网就已经全球可访问了！

## 后续更新

*   如果需要更新网站，只需修改本地文件，然后再次上传/Push 到 GitHub，网站会自动更新。
*   **下载链接配置**：
    *   请记得将 `index.html` 中的 "添加到 Chrome" 链接修改为您在 Chrome 商店的真实地址。
    *   如果是提供离线下载，可以将 `.zip` 文件也上传到仓库，并将链接指向该文件（如 `./intentflow-v1.0.zip`）。
