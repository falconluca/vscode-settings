## User Settings

```json
{
  "workbench.colorTheme": "Default Dark+",
  "workbench.iconTheme": "vscode-icons",

  "editor.fontFamily": "Monaco, Menlo, 'Courier New', monospace",
  "editor.fontSize": 14,
  "editor.minimap.enabled": false,

  "gitlens.graph.minimap.enabled": false,
  "gitlens.blame.format": "${author|6?} ${date|11-}",
  "gitlens.blame.dateFormat": "YYYY-MM-DD",
  "gitlens.launchpad.indicator.enabled": false,

  "git-graph.commitDetailsView.location": "Docked to Bottom",
  "git-graph.date.format": "ISO Date & Time",
  "git-graph.repository.commits.fetchAvatars": true,
  "git-graph.repository.commits.initialLoad": 350,

  "diffEditor.ignoreTrimWhitespace": true,

  "git.enableSmartCommit": true,

  "files.autoSave": "afterDelay",

  "debug.console.fontSize": 18,

  "window.zoomLevel": 1.8,
  "editor.mouseWheelZoom": true,

  "editor.formatOnSave": true,
  "editor.rulers": [120],
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
    "editor.rulers": [100]
  },
  "go.formatTool": "gofmt",

  "breadcrumbs.symbolPath": "off",

  // "window.title": "${activeRepositoryBranchName}${separator}${rootName}",
  "window.title": "${rootName}",

  "eslint.enable": true,
  "eslint.validate": ["vue", "react", "javascript", "typescript", "html"],

  "workbench.startupEditor": "newUntitledFile",

  "editor.suggestSelection": "recentlyUsed",

  "workbench.editor.wrapTabs": true,
  "workbench.editor.editorActionsLocation": "titleBar",
  "workbench.editorAssociations": {
    "git-rebase-todo": "gitlens.rebase"
  },

  "git-graph.dialog.merge.noFastForward": false,
  "git-graph.dialog.createBranch.checkOut": true,

  "git-log--graph.details-panel-position": "bottom",

  "gitlens.views.commitDetails.files.layout": "tree",
  "gitlens.graph.dateFormat": "YYYY-MM-DD HH:mm:ss",
  "gitlens.graph.dateStyle": "absolute",
  "gitlens.graph.avatars": false,
  "gitlens.graph.pullRequests.enabled": false,

  "periscope.peekBorderStyle": "dashed",
  "periscope.rgOptions": ["--smart-case", "--sortr path", "--no-ignore"],

  "workbench.colorCustomizations": {
    "terminal.background": "#00000000",

    "editorStickyScroll.background": "#474550" // Sticky Scroll 的背景颜色
    // "editorStickyScrollHover.background": "#1111cc" // 鼠标悬停时的背景颜色
  },
  "workbench.settings.applyToAllProfiles": ["workbench.colorCustomizations"],
  "vscode_vibrancy.theme": "Catppuccin Mocha",
  "update.mode": "manual",
  "cSpell.userWords": ["Catppuccin", "Darcula", "sortr"],
  "workbench.activityBar.location": "top",
  "workbench.layoutControl.enabled": false,

  // 关闭文件管理器的 Sticky Scroll 代码导航功能
  "workbench.tree.enableStickyScroll": false,
  "workbench.panel.showLabels": false,
  "terminal.integrated.fontSize": 18,
  "gitlens.graph.scrollMarkers.additionalTypes": [
    "stashes",
    "localBranches",
    "tags"
  ]

  // "window.commandCenter": false,
}
```

## Extensions

