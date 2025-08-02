# uv

## Installation

### Windows:
```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```
### Linux:
```
curl -LsSf https://astral.sh/uv/install.sh | sudo sh
```
If it was installed for root user
```
curl -LsSf https://astral.sh/uv/install.sh | sudo sh
downloading uv 0.8.3 x86_64-unknown-linux-gnu
no checksums to verify
installing to /root/.local/bin
  uv
  uvx
everything's installed!
```
then ```sudo mv /root/.local/bin/uv /usr/local/bin/```

### Raspberry Pi

[Install uv with Snap](https://snapcraft.io/install/astral-uv/raspbian)

## Use

New project: ```uv init <project-name>```

Change python version in **.python-version** file<br>
Update python: ```uv sync```<br>
Update project python version: ```uv pip install -e . --link-mode=copy```<br>
*(--link-mode=copy to avoid Windows error)*

Run: ```uv run <python-file>```<br>

## Links
[Tutorial](https://www.datacamp.com/tutorial/python-uv)
