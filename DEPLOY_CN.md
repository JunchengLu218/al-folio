# GitHub 个人主页部署说明（al-folio）

> 适用于将本仓库发布为 GitHub Pages 个人主页。

## 1. 准备仓库

1. 在 GitHub 创建仓库：
   - 若想发布为**个人主页**，仓库名必须为 `your-username.github.io`。
   - 若是项目页，仓库可任意命名（如 `my-portfolio`）。
2. 将本项目推送到该仓库主分支（`main`）。

## 2. 修改站点配置

编辑 `_config.yml`：

- `url`: 改为 `https://your-username.github.io`
- `baseurl`:
  - 个人主页仓库（`your-username.github.io`）留空
  - 项目仓库填写 `/repo-name`

## 3. 启用 GitHub Pages

在 GitHub 仓库设置中：

1. 进入 `Settings` → `Pages`
2. `Build and deployment` 选择 **GitHub Actions**
3. 保存后，推送代码会自动触发 `.github/workflows/deploy.yml` 进行构建和发布。

## 4. 本地预览（可选）

```bash
bundle install
bundle exec jekyll serve
```

访问 `http://127.0.0.1:4000` 查看效果。

## 5. 更新内容建议

- 个人介绍：`_pages/about.md`
- 在线简历：`_data/cv.yml`
- 社交链接：`_data/socials.yml`
- 头像：`assets/img/prof_pic.jpg`

## 6. 发布检查清单

- [ ] `_config.yml` 的 `url` 与 `baseurl` 配置正确
- [ ] 邮箱、GitHub、LinkedIn 等链接已替换为你的真实信息
- [ ] 简历内容无占位符（如“你的名字”）
- [ ] GitHub Actions 构建成功（Actions 页面绿色）
