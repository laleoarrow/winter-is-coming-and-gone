# Winter is Coming and Gone Theme

基于 "Winter is Coming (Dark Blue)" 主题，增强了选中文本的高亮效果。

已内置原始 "Winter is Coming (Dark Blue)" 主题文件（johnpapa.winteriscoming v1.4.4），无需额外安装基底主题。

## 特性

- 🔵 蓝色光晕效果的词语高亮
- ✨ 更清晰的选中区域显示
- 🔍 优化的搜索匹配高亮

## 安装方式

### 方式 1：直接复制到扩展目录（推荐）

```bash
cp -r /Users/leoarrow/Project/mypackage/winter-is-coming-and-gone ~/.vscode/extensions/
```

重启 VS Code 后，使用 `Cmd+K Cmd+T` 选择 "Winter is Coming and Gone Theme"。

### 方式 2：打包安装

```bash
# 安装打包工具（首次）
npm install -g @vscode/vsce

# 打包
cd /Users/leoarrow/Project/mypackage/winter-is-coming-and-gone
vsce package

# 安装 .vsix 文件
code --install-extension winter-is-coming-and-gone-1.0.0.vsix
```

## 使用后的配置清理

安装主题后，你可以从 `settings.json` 中**删除**：

```jsonc
// 删除整个 workbench.colorCustomizations 块
"workbench.colorCustomizations": {
    "editor.selectionBackground": "#4A90E2AA",
    // ... 这里的所有内容都可以删掉
}
```

然后**修改主题名称**：

```jsonc
"workbench.colorTheme": "Winter is Coming and Gone Theme"
```

⚠️ **注意**：其他编辑器配置（字体、字号、tab大小等）需要保留在 settings.json 中，它们不属于主题范围。

## 备份完整设置（可选）

如果想同时备份所有编辑器设置：

```bash
# 备份 settings.json
cp ~/Library/Application\ Support/Code/User/settings.json \
   /Users/leoarrow/Project/mypackage/winter-is-coming-and-gone/my-settings.json

# 备份 keybindings.json
cp ~/Library/Application\ Support/Code/User/keybindings.json \
   /Users/leoarrow/Project/mypackage/winter-is-coming-and-gone/my-keybindings.json
```

新电脑恢复：
```bash
cp my-settings.json ~/Library/Application\ Support/Code/User/settings.json
cp my-keybindings.json ~/Library/Application\ Support/Code/User/keybindings.json
```

## 发布到 GitHub

```bash
cd /Users/leoarrow/Project/mypackage/winter-is-coming-and-gone
git init
git add .
git commit -m "Initial commit: Winter is Coming and Gone Theme"
git remote add origin https://github.com/你的用户名/winter-is-coming-and-gone.git
git branch -M main
git push -u origin main
```

## 发布到 VS Code Marketplace

1. 访问 https://marketplace.visualstudio.com/manage
2. 创建发布者账号并获取 Personal Access Token
3. 发布：

```bash
vsce login leoarrow
vsce publish
```

## 换电脑后的安装

只需要复制这个文件夹到新电脑的 `~/.vscode/extensions/` 目录即可。
