# just

## Installation

### Windows

Download Windows release from: [Releases (github)](https://github.com/casey/just/releases)
*(Windows 64 bit: just-x.x.x-x86_64-pc-windows-msvc.zip)*

Extract **just.exe** from the zip file<br>
Move just.exe to **C:\Program Files\Just** folder<br>

Add the path with PowerShell<br>
```[Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\Program Files\Just", "User")```<br>
[Adding path With Windows GUI](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10)

To run just in PowerShell, it reuires following in the top of the justfile<br>
```set shell := ["powershell.exe", "-NoProfile", "-Command"]```<br>
*It's recomended to run just in Git Bash terminsal to use same justfile in Windows and Linux*

### Linux

Ubuntu 24.04 ```sudo apt update && sudo apt install just```

## Links
[README (github)](https://github.com/casey/just)

[Just Programmer's Manual](https://just.systems/man/en/)