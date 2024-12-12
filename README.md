## User Settings

```json
{
  "workbench.colorTheme": "JetBrains Darcula Theme",
  "workbench.iconTheme": "vscode-icons",

  "editor.fontFamily": "Monaco, Menlo, 'Courier New', monospace",
  "editor.fontSize": 16,
  "editor.minimap.enabled": false,
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",

  "windsurf.autocompleteSpeed": "fast",
  "windsurf.enableSupercomplete": false,
  "windsurf.enableAutocomplete": false,

  "gitlens.views.commitDetails.files.layout": "tree",
  "gitlens.ai.model": "openai:o1-preview",
  "gitlens.graph.minimap.enabled": false,
  "gitlens.blame.format": "${author|6?} ${date|11-}",
  "gitlens.blame.dateFormat": "YYYY-MM-DD",

  "terminal.integrated.fontSize": 18,
  "debug.console.fontSize": 18,

  "window.zoomLevel": 0.4,

  "terminal.integrated.fontSize": 18,
  "debug.console.fontSize": 18,

  "window.zoomLevel": 0.4,
  "git-graph.commitDetailsView.location": "Docked to Bottom",
  "git-graph.date.format": "ISO Date & Time",
  "git-graph.repository.commits.fetchAvatars": true,
  "git-graph.repository.commits.initialLoad": 350,

  "diffEditor.ignoreTrimWhitespace": false,

  "git.enableSmartCommit": true,

  "files.autoSave": "afterDelay",

  "terminal.integrated.fontSize": 18,

  "debug.console.fontSize": 18,

  "window.zoomLevel": 0.2
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
  {
    "key": "alt+cmd+b",
    "command": "workbench.action.closePanel"
  },
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
  {
    "key": "cmd+2",
    "command": "git-graph.view"
  },
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
  {
    "key": "cmd+1",
    "command": "workbench.files.action.showActiveFileInExplorer"
  },
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
  {
    "key": "alt+cmd+1",
    "command": "git-graph.openFile"
  }
]
```
