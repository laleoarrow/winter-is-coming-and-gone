# Winter is Coming and Gone Theme

一款基于 Winter is Coming (Dark Blue) 的暗色主题，强化了选区、搜索匹配和词高亮。已内置原始 Dark Blue 配色（来自 johnpapa.winteriscoming v1.4.4），无需额外安装基底主题。

## 特性
- 亮眼的蓝色光晕选区和词高亮
- 更清晰的搜索匹配提示
- 内置基底主题，开箱即用

## 安装
- **VS Code Marketplace**：待上架后，可在扩展市场搜索 “Winter is Coming and Gone Theme” 直接安装。
- **VSIX 手动安装**：已有 `.vsix` 时执行 `code --install-extension winter-is-coming-and-gone-1.0.0.vsix`。
- **源码安装**：
  ```bash
  git clone git@github.com:laleoarrow/winter-is-coming-and-gone.git
  cp -r winter-is-coming-and-gone ~/.vscode/extensions/
  ```
  重启 VS Code 后在 `Cmd+K Cmd+T`（或 `Ctrl+K Ctrl+T`）中选择主题。

## 设置清理
若之前在 `settings.json` 里手动配置过选区/高亮颜色，安装本主题后可删除 `workbench.colorCustomizations` 中相关条目，避免覆盖主题：
```jsonc
"workbench.colorCustomizations": {
  // 安装主题后可删除整个块
}
```
然后把 `workbench.colorTheme` 改为：
```jsonc
"workbench.colorTheme": "Winter is Coming and Gone Theme"
```

## 开发者打包/发布
需要 Node 18+ 和 npm，以及 VS Code Marketplace 的 PAT（权限：Marketplace Manage + Packaging Read/Write）。
```bash
# 打包（不装全局模块）
npx @vscode/vsce package

# 登录发布者（首次）
npx @vscode/vsce login laleoarrow   # 按提示粘贴 PAT

# 发布
npx @vscode/vsce publish
```
若只需本地安装，可跳过登录/发布步骤，直接使用生成的 `.vsix`。

## 鸣谢
基于 johnpapa 的 Winter is Coming 主题（Dark Blue 方案）。
