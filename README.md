# nodev

Lightweight nvm alternative

## Install

Clone the repo and put the `nodev` executable in your `PATH`.

```bash
git clone https://github.com/peterszarvas94/nodev.git
cd nodev
chmod +x nodev
sudo cp nodev /usr/local/bin/
```

Add `$HOME/.nodev/current` to your `PATH` in your shell profile:

**Bash:**

```bash
echo 'export PATH="$HOME/.nodev/current:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

**Zsh:**

```bash
echo 'export PATH="$HOME/.nodev/current:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

**Fish:**

```fish
echo 'set -gx PATH $HOME/.nodev/current $PATH' >> ~/.config/fish/config.fish
source ~/.config/fish/config.fish
```

## Usage

### Install a Node.js version

```bash
nodev install 18.17.0
nodev install v20.8.0
```

### Use a specific version

```bash
nodev use 18.17.0
```

### List installed versions

```bash
nodev list
```

### Show current version

```bash
nodev current
```

### Remove a version

```bash
nodev remove 18.17.0
```

## Supported Platforms

- macOS
- Linux
- Windows WLS

## How it works

- Automatically detects your OS and architecture
- Downloads Node.js binaries from the official distribution
- Stores versions in `$HOME/.nodev/versions/`
- Creates symlinks in `$HOME/.nodev/current/` for the active version

The code in this repo was created with the help of AI models.
