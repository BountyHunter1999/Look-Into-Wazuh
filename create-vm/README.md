# Create VM to experiment with Wazuh

## Prerequisites

- Install Vagrant on both Windows and WSL2
- Export this to `~/.bashrc` or `~/.zshrc`

```bash
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
export VAGRANT_WSL_WINDOWS_ACCESS_USER_HOME_PATH="/mnt/c/Users/username/"
export PATH="$PATH:/mnt/c/Program Files/Oracle/VirtualBox"
```

- Install the `virtualbox_WSL2` plugin `vagrant plugin install virtualbox_WSL2`
