## User Settings

```json
{
    "workbench.colorTheme": "Tokyo Night",
    
    "editor.fontFamily": "Monaco, Menlo, 'Courier New', monospace",
    "editor.fontSize": 18,

    "git.enableSmartCommit": true,
    
    "files.autoSave": "afterDelay",

    "windsurf.autocompleteSpeed": "fast",
    "windsurf.enableSupercomplete": false,
    "windsurf.enableAutocomplete": false,
    
    "gitlens.views.commitDetails.files.layout": "tree",
    "gitlens.ai.model": "openai:o1-preview",
    "gitlens.graph.minimap.enabled": false
}
```

## Extensions

```
eamodio.gitlens
esbenp.prettier-vscode
golang.go
ritwickdey.liveserver
vue.volar
```

导出所有插件：`code --list-extensions > extensions.txt`

安装所有插件：`cat extensions.txt | xargs -L 1 code --install-extension`

## Keyboard Shortcuts

```json
[
    {
        "key": "cmd+2",
        "command": "workbench.view.extension.gitlensPanel"
    },
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
        "key": "ctrl+shift+g",
        "command": "-workbench.view.scm",
        "when": "workbench.scm.active"
    }
]
```