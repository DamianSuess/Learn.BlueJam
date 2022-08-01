# Configuring Kali Linux

1. [Get Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines)
3. Profit.

## Install VSCode

Official [Install VSCode](https://code.visualstudio.com/docs/setup/linux) on Linux guide.

```bash
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
```

Next Update package cache

```bash
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```

### Optional, Set VSCode as Default Editor

```bash
sudo update-alternatives --set editor /usr/bin/code
```

If it doesn't show up, `sudo update-alternatives --install /usr/bin/editor editor $(which code) 10`
