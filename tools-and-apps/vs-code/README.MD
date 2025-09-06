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
    "git.allowForcePush": true,
    "flake8.args": [
        "--max-line-length=130"
    ]
```

## Extensions

### List Extensions

To list all installed extensions: ```code --list-extensions```

To create below code installation list: ```code --list-extensions | xargs -L 1 echo code --install-extension```<br>
*Note: on Windows run the command line in Git Bash terminal*<br>
[Export the Visual Studio Code extension list](https://stackoverflow.com/questions/35773299/how-can-you-export-the-visual-studio-code-extension-list)


### Install Extensions

Run following in terminal to install extensions:
```
code --install-extension ahmadalli.vscode-nginx-conf
code --install-extension almir.nginx-syntax-highlighter
code --install-extension bierner.markdown-preview-github-styles
code --install-extension charliermarsh.ruff
code --install-extension davidanson.vscode-markdownlint
code --install-extension docker.docker
code --install-extension donjayamanne.python-environment-manager
code --install-extension eamodio.gitlens
code --install-extension hediet.vscode-drawio
code --install-extension hnw.vscode-auto-open-markdown-preview
code --install-extension johnpapa.vscode-peacock
code --install-extension ms-azuretools.vscode-containers
code --install-extension ms-azuretools.vscode-docker
code --install-extension ms-python.debugpy
code --install-extension ms-python.flake8
code --install-extension ms-python.isort
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-python.vscode-python-envs
code --install-extension ms-toolsai.jupyter
code --install-extension ms-toolsai.jupyter-keymap
code --install-extension ms-toolsai.jupyter-renderers
code --install-extension ms-toolsai.vscode-jupyter-cell-tags
code --install-extension ms-toolsai.vscode-jupyter-slideshow
code --install-extension ms-vscode-remote.remote-containers
code --install-extension ms-vscode-remote.remote-ssh
code --install-extension ms-vscode-remote.remote-ssh-edit
code --install-extension ms-vscode-remote.remote-wsl
code --install-extension ms-vscode-remote.vscode-remote-extensionpack
code --install-extension ms-vscode.remote-explorer
code --install-extension ms-vscode.remote-server
code --install-extension redhat.java
code --install-extension ritwickdey.liveserver
code --install-extension secanis.jenkinsfile-support
code --install-extension shanoor.vscode-nginx
code --install-extension shd101wyy.markdown-preview-enhanced
code --install-extension techer.open-in-browser
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension visualstudioexptteam.intellicode-api-usage-examples
code --install-extension visualstudioexptteam.vscodeintellicode
code --install-extension vscjava.vscode-gradle
code --install-extension vscjava.vscode-java-debug
code --install-extension vscjava.vscode-java-dependency
code --install-extension vscjava.vscode-java-pack
code --install-extension vscjava.vscode-java-test
code --install-extension vscjava.vscode-maven
code --install-extension william-voyek.vscode-nginx
code --install-extension yy0931.save-as-root
code --install-extension yzane.markdown-pdf
code --install-extension yzhang.markdown-all-in-one
```

Install/use with care:
```
Change All End Of Line Sequence
```

### To remove all installed extensions:

Linux: ```rm -rf ~/.vscode/extensions```

Windows: ```rmdir %USERPROFILE%\.vscode\extensions /s```

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
