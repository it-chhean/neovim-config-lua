# 🚀 Neovim Java Development Setup

A modern Neovim configuration powered by Lazy.nvim for Java and general development.

---

# ✨ Features

- ☕ Java development using JDTLS
- ⚡ Fast plugin management with Lazy.nvim
- 🔍 Telescope fuzzy finder
- 📁 NvimTree file explorer
- 🧠 IntelliSense-like autocompletion
- 🎨 Transparent UI
- ✨ Smear cursor animation
- 📦 Lombok support
- 🔄 Auto organize imports
- ⌨️ VSCode-like workflow

---

# 📦 Requirements

Install these packages first.

## Ubuntu / Debian

```bash
sudo apt update

sudo apt install neovim git openjdk-17-jdk maven unzip curl build-essential wget
```

---

# 📁 Create Neovim Config Folder

```bash
mkdir -p ~/.config/nvim
```

Move into directory:

```bash
cd ~/.config/nvim
```

---

# 📝 Create init.lua

```bash
touch init.lua
```

Open file:

```bash
nvim init.lua
```

Paste your Neovim configuration into `init.lua`.

Save file:

```vim
:w
```

Exit:

```vim
:q
```

---

# ⚡ Start Neovim

```bash
nvim
```

Lazy.nvim will automatically install plugins.

Wait until installation finishes.

---

# ☕ Install Java JDTLS

Create JDTLS directory:

```bash
mkdir -p ~/.local/share/jdtls
```

Move into directory:

```bash
cd ~/.local/share/jdtls
```

Download JDTLS:

```bash
wget https://download.eclipse.org/jdtls/snapshots/jdt-language-server-latest.tar.gz
```

Extract archive:

```bash
tar -xvf jdt-language-server-latest.tar.gz
```

Folder structure:

```bash
~/.local/share/jdtls/
├── config_linux
├── plugins
└── features
```

---

# 🔤 Install Nerd Font

Recommended fonts:

- JetBrainsMono Nerd Font
- Cascadia Code Nerd Font

After installation:

1. Open terminal settings
2. Change terminal font
3. Select Nerd Font

---

# 📦 Lombok Support (Optional)

Lombok is automatically detected from Maven repository.

Add dependency to your Java project:

```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <version>latest</version>
</dependency>
```

---

# 🚀 Start Java Project

Create project:

```bash
mkdir demo-project

cd demo-project
```

Open with Neovim:

```bash
nvim .
```

JDTLS will automatically start.

---

# ⌨️ Keymaps

## General

| Key | Action |
|---|---|
| `jk` | Exit insert mode |
| `<leader>w` | Save file |
| `<leader>q` | Quit |
| `<leader>h` | Clear search |
| `<leader>e` | Toggle file explorer |

---

## Telescope

| Key | Action |
|---|---|
| `<leader>ff` | Find files |
| `<leader>fg` | Live grep |
| `<leader>fb` | Buffers |
| `<leader>fh` | Help tags |
| `<leader>fr` | Recent files |

---

## Java JDTLS

| Key | Action |
|---|---|
| `<leader>oi` | Organize imports |
| `<leader>ev` | Extract variable |
| `<leader>ec` | Extract constant |
| `<leader>tm` | Test nearest method |

---

# 🔌 Plugins

- lazy.nvim
- nvim-lspconfig
- nvim-jdtls
- nvim-cmp
- LuaSnip
- telescope.nvim
- nvim-tree.lua
- smear-cursor.nvim

---

# 🖥️ Recommended Terminal

- Kitty
- WezTerm
- Alacritty

Enable transparency for best experience.

---

# 🛠️ Troubleshooting

## JDTLS Not Starting

Check Java version:

```bash
java --version
```

Make sure:

- JDK 17+ installed
- `config_linux` exists
- Project contains:
  - `.git`
  - `pom.xml`
  - `gradlew`
  - `mvnw`

---

## Telescope FZF Not Working

Build extension manually:

```bash
cd ~/.local/share/nvim/lazy/telescope-fzf-native.nvim

make
```

---

# 📁 Folder Structure

```bash
~/.config/nvim/
└── init.lua
```

Future structure:

```bash
lua/
├── config/
├── plugins/
├── lsp/
├── keymaps/
└── settings/
```

---

# 📜 License

MIT
