# VS Code

## Settings

### User settings

[shift][ctrl][p] Preferences: Open Settings (JSON)
```
    "files.autoSave": "afterDelay",
    "editor.rulers": [
        130
    ],
    "workbench.tree.indent": 24,
    "git.allowForcePush": true
```

## Plugins

```
Code Spell Checker, v2.2.5
markdownlint, v0.47.0
Pylance
GitLens
pylens
Auto-Open Markdown Preview
Change All End Of Line Sequence
```

## Windows - Git Bash terminal

[shift][ctrl][p] Select Default Profile >> Terminal: Select Default Profile >> Git Bash

## WSL

### Open project in WSL

Open folder
Shift+Ctrl+P ```WSL:Reopen Folder in WSL```

## Links

[ArjanCodes YT - COMPLETE No-Nonsense VSCode Setup for Python Devs](https://www.youtube.com/watch?v=PwGKhvqJCQM)

## OLD NOTES

In powershell terminal:<br>
```Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted```

ERROR: pip is configured with locations that require TLS/SSL, however the ssl module in Python is not available<br>
https://stackoverflow.com/questions/45954528/pip-is-configured-with-locations-that-require-tls-ssl-however-the-ssl-module-in<br>
I copy the following files from C:\Users\MyUser\Miniconda3\Library\bin to C:\Users\MyUser\Miniconda3\DLLs:<br>
libcrypto-1_1-x64.dll<br>
libcrypto-1_1-x64.pdb<br>
libssl-1_1-x64.dll<br>
libssl-1_1-x64.pdb<br>

### User settings - conda
[shift][ctrl][p] Preferences: Open Settings (JSON)
```
	### Disable conda activate
	"python.terminal.activateEnvironment": false
```

### WSL / .venv
    https://docs.microsoft.com/en-us/windows/python/web-frameworks
        
    https://stackoverflow.com/questions/61528500/installing-venv-for-python3-in-wsl-ubuntu
    sudo pip install virtualenv
    mkdir .venv
    virtualenv -p python3 .venv
    source .venv/bin/activate
    deactivate

    If no python found for windows then try with:
    py -m venv .venv

### From Blum, Troels 
If you like your bash shell to work in vscode: set allowChords: false 
https://code.visualstudio.com/docs/editor/integrated-terminal#_chord-keybindings-in-the-terminal  
