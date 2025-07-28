# wsl

List Available Distributions
```wsl --list --online```

Install a Specific Distribution
```wsl --install -d <DistroName>```

Check Linux version
```lsb_release -a```

Create shortcut: Windows search <DistroName> (e.g. Ubuntu), right click and pin it

Change to drive D
```cd /mnt/d```

## Installing pip for Python 3
sudo apt update && sudo apt install python3-pip && pip3 --version
sudo pip install virtualenv

## Avoid to use sudo for Python environment
https://stackoverflow.com/questions/61528500/installing-venv-for-python3-in-wsl-ubuntu<br>
in ubuntu terminal
sudo umount /mnt/d && sudo mount -t drvfs D: /mnt/d -o metadata

## Mounting a disk
https://docs.microsoft.com/en-us/windows/wsl/wsl2-mount-disk
https://www.scivision.dev/mount-usb-drives-windows-subsystem-for-linux/

## Open wsl file folders from Windows File Explorer:
\\wsl$
\\wsl$\<DistroName>\home\<UserName>\