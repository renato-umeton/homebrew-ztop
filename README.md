# Homebrew Tap for ZTop

This is the official Homebrew tap for [ZTop](https://github.com/renato-umeton/ztop) - an all-in-one terminal system monitor for macOS.

## Installation

```bash
brew tap renato-umeton/ztop
brew install ztop
```

## What is ZTop?

ZTop is a fully automatic terminal system monitor with a 5-pane layout showing:
- CPU usage (htop)
- Memory usage (htop)
- Mac metrics (mactop)
- Container stats (ctop)
- Network traffic (nethogs)

### Features

- **Zero Configuration**: Fully automatic setup
- **Instant Warm Start**: Press `q` to detach, reattach instantly
- **Dual Commands**: Use `ztop` or `zz`
- **Oh My Zsh Plugin**: Included in installation

## Usage

After installation:

```bash
ztop  # or
zz    # shorter version
```

### Configure Passwordless Sudo (Required)

```bash
sudo visudo
# Add this line:
%admin ALL=(ALL) NOPASSWD: /opt/homebrew/bin/htop, /opt/homebrew/bin/mactop, /opt/homebrew/bin/nethogs
```

## Oh My Zsh Plugin

The Homebrew installation includes the Oh My Zsh plugin. To use it:

```bash
# Link to your Oh My Zsh plugins
ln -s /opt/homebrew/share/oh-my-zsh/custom/plugins/ztop ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/ztop

# Add to ~/.zshrc
plugins=(... ztop)

# Reload shell
source ~/.zshrc
```

## Requirements

- macOS with Homebrew
- Dependencies (auto-installed): tmux, htop, mactop, ctop, nethogs

## More Information

- **Main Repository**: https://github.com/renato-umeton/ztop
- **Latest Release**: https://github.com/renato-umeton/ztop/releases/latest
- **Issues**: https://github.com/renato-umeton/ztop/issues

## License

MIT License - See [LICENSE](https://github.com/renato-umeton/ztop/blob/main/LICENSE)
