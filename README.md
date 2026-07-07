# ai-vm-sandbox

## 🚀 Quickstart

```bash
# prerequisites: lima, see https://lima-vm.io/docs/installation/
./sandbox                   # create sandbox or ssh into existing sandbox
./sandbox recreate          # recreate sandbox (to apply configuration changes)
./sandbox stop              # stop sandbox
./sandbox delete            # delete sandbox
```

> ℹ️ The sandbox configuration is split into a shared base and a tracked user configuration.
> Adapt the user configuration in `ai-sandbox.user.yaml` to your personal setup.

## ✨ Additional Features

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
