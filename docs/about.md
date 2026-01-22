# 关于
作为与嵌入式系统相处人生近半时间的中年人，我深知嵌入式系统的复杂性和挑战性。
在这个领域，我积累了丰富的经验和教训，也参与了多个有趣的项目和实验。
我希望本栏目能够帮助其他嵌入式系统爱好者，分享我的经验和知识，
并启发他们在嵌入式系统领域的创新和发展。



## 下载与备份（本地）

### 1) 最推荐：用 Git 备份（含历史版本）
```bash
git clone https://github.com/<YOUR_GITHUB_USERNAME>/<REPO_NAME>.git
```

### 2) 导出静态站（可打包迁移）
```bash
mkdocs build
```
输出目录：`site/`

你可以把 `site/` 压缩并拷走（脱离 GitHub 也能部署到任何静态托管）：

```bash
zip -r site.zip site/
```

### 3) 发布到其他托管平台
常见静态托管：GitHub Pages / Gitee Pages / Cloudflare Pages / Netlify / Vercel

迁移时只需要：
- 拿到仓库代码（或 `site/` 静态目录）
- 新平台重新部署
- （可选）更新 `mkdocs.yml` 里的 `site_url`

