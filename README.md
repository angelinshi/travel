# quanzhou · 泉州文化漫游

一个无需安装、无需构建的静态导览站点。主页连接开元寺、承天寺和鲤城区小巷三份完整手册，适合自己阅读或带朋友步行漫游。

## 页面

| 入口 | 内容 |
| --- | --- |
| `index.html` | quanzhou 主页，三个图文导览入口 |
| `kaiyuan-temple-guide.html` | 开元寺：21站、77张点位图片 |
| `chengtian-temple-guide.html` | 承天寺：26站、126张点位图片 |
| `quanzhou-old-town-lanes-guide.html` | 鲤城区小巷：24站、73张点位图片 |

手册包含连贯正文、独立知识模块、照片相册、原配套路线图、历史线索跳转、目录搜索，以及折叠保存的转写和资料出处。

## 本地使用

解压后，用浏览器打开 `index.html` 即可。主页和三份手册保持在同一文件夹；主页使用相对链接，适用于本地文件和 GitHub Pages 项目路径。

三份手册各自内嵌图片、地图、CSS与JavaScript，单独复制任意一份手册也可以离线阅读。只有点击资料出处中的外部网页链接才需要联网。无需 npm、Python、数据库或任何账户即可浏览。

## 上传到 GitHub

承天寺约46 MiB、小巷约28 MiB，超过 GitHub 网页上传的单文件25 MiB限制。请使用 GitHub Desktop 或 Git。所有文件均小于 Git 常规上传的100 MiB单文件上限，无需 Git LFS。

### 方法一：GitHub Desktop

1. 解压本项目，安装并登录 GitHub Desktop。
2. 选择 **File → Add Local Repository**，选中解压得到的 `quanzhou` 文件夹。
3. 若提示该目录还不是Git仓库，使用界面中的 **create a repository here**，确认仓库位置为这个文件夹，避免再多嵌套一层。
4. 如文件尚未提交，填写提交说明并提交；随后点 **Publish repository**，仓库名填写 `travel`，按需要选择可见性。

下载的ZIP只包含项目文件，不含本机Git历史；同时提供的本地仓库文件夹已初始化 `main` 分支。远程仓库地址为 `https://github.com/angelinshi/travel.git`；GitHub Pages 需在仓库设置中启用。

### 方法二：Git命令

先在GitHub新建名为 `travel` 的空仓库，不勾选自动生成README、License或.gitignore。然后在本项目文件夹打开终端：

```bash
git init -b main
git add .
git commit -m "Add Quanzhou cultural walking guides"
git remote add origin https://github.com/angelinshi/travel.git
git push -u origin main
```

本项目对应的远程仓库为 `angelinshi/travel`。若直接使用已初始化的本地仓库文件夹，可以跳过第一行。Git会使用你本机已配置的身份和认证方式。

## 用 GitHub Pages 发布

1. 文件推送后，打开仓库的 **Settings → Pages**。
2. 在 **Build and deployment** 中选择 **Deploy from a branch**。
3. 分支选 `main`，目录选 **/ (root)**，保存。
4. 等待GitHub完成部署，在该设置页打开它给出的站点地址。

项目仓库的典型地址为 `https://angelinshi.github.io/travel/`。根目录的 `index.html` 是首页；`.nojekyll` 表示直接提供静态文件，不需要Jekyll加工。仓库可见性与账户方案会影响Pages的可用设置，以GitHub页面提示为准。

## 修改与维护

- 调整主页：编辑 `index.html` 的文字、样式和卡片链接。
- 修改手册时保留页面内的数据与脚本结构。图片以数据地址内嵌，所以文件较大。
- `.gitattributes` 对三份导览关闭文本diff显示，以免大量图片编码干扰查看；不影响浏览器使用，也不会删除内容。
- 这是一份可直接部署的网站成品仓库，不需要构建工具；原始PDF和完整制作过程未重复打包。

## 资料与阅读说明

手册根据所提供《来去泉州》相关转写、配套图片及补充文史材料整理。各章“深入了解”保存转写、校读说明和资料链接；历史、传说与读图解释在正文中分别表述。路线图用于相对位置对照，不提供实时定位；通行、馆舍开放与住宅参观以现场许可为准。

## 官方操作文档

- [GitHub文件上传与大小限制](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github)
- [添加文件到仓库](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
- [配置GitHub Pages发布分支](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
