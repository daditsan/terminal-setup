*My personal terminal setup. This is the most minimalist (less distraction, more focused) and sleek looking yet still fast!</br></br>
and it also beginner friendly!* </br></br>
Tested in: 
- MacOS Sequoia
- Arch Linux.

___

<div align="center">
  <img width=150 height=150 src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/Alacritty_logo.svg/1920px-Alacritty_logo.svg.png">
  <img width=150 height=150 src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Z_Shell_Logo_Color_Vertical.svg/330px-Z_Shell_Logo_Color_Vertical.svg.png"
  <img width=150 height=150 src="https://ohmyz.sh/img/ohmyzsh-logo-ansi.png">
  <img width=150 heigth=150 src="https://raw.githubusercontent.com/romkatv/powerlevel10k-media/master/prompt-styles-high-contrast.png">
  <img width=500 height=150 src="https://raw.githubusercontent.com/tmux/tmux/master/logo/tmux-logo-medium.png">
</div>

___

# Prerequisites

## 1. **Install Alacritty**:
   Alacritty is a robust Terminal Emulator, powerful and fast!
   > You can download it from the official [Alacritty Website](https://alacritty.org/), make sure to get the latest version. Or you can also install it using your system's package manager.
## 2. **Install zsh (*if not installed*)**:
   Zsh is a Unix shell. Just like Bourne shell but with more improvement.</br>
   We need Zsh shell to use *Oh My Zsh*.</br>
   Follow instruction below based on your operating system.</br>
  - On macOS:</br>
  Zsh is pre-installed.
  You can check by running:
  ```bash
  zsh --version
  ```
  - On Debian/Ubuntu:</br>
  You can install it by running:
  ```bash
  sudo apt update
  sudo apt install zsh
  ```
  - On Arch Linux:</br>
  You can install it by running:
  ```bash
  sudo apt update
  sudo apt install zsh
  ```
## 3. Install **Oh My zsh**:
   This setup uses [Oh My Zsh](https://ohmyz.sh/) as the Zsh framework.</br>
   Oh My Zsh is a delightful, filled with helpful functions, helpers, plugins, themes.
   Install Oh My Zsh by running this command:
   ```bash
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```
## 4. **Optional but Recommended** Install **Powerlevel10k** (Zsh Theme):
   [Powerlevel10k](https://github.com/romkatv/powerlevel10k) is a theme for Zsh. It emphasizes speed, flexibility and out-of-the-box experience.</br>
   This is optional to improve UI and UX to get the best Terminal experience.</br>
   Install by running by following these steps:</br>
    - Install the [recommended font](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k). Optional but highly recommended.</br>
    - Install [Powerlevel10k](https://github.com/romkatv/powerlevel10k#installation) itself.</br>
    - Restart Zsh with `exec zsh`.</br>
    - Type `p10k configure` if the configuration wizard doesn't start automatically.</br>
## 5. Install **Tmux** (Terminal Multiplexer):
   [tmux](https://github.com/tmux/tmux/wiki) is a terminal multiplexer.</br>
   It makes switching between several programs in one terminal easily, detach and reattach them to a different terminal.</br>
   Tmux needed for splitting Terminal window as Alacritty don't support splliting window or tab-like by default.</br>
   Install by running by following the steps [here](https://github.com/tmux/tmux/wiki/Installing)</br>
# Configuring Custom Config
Here below are the custom configs for Alacritty, zsh, Oh My zsh, Powerlevel10k and Tmux.
## 1. Prequisite
Now that we have zsh. We need to set it as our default *shell*.</br>
Because most OS tend to use *bash* as the default shell.
### A. Check zhs's path 
In Alacritty or any terminal emulator. Run:
```bash
which zsh
```
It typically returns **/bin/zsh** or **/usr/bin/zsh**.
### B. Make zsh as your default shell
Run:
```
chsh -s $(which zsh)
```
> You’ll need to log out and **log back in (or reboot)** for the change **to take effect**.
>> If it doesn't work due to permissions or shell not being in /etc/shells, add it manually:
>>> Add the zsh path if it's not listed by running:
```
echo $(which zsh) | sudo tee -a /etc/shells
```
> Then run:
```
chsh -s $(which zsh)
```
### C. Launch zsh manually (to test)
Run:
```
zsh
```
## 2. Alacritty Custom Config
Now that zsh is already set as default shell.</br>
We have to customise the Alacritty to be looking sleek and clean, by editing the `alacritty.toml` file.</br>
It's usually located in `~/.config/alacritty/alacritty.toml`, if it not exits, proceed to create one.</br>
Follow these steps below.
### A. In Alacritty or any terminal. 
Run:
```
cd
```
This command is to get you to your home path or `~`</br>
### B. Create alacritty.toml
Run:
```
mkdir -p ~/.config/alacritty
```
Then create the alacritty.toml file, by running this command:
```
touch ~/.config/alacritty/alacritty.toml
```
### C. Adding Custom Config to alacritty.toml
Use *vim* or *nano*, or any text editor (if you prefer), to edit the alacritty.toml file</br>
With Vim:
```
vim ~/.config/alacritty/alacritty.toml
```
Paste this configuration:
```
# Window settings
[window]
decorations = "none"
padding = { x = 10, y = 10 }
opacity = 1.0

# Font settings
[font]
normal = { family = "JetBrainsMono Nerd Font", style = "Regular" }
size = 13.0

# Colors settings
[colors]
[colors.primary]
background = "#000000"
foreground = "#cdd6f4"

[colors.cursor]
text = "#1e1e2e"
cursor = "#cdd6f4"

[colors.selection]
text = "#1e1e2e"
background = "#cdd6f4"
```
This alacritty.toml config will make Alacritty:
- Borderless
- Remove titlebar
- Black background
- Uses JetBraunsMono Nerd Font **(Make sure you already installed JetBrainsMono Nerd Font!)**<br>
> Run `:wq` in Vim to save the file and exit vim.
## 3. Powerlevel10k Config
To improve our zsh experience, we need to custom our zsh with Powerlevel10k zsh theme.
To run Powerlevel10k custom configuration wizard, In terminal run:
```
p10k configure
```
Then follow these answers below:
### 1. Answer based on what appears
press `y` if it that symbol look like a diamond. Or `n` if it's not. If not there might be another try with different object.
### 2. Answer based of what appears
press `y` if it look like a lock icon. Or `n` if it's not. If not there might be another try with different object.
### 3. Answer based of what appears
press `y` if it look like a upwards arrow icon. Or `n` if it's not. If not there might be another try with different object.
### 4. Answer based of what appears
press `y` if it look like a upwards arrow icon. Or `n` if it's not. If not there might be another try with different object.
### 5. Answer based of what digit is pointed at
### 6. Answer based of what appears
### 7. Lean.
Answer with `1`
### 8. ASCII.
Answer with `2`
### 9. 256 colors.
Answer with `1`
### 10. Answer with your personal preference
### 11. Two lines.
Answer with `2`
### 12. Disconnected.
Answer with `1`
### 13. Compact.
Answer with `1`
### 14. Fluent.
Answer with `2
### 14. No.
Answer with `n`
### 15. Verbose.
Answer with `1`
## 4. Tmux Config
