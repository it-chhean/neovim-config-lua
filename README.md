A modern Neovim configuration powered by Lazy.nvim for Java and general development.

Create Neovim Config Folder

```bash
mkdir -p ~/.config/nvim
```

Move into the directory:

```bash
cd ~/.config/nvim
```

Create init.lua

```bash
touch init.lua
```

Open the file:

```bash
nvim init.lua
```

Paste your Neovim configuration into `init.lua`.

Save the file:

```vim
:w
```

Exit:

```vim
:q
```
 
Start Neovim

```bash
nvim
```

Lazy.nvim will automatically install all plugins. Wait until the installation finishes before proceeding.

 

Install Java JDTLS

Create the JDTLS directory:

```bash
mkdir -p ~/.local/share/jdtls
```

Move into the directory:

```bash
cd ~/.local/share/jdtls
```

Download JDTLS:

```bash
wget https://download.eclipse.org/jdtls/snapshots/jdt-language-server-latest.tar.gz
```

Extract the archive:

```bash
tar -xvf jdt-language-server-latest.tar.gz
```

Expected folder structure:

```
~/.local/share/jdtls/
├── config_linux
├── plugins
└── features
```

Start a Java Project

Create a new project directory:

```bash
mkdir demo-project
cd demo-project
```

Open it with Neovim:

```bash
nvim .
```

JDTLS will automatically start when a valid Java project is detected.

 

Keymaps

| Key            | Action                |
|     -|       --|
| `jk`           | Exit insert mode      |
| `<leader>w`    | Save file             |
| `<leader>q`    | Quit                  |
| `<leader>h`    | Clear search highlight|
| `<leader>e`    | Toggle file explorer  |

Telescope

| Key            | Action       |
|     -|    --|
| `<leader>ff`   | Find files   |
| `<leader>fg`   | Live grep    |
| `<leader>fb`   | Buffers      |
| `<leader>fh`   | Help tags    |
| `<leader>fr`   | Recent files |


Plugins

| Plugin            | Purpose               |
|      -|       --|
| lazy.nvim         | Plugin manager        |
| nvim-lspconfig    | LSP configuration     |
| nvim-jdtls        | Java language server  |
| nvim-cmp          | Autocompletion engine |
| LuaSnip           | Snippet support       |
| telescope.nvim    | Fuzzy finder          |
| nvim-tree.lua     | File explorer         |
| smear-cursor.nvim | Cursor animation      |

Telescope FZF Not Working

Build the extension manually:

```bash
cd ~/.local/share/nvim/lazy/telescope-fzf-native.nvim
make
```

Folder Structure

Current structure:

```
~/.config/nvim/
└── init.lua
```
