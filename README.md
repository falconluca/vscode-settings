## User Settings

```json
{
  // 主题
  "workbench.colorTheme": "JetBrains Darcula Theme",
  "editor.tokenColorCustomizations": {
    "[JetBrains Darcula Theme]": {
      "textMateRules": [
        {
          "scope": "entity.name.type.go",
          "settings": {
            "foreground": "#3d9bb8"
          }
        }
      ]
    }
  },

  // "workbench.colorTheme": "Tokyo Night",
  // "workbench.colorTheme": "Tokyo Night Storm",
  
  "workbench.iconTheme": "vscode-icons",

  // "workbench.statusBar.visible": false

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
  "gitlens.launchpad.indicator.enabled": false,

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

  "editor.formatOnSave": true,

  // 格式化
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[less]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[go]": {
    "editor.defaultFormatter": "golang.go",
  },
  "go.formatTool": "gofmt",

  "breadcrumbs.symbolPath": "off",

  "window.title": "${activeRepositoryBranchName}${separator}${rootName}",

  "eslint.enable": true,
  "eslint.validate": [
    "vue",
    "react",
    "javascript",
    "typescript",
    "html"
  ],

  "workbench.startupEditor": "newUntitledFile",
  
  "editor.suggestSelection": "recentlyUsed",
  
  "go.toolsManagement.autoUpdate": true,
  
  "bracketPairColorizer.depreciation-notice": false,
}
```

## Extensions

[GitLens](https://github.com/gitkraken/vscode-gitlens)

[无限试用 GitLens 的方案](https://zhuanlan.zhihu.com/p/675238420)

```
anan.jetbrains-darcula-theme
codeium.windsurfpyright
coenraads.bracket-pair-colorizer
dbaeumer.vscode-eslint
eamodio.gitlens
esbenp.prettier-vscode
golang.go
mhutchie.git-graph
mikoz.black-py
ms-azuretools.vscode-docker
ms-kubernetes-tools.vscode-kubernetes-tools
ms-python.debugpy
ms-python.python
redhat.vscode-yaml
ritwickdey.liveserver
vscode-icons-team.vscode-icons
vue.volar
wayou.vscode-todo-highlight
xabikos.javascriptsnippets
```

导出所有插件：`code --list-extensions > extensions.txt`

安装所有插件：`cat extensions.txt | xargs -L 1 code --install-extension`

## Keyboard Shortcuts

```json
[
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
    "command": "git.openFile"
  },
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
  },

  // 关闭底部面板 PS：类似 CMD+B 关闭左侧面板
  {
    "key": "alt+cmd+b",
    "command": "workbench.action.closePanel"
  },

  // Rollback all changes
  {
    "key": "alt+cmd+z",
    "command": "git.cleanAll"
  },
  // Rollback changes of current open file 
  {
    "key": "alt+cmd+x",
    "command": "git.clean"
  },
  
  // 分屏
  {
    "key": "cmd+s cmd+d",
    "command": "workbench.action.splitEditorDown"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorDown"
  },
  {
    "key": "cmd+s cmd+l",
    "command": "workbench.action.splitEditorLeft"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorLeft"
  },
  {
    "key": "cmd+s cmd+r",
    "command": "workbench.action.splitEditorRight"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorRight"
  },
  {
    "key": "cmd+s cmd+u",
    "command": "workbench.action.splitEditorUp"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorUp"
  },
]
```
