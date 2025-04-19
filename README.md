# 📝 Neovim Custom Keymaps

A curated set of personal key mappings for **Neovim** designed to streamline navigation, editing, and development workflows.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Keymap Overview](#keymap-overview)
- [Tips & Tricks](#tips--tricks)
- [Contributing](#contributing)
- [License](#license)

## Features

- Leader key mapped to `<Space>` for fast mnemonic shortcuts
- Seamless navigation and centered scrolling
- System clipboard integration
- Quickfix/location list navigation helpers
- Handy Go‑language snippet
- Pair‑programming with Vim‑With‑Me
- Fun extras like CellularAutomaton rain 🌧️

## Installation

1. Make sure **Neovim ≥ 0.9** is installed.
2. Copy `keymaps.lua` (or the snippet below) into your `~/.config/nvim/lua/` directory and source it from your `init.lua`:

```lua
require("keymaps")     -- adapt the path if you place the file elsewhere
```

3. Restart Neovim (or `:source ~/.config/nvim/init.lua`) and enjoy!

## Keymap Overview

| Mode          | Shortcut                       | Action                                           |
| ------------- | ------------------------------ | ------------------------------------------------ |
| **Normal**    | `<leader>pv`                   | Open netrw explorer                              |
| Normal        | `<leader>vpp`                  | Open packer config                               |
| Normal        | `<leader><leader>`             | Source current file                              |
| Normal        | `<C-d>` / `<C-u>`              | Scroll half page down/up and keep cursor centred |
| Normal        | `n` / `N`                      | Next / previous search result centred            |
| Normal        | `J`                            | Append line below without moving cursor          |
| Visual        | `J` / `K`                      | Move selection down / up                         |
| Visual        | `<leader>p`                    | Paste over selection without yanking             |
| Normal/Visual | `<leader>y`                    | Yank to system clipboard                         |
| Normal        | `<leader>Y`                    | Yank line to system clipboard                    |
| Normal/Visual | `<leader>d`                    | Delete without yanking                           |
| Insert        | `<C-c>`                        | Leave insert mode (as `<Esc>`)                   |
| Normal        | `Q`                            | Disabled (prevents accidental Ex‑mode)           |
| Normal        | `<C-f>`                        | Open tmux‑sessionizer in new tmux window         |
| Normal        | `<leader>f`                    | `vim.lsp.buf.format`                             |
| Normal        | `<C-k>` / `<C-j>`              | Next / previous Quickfix entry                   |
| Normal        | `<leader>k` / `<leader>j`      | Next / previous Location entry                   |
| Normal        | `<leader>s`                    | Search & replace current word (`:%s/.../.../gI`) |
| Normal        | `<leader>x`                    | Make current file executable (`chmod +x`)        |
| Normal        | `<leader>ee`                   | Insert Go error‑handling snippet                 |
| Normal        | `<leader>vwm` / `<leader>svwm` | Start / stop Vim-With-Me session                 |
| Normal        | `<leader>mr`                   | CellularAutomaton make\_it\_rain                 |
| Normal        | `<leader>` (`Space`)           | *Leader key*                                     |

> **Tip:** Because the leader is `<Space>`, combinations read naturally: `<Space> y` feels like “*y*ank globally”, `<Space> p` feels like “*p*aste”, etc.

## Tips & Tricks

- Use `:verbose map <lhs>` to discover where a mapping comes from.
- Pair these mappings with a plugin manager like **packer.nvim** or **lazy.nvim** for maintainability.
- Inside tmux, set `set -g focus-events on` so Neovim redraws correctly when switching panes.

## Contributing

Pull requests are welcome! Feel free to suggest new mappings, improvements, or corrections.\
Please keep the table alphabetically ordered by shortcut and update any relevant documentation.

## License

Released under the **MIT License** – see [LICENSE](LICENSE) for details.

