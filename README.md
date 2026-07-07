# 🤖 📦 ai-vm-sandbox

## 🚀 Quickstart

```bash
# prerequisites: lima, see https://lima-vm.io/docs/installation/
./sandbox                   # create sandbox or ssh into existing sandbox
./sandbox recreate          # recreate sandbox (to apply configuration changes)
./sandbox stop              # stop sandbox
./sandbox delete            # delete sandbox
```

> ℹ️ The sandbox configuration is split into a shared base and a tracked user configuration.
> 
> - Adapt the `ai-sandbox.user.yaml` config to your personal setup.
> - Adapt the `LIMA_SHELLENV_ALLOW` config in `sandbox` to pass additional environment variables into the sandbox, if needed.

### Recommendations

1. Mount your local shell configuration for a familiar shell experience. Make sure that it doesn't contain any sensitive information (e.g., credentials) beforehand.
2. Inject credentials via environment variables into the sandbox.

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
