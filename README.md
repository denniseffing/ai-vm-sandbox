# ai-vm-sandbox

## 🚀 Quickstart

```bash
# prerequisites: lima, see https://lima-vm.io/docs/installation/
./sandbox                   # create sandbox or ssh into existing sandbox
./sandbox recreate          # recreate sandbox (to apply configuration changes)
./sandbox stop              # stop sandbox
./sandbox delete            # delete sandbox
```

> ℹ️ Look at the following defaults in `ai-sandbox.yaml`and adapt them for your setup:
> 
> - Directory mounts – the default configuration expects your ZSH shell config in `~/.config/zsh` and your development > projects the agent should have access to in `~/projects`.
> - usermod usernames – they are set to my personal usernames by default

## Additional Features

### Support for pasting images (macOS only)

Coding agents inside the sandbox cannot access your macOS clipboard or local screenshot files directly. The `paste-image` script bridges that gap by uploading image clipboard content into the active SSH session and pasting the remote file path into the terminal.

**Requirements**

- iTerm2
- `pngpaste` (`brew install pngpaste`)

**iTerm2 key binding**

```text
Keyboard Shortcut: ^v (Ctrl+V)
Action: Run Coprocess
Command: /path/to/paste-image
```
