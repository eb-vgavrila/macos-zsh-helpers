# Helpers

Collection of helper functions to add to you macOS system.
* Clone this repo and navigate to it
* Deploy with the following command: `cp .helpers ~/.helpers && if [ -f ~/.zshrc ]; then grep -qF "source ~/.helpers" ~/.zshrc || (echo "source ~/.helpers"; cat ~/.zshrc) > ~/.zshrc.tmp && mv ~/.zshrc.tmp ~/.zshrc; else echo "source ~/.helpers" > ~/.zshrc; fi; source ~/.zshrc`
* Run `helpers` to see available commands
* Anytime you want to update to get new commands run `git pull` and `update_helpers`

## Features

### Auto-completion for Network Commands
The helpers automatically set up tab completion for network commands using hostnames from:
- `/etc/hosts` (excluding localhost, loopback, and broadcast addresses)
- `~/.ssh/config` (excluding wildcard entries)

**Supported commands:**
- `ssh` - Secure Shell
- `scp` - Secure Copy
- `sftp` - SSH File Transfer Protocol
- `ping` - Network connectivity test
- `rsync` - Remote sync
- `telnet` - Telnet client
- `ftp` - File Transfer Protocol

**Usage:**
Simply type any of the supported commands followed by TAB to see available hosts:
```bash
ssh <TAB>         # Shows all available hosts
scp file.txt <TAB>:  # Shows hosts for remote copy
ping <TAB>        # Shows hosts to ping
```

The completion list is automatically updated each time you source the helpers file.