[GitLens](https://github.com/gitkraken/vscode-gitlens)

[无限试用 GitLens 的方案](https://zhuanlan.zhihu.com/p/675238420)

```
cmstead.js-codeformer
cmstead.jsrefactor
codeium.windsurfpyright
dbaeumer.vscode-eslint
eamodio.gitlens
esbenp.prettier-vscode
evgeniypeshkov.syntax-highlighter
formulahendry.code-runner
github.copilot
github.copilot-chat
golang.go
grapecity.gc-excelviewer
hediet.vscode-drawio
illixion.vscode-vibrancy-continued
joshmu.periscope
mads-hartmann.bash-ide-vscode
mhutchie.git-graph
mikoz.black-py
ms-azuretools.vscode-docker
ms-kubernetes-tools.vscode-kubernetes-tools
ms-python.debugpy
ms-python.python
ms-vscode.extension-test-runner
phil294.git-log--graph
redhat.vscode-yaml
ritwickdey.liveserver
streetsidesoftware.code-spell-checker
vscode-icons-team.vscode-icons
vsls-contrib.codetour
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
  // 定位到当前文件
  {
    "key": "cmd+b",
    "command": "workbench.files.action.showActiveFileInExplorer"
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

  // 打开 git diff 文件
  {
    "key": "cmd+0",
    "command": "git.openFile"
  },
  {
    "key": "cmd+0",
    "command": "git-graph.openFile"
  },
  {
    "key": "cmd+0",
    "command": "git.openFile2"
  },
  {
    "key": "cmd+0",
    "command": "-workbench.action.focusSideBar"
  },
  // 打开 git graph
  {
    "key": "cmd+9",
    "command": "git-graph.view"
  },
  // 打开 gitlens graph
  {
    "key": "alt+cmd+9",
    "command": "gitlens.showGraph"
  },
  // 打开、关闭 git blame
  {
    "key": "cmd+8",
    "command": "gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'alternate' && gitlens:activeFileStatus =~ /blameable/"
  },
  {
    "key": "alt+b",
    "command": "-gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'alternate' && gitlens:activeFileStatus =~ /blameable/"
  },
  {
    "key": "cmd+8",
    "command": "gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'chorded' && gitlens:activeFileStatus =~ /blameable/"
  },
  {
    "key": "alt+cmd+g b",
    "command": "-gitlens.toggleFileBlame",
    "when": "editorTextFocus && config.gitlens.keymap == 'chorded' && gitlens:activeFileStatus =~ /blameable/"
  },

  /* 分屏 */
  {
    "key": "alt+cmd+s alt+cmd+v",
    "command": "workbench.action.splitEditorRight"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorRight"
  },
  {
    "key": "alt+cmd+s alt+cmd+h",
    "command": "workbench.action.splitEditorDown"
  },
  {
    "key": "cmd+k cmd+\\",
    "command": "-workbench.action.splitEditorDown"
  },
  // 关闭其它
  {
    "key": "alt+cmd+s alt+cmd+o",
    "command": "workbench.action.closeOtherEditors"
  },
  {
    "key": "alt+cmd+t",
    "command": "-workbench.action.closeOtherEditors"
  },

  /* 搜索 */
  {
    "key": "cmd+f",
    "command": "periscope.search"
  },

  /* LSP 基本键 */
  // Goto Definition PS：组合 svgd 命令
  {
    "key": "cmd+g cmd+d",
    "command": "editor.action.revealDefinition",
    "when": "editorHasDefinitionProvider && editorTextFocus"
  },
  {
    "key": "f12",
    "command": "-editor.action.revealDefinition",
    "when": "editorHasDefinitionProvider && editorTextFocus"
  },
  {
    "key": "cmd+g cmd+d",
    "command": "editor.action.revealDefinition",
    "when": "editorHasDefinitionProvider && editorTextFocus && isWeb"
  },
  {
    "key": "cmd+f12",
    "command": "-editor.action.revealDefinition",
    "when": "editorHasDefinitionProvider && editorTextFocus && isWeb"
  },
  // Goto T[y]pe Definition
  {
    "key": "cmd+g cmd+y",
    "command": "editor.action.goToTypeDefinition"
  },
  // Goto Implementation
  {
    "key": "cmd+g cmd+i",
    "command": "editor.action.goToImplementation",
    "when": "editorHasImplementationProvider && editorTextFocus"
  },
  {
    "key": "cmd+f12",
    "command": "-editor.action.goToImplementation",
    "when": "editorHasImplementationProvider && editorTextFocus"
  },
  // 	References
  {
    "key": "cmd+g cmd+r",
    "command": "editor.action.goToReferences",
    "when": "editorHasReferenceProvider && editorTextFocus && !inReferenceSearchEditor && !isInEmbeddedEditor"
  },
  {
    "key": "shift+f12",
    "command": "-editor.action.goToReferences",
    "when": "editorHasReferenceProvider && editorTextFocus && !inReferenceSearchEditor && !isInEmbeddedEditor"
  },
  // Go to Prev Reference
  {
    "key": "alt+cmd+right",
    "command": "references-view.next",
    "when": "reference-list.hasResult && references-view.canNavigate"
  },
  {
    "key": "f4",
    "command": "-references-view.next",
    "when": "reference-list.hasResult && references-view.canNavigate"
  },
  // Go to Next Reference
  {
    "key": "alt+cmd+left",
    "command": "references-view.prev",
    "when": "reference-list.hasResult && references-view.canNavigate"
  },
  {
    "key": "shift+f4",
    "command": "-references-view.prev",
    "when": "reference-list.hasResult && references-view.canNavigate"
  },
  // Hover
  {
    "key": "cmd+g cmd+k",
    "command": "editor.action.showHover",
    "when": "editorTextFocus"
  },
  {
    "key": "cmd+k cmd+i",
    "command": "-editor.action.showHover",
    "when": "editorTextFocus"
  },

  // Toggle Sidebar
  {
    "key": "cmd+1",
    "command": "workbench.action.toggleSidebarVisibility"
  },
  {
    "key": "cmd+b",
    "command": "-workbench.action.toggleSidebarVisibility"
  },
  // Toggle Panel
  {
    "key": "cmd+2",
    "command": "workbench.action.togglePanel"
  },
  {
    "key": "cmd+j",
    "command": "-workbench.action.togglePanel"
  },
  // AI Chat bar
  {
    "key": "cmd+3",
    "command": "workbench.action.toggleAuxiliaryBar"
  },
  {
    "key": "alt+cmd+b",
    "command": "-workbench.action.toggleAuxiliaryBar"
  },
  // Terminal
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

  // Git pull & push
  {
    "key": "cmd+t",
    "command": "git.pull"
  },
  {
    "key": "cmd+t",
    "command": "-workbench.action.showAllSymbols"
  },
  {
    "key": "shift+cmd+k",
    "command": "git.push"
  },
  {
    "key": "shift+cmd+k",
    "command": "-editor.action.deleteLines",
    "when": "textInputFocus && !editorReadonly"
  }

  /* 标签页 */
  // {
  //   "key": "ctrl+right",
  //   "command": "workbench.action.nextEditor"
  // },
  // {
  //   "key": "alt+cmd+right",
  //   "command": "-workbench.action.nextEditor"
  // },
  // {
  //   "key": "ctrl+left",
  //   "command": "workbench.action.previousEditor"
  // },
  // {
  //   "key": "alt+cmd+left",
  //   "command": "-workbench.action.previousEditor"
  // }
]
```
