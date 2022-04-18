# Linux

A guideline for my Linux configuration

# Kitty Terminal

---

[kitty.conf](Linux%2045edd/kitty.conf)

## Usage

---

The commands that I use most of the time

```markdown
Ctrl+Shift+Enter - New layout
Ctrl+Shift+{ or } - Cycling between layouts
Ctrl+Shift+W - Closing the layout
Ctrl+Shfit+F or B - Moving the layout forward or backwards
Ctrl+Shift+L or M - Increase or Decrease Background opacity
```

Comand to install Kitty theme

```bash
cp theme.conf ~/.config/kitty/
echo "include theme.conf" >> ~/.config/kitty/kitty.conf
```

# Gnome Extensions

---

If for some reason i decide to use Gnome again, here is a short but useful gnome extension list that i use

I could try to learn how to use gnome-shell-extensions sync but i’m too lazy so i’ll list everything.

### Burn My Windows

- simple but elegant animations when opening/closing windows

[GitHub - Schneegans/Burn-My-Windows: 🔥 Disintegrate your windows with style.](https://github.com/Schneegans/Burn-My-Windows)

### Impatience

- speeds up animations

[Impatience - GNOME Shell Extensions](https://extensions.gnome.org/extension/277/impatience/)

### No overview at start-up

- does what the title says

[GitHub - fthx/no-overview](https://github.com/fthx/no-overview)

### Remove Alt+Tab Delay v2

- fixes annoying delay

[](https://github.com/BjoernDaase/remove-alt-tab-delay)

### Extension List

- shows extensions in shell

[GitHub - tuberry/extension-list: Simple GNOME Shell extension manager in the top panel.](https://github.com/tuberry/extension-list)

### Arch Linux Updates Indicator

- shows if i have an update

[GitHub - RaphaelRochet/arch-update: Update indicator for ArchLinux and Gnome-Shell](https://github.com/RaphaelRochet/arch-update)

# Oh my Zsh

- Installation:

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

- ZSH configuration commands:

```bash
zplug "dracula/zsh",as:theme
plugins=(
          git 
          zsh-autosuggestions)

source $ZSH/oh-my-zsh.sh
# Example aliases
alias kittyconfig="nvim ~/.config/kitty/kitty.conf"
alias zshconfig="nvim ~/.zshrc"
alias ohmyzsh="nvim ~/.oh-my-zsh"
alias c="clear"
alias update="sudo pacman -Syu"
alias open="nautilus"
alias ls="lsd"
alias e="exit"
alias restart="exec terminator"
alias fish="asciiquarium"
alias norm="wmctrl -r :ACTIVE: -e 0,-1,-1,800,800"
alias fat="wmctrl -r :ACTIVE: -e 0,-1,-1,1200,850"
alias slim="wmctrl -r :ACTIVE: -e 0,-1,-1,650,800"
alias mid="wmctrl -r :ACTIVE: -e 0,550,100,-1,-1"
alias right="wmctrl -r :ACTIVE: -e 0,1200,100,-1,-1"
alias left="wmctrl -r :ACTIVE: -e 0,100,100,-1,-1"
alias untar="tar xvf"
```

## Powerlevel10k

- Installation :

```bash
yay -S --noconfirm zsh-theme-powerlevel10k-git
echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
p10k configure
```
