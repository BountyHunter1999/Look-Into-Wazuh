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



## Debugging


### `java.lang.IllegalArgumentException: Values less than -1 bytes are not supported: -22388736b`
- If you get an error like this view `/var/log/wazuh-indexer/wazuh.log`

- `sudo vim /etc/wazuh-indexer/jvm.options` Add `--enable-native-access=ALL-UNNAMED`
- `sudo vim /etc/wazuh-indexer/opensearch.yml` Add `opensearch.security.allow_generic_native_transport_client_auth_enabled: true`