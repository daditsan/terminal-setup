*My personal Terminal Setup for mostly every purpose. This is the most minimalist (less distraction, more focused) and sleek looking yet still fast!</br></br>
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
