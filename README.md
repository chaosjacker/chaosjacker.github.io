# GitHub Pages 个人主页模板

一个开箱即用的 GitHub 个人主页，自动拉取 GitHub API 数据，无需后端。

## 功能

- 顶部横幅 + 个人简介 + 技术标签
- 摸鱼计时器（实时倒计时距离上次 commit 的时间）
- GitHub 概览（仓库数 / Star 总数 / 关注者）
- 常用语言占比条（自动统计所有仓库）
- 最近仓库动态列表
- 响应式布局，手机端自适应

## 使用方法

### 1. Fork 或新建仓库

在 GitHub 上新建一个仓库，名字必须是：

```
你的用户名.github.io
```

例如用户名叫 `abc`，仓库名就叫 `abc.github.io`。

### 2. 上传 index.html

把本目录的 `index.html` 上传到仓库根目录。

### 3. 修改配置

打开 `index.html`，找到这一行，把 `fantuanmtf` 改成你自己的 GitHub 用户名：

```js
const GH_USER = "fantuanmtf";   // ← 改成你的用户名
```

### 4. 自定义内容

- **横幅图片**：找到 `<img class="banner-img" src="...">`，把 `src` 换成你喜欢的图片链接
- **技术标签**：修改 `<div id="tagWrap">` 里的 `<span class="tag">` 内容
- **个人简介**：会自动从 GitHub profile 的 bio 读取，也可以在 GitHub 网站上修改

### 5. 开启 GitHub Pages

仓库 → **Settings** → **Pages** → Source 选 `main` 分支 / `(root)` → 保存。

等待 1~3 分钟，访问 `https://你的用户名.github.io` 即可。

## 注意事项

- GitHub API 未认证状态下每小时限 **60 次请求**，访问量大会被限流。如果需要更高额度，可以去 GitHub 生成一个 Personal Access Token（仅 public_repo 权限），并在代码里加上请求头。
- 仓库默认设为 Public，Pages 才能免费使用。
- 语言占比是按仓库 size 粗略统计的，仅供参考。
