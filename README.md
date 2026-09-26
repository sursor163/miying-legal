# 觅影 · Shadowseek — 法律与支持站点

《觅影》（Shadowseek，采光计算专家）的隐私政策与技术支持页面，通过 GitHub Pages 对外发布。

## 线上地址（App Store 上架填写这两条）

- 隐私政策：<https://sursor163.github.io/miying-legal/privacy/>
- 技术支持：<https://sursor163.github.io/miying-legal/support/>

页面结构：

- 首页：`/` — 法律与支持中心
- 隐私政策：`/privacy/`
- 技术支持与常见问题：`/support/`

纯静态站点，无构建步骤、无外部依赖。每个页面内置中英双语切换。

## ⚠️ 更新页面时必须推两个分支

本仓库的 Pages 发布源是 **`gh-pages` 分支**（不是 `main`）。只推 `main` 的话，线上仍然是旧版本。

```bash
git add -A && git commit -m "说明本次改动"
git push origin main
git push origin main:gh-pages   # 这一条不能少
```

推送后约 30–60 秒生效，可用下面的命令确认线上已是新版：

```bash
curl -s https://sursor163.github.io/miying-legal/privacy/ | grep -c "关键词"
```

## 内容维护约定

页面上的收费说明必须与 App 内实际逻辑一致。已知的强绑定项：

- 免费试用是**按设备**一次（Keychain 防重装），不是"每次安装一次"
- 付费是**消耗型按次**，不是一次性买断；已生成的报告重复打开/导出不再收费
- **不存在「恢复购买」入口**（消耗型内购没有恢复语义），文案里也不应出现
- 付费生成的报告**不会被自动清理**；只有免费试用的记录受 100 条上限约束
