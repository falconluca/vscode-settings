## User Settings

```json
{
  "workbench.colorTheme": "JetBrains Darcula Theme",
  "workbench.iconTheme": "vscode-icons",

  "editor.fontFamily": "Monaco, Menlo, 'Courier New', monospace",
  "editor.fontSize": 16,
  "editor.minimap.enabled": false,

  "windsurf.autocompleteSpeed": "fast",
  "windsurf.enableSupercomplete": false,
  "windsurf.enableAutocomplete": false,

  "gitlens.views.commitDetails.files.layout": "tree",
  "gitlens.ai.model": "openai:o1-preview",
  "gitlens.graph.minimap.enabled": false,
  "gitlens.blame.format": "${author|6?} ${date|11-}",
  "gitlens.blame.dateFormat": "YYYY-MM-DD",

  "git-graph.commitDetailsView.location": "Docked to Bottom",
  "git-graph.date.format": "ISO Date & Time",
  "git-graph.repository.commits.fetchAvatars": true,
  "git-graph.repository.commits.initialLoad": 350,

  "diffEditor.ignoreTrimWhitespace": false,

  "git.enableSmartCommit": true,

  "files.autoSave": "afterDelay",

  "terminal.integrated.fontSize": 18,

  "debug.console.fontSize": 18,

  "window.zoomLevel": 0.2,

  // 格式化
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[less]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true,
  },
  "[go]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "golang.go",
  },
  "go.formatTool": "gofmt",
}
```

## Extensions

[GitLens](https://github.com/gitkraken/vscode-gitlens)

[无限试用 GitLens 的方案](https://zhuanlan.zhihu.com/p/675238420)

```
anan.jetbrains-darcula-theme
coenraads.bracket-pair-colorizer
eamodio.gitlens
esbenp.prettier-vscode
golang.go
mhutchie.git-graph
ritwickdey.liveserver
vscode-icons-team.vscode-icons
vue.volar
```

导出所有插件：`code --list-extensions > extensions.txt`

安装所有插件：`cat extensions.txt | xargs -L 1 code --install-extension`

## Keyboard Shortcuts

```json
[
  // 关闭底部面板 PS：类似 CMD+B 关闭左侧面板
  {
    "key": "alt+cmd+b",
    "command": "workbench.action.closePanel"
  },

  // 打开内置 SCM（源代码管理）面板
  {
    "key": "shift+cmd+g",
    "command": "workbench.view.scm",
    "when": "workbench.scm.active"
  },
  {
    "key": "shift+ctrl+g",
    "command": "workbench.view.scm",
    "when": "-workbench.scm.active"
  },

  // 打开 git graph
  {
    "key": "cmd+2",
    "command": "git-graph.view"
  },

  // 打开、关闭 git blame
  {
    "key": "cmd+3",
    "command": "gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'alternate' && resource in 'gitlens:tabs:blameable'"
  },
  {
    "key": "alt+b",
    "command": "-gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'alternate' && resource in 'gitlens:tabs:blameable'"
  },
  {
    "key": "cmd+3",
    "command": "gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'chorded' && resource in 'gitlens:tabs:blameable'"
  },
  {
    "key": "alt+cmd+g b",
    "command": "-gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'chorded' && resource in 'gitlens:tabs:blameable'"
  },
  
  // 定位到当前文件
  {
    "key": "cmd+1",
    "command": "workbench.files.action.showActiveFileInExplorer"
  },

  // 打开、关闭终端
  {
    "key": "cmd+4",
    "command": "workbench.action.terminal.toggleTerminal",
    "when": "terminal.active"
  },
  {
    "key": "ctrl+`",
    "command": "-workbench.action.terminal.toggleTerminal",
    "when": "terminal.active"
  },

  // 打开 git diff 文件
  {
    "key": "alt+cmd+1",
    "command": "git-graph.openFile"
  },

  // 模拟 Goland 复杂到下一行
  {
    "key": "cmd+d",
    "command": "editor.action.copyLinesDownAction",
    "when": "editorTextFocus && !editorReadonly"
  },
  {
    "key": "shift+alt+down",
    "command": "-editor.action.copyLinesDownAction",
    "when": "editorTextFocus && !editorReadonly"
  }
]
```
