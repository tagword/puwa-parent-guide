# 发布说明

## 目标

把本书发布到 GitHub Pages，让家长能在线检索。

## 前置条件

1. GitHub 账号，已建好仓库（如 `puwa-parent-guide`）
2. 本地已配置 git 的 SSH key 或 token

## 步骤

### 1. 关联远程仓库

```bash
cd /home/u2/infos/puwa-parent-guide
git remote add origin git@github.com:<你的用户名>/puwa-parent-guide.git
git branch -M main
git push -u origin main
```

### 2. 开启 GitHub Pages

仓库 → Settings → Pages：
- Source 选 `Deploy from a branch`
- Branch 选 `main`，目录选 `/ (root)`
- 保存

约 1 分钟后访问：`https://<你的用户名>.github.io/puwa-parent-guide/`

### 3. 验证

- [ ] 首页 `index.html` 正常渲染，条目数显示 70
- [ ] 搜索"补习"能返回结果
- [ ] 筛选"证据 C"能返回 2 条
- [ ] 手机端布局正常
- [ ] `README.md`、`book/` 链接可点

## 说明

- 本页是纯静态文件，无需构建步骤
- `.nojekyll` 已加，避免 GitHub Pages 的 Jekyll 处理干扰
- 检索页通过相对路径 `book/*.md` 加载正文，Pages 环境下正常

## 备选：本地预览

```bash
python3 -m http.server 8088
# 访问 http://localhost:8088/
```
