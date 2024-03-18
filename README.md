<div align="center">
     <h1> ☕ Paulo Dotfiles ☕</h1>
 </div>
 
# 🌿Sections

- ☕ [Presentations](https://github.com/paulo-barbosa2006/paulo-dotfiles/tree/main#system)
- ☕ [Galery](https://github.com/paulo-barbosa2006/paulo-dotfiles/tree/main#galery)
- ☕ [Intructions](https://github.com/paulo-barbosa2006/paulo-dotfiles/tree/main#download)
- ☕ [Informations](https://github.com/paulo-barbosa2006/paulo-dotfiles/tree/main#contact-me)

## 🌿Presentation

Don't you think a system should be visually beautiful but just as fast? Simple yet elegant setup based on the BSPWM graphics system.
This setup aims for visual elegance and fluidity.

This is mainly for my personal use but if you want to take a try feel free, i will upgrade very often.
I'm doing this for fun so for now it's pretty similar in comparison of Gh0stzk rice.

## 🌿Keys-Map

- **Alt + F1** Open the key display. This key combination can be useful to access various functions in my settings.


## 🌿System

|    Distro    |                        [Archlinux](https://github.com/archlinux)               |
| :----------: | :----------------------------------------------------------------------------: |
|      WM      |                 [BSPWM](https://github.com/baskerville/bspwm)                  |
|   Terminal   |                         [Alacritty](https://alacritty)    
|   Widgets    |            [ElKowars wacky widgets](https://github.com/elkowar/eww)            |
|     Bar      |            [Polybar](https://github.com/polybar/polybar)                       |
|    Shell     |                [zsh](https://github.com/ohmyzsh/ohmyzsh)                       |
|   Launcher   |                   [Rofi](https://github.com/davatorium/rofi)                   |
|    Editor    | [Neovim](https://github.com/neovim/neovim)-[Vs](https://code.visualstudio.com/)|
|  Compositor  |              [Picom](https://github.com/FT-Labs/picom)                         |
| File Manager |              [Thunar](https://github.com/xfce-mirror/thunar)                   |
| Notification |              [Dunst](https://github.com/dunst-project/dunst)                   |
| Theme Brow   |              [Firefox-gx](https://github.com/Godiesc/firefox-gx)               |
| Lockscreen   |     [fairyglade](https://github.com/fairyglade/ly)                             |
| Sesion UI    |   [Glorius](https://github.com/thecmdrunner/lightdm-glorious-webkit2)          |

# 🌿Galery

<details>

<summary><b><code>Karla</code></b></summary>

![demo](/assets/karla.png)

</details>

<details>

<summary><b><code>Silvia</code></b></summary>

![demo](/assets/silvia.png)

</details>

<details>

<summary><b><code>Cynthia</code></b></summary>

![demo](/assets/chynthia.png)

</details>

<details>

<summary><b><code>Cristina</code></b></summary>

![demo](/assets/cristina.png)

</details>


<details>

<summary><b><code>Aline</code></b></summary>

![demo](/assets/aline.png)

</details>


<details>

<summary><b><code>Firefox</code></b></summary>

![demo](/assets/firefox_page.png)

</details>

<details>

<summary><b><code>Spotify</code></b></summary>

![demo](/assets/spicetify.png)

</details>

<details>

<summary><b><code>Discord</code></b></summary>

![demo](/assets/discord.png)

</details>

# 🌿Installations

<details>

<summary><b><code>PipeWire</code></b></summary>
<br>
Pulseaudio tends to cause a lot of problems in the long term, so the solution I found is to use pipewire.
<br>
<pre><code>
     sudo pacman -S pipewire pipewire-alsa wireplumber pipewire-media-session pipewire-pulse
     
</pre></code>
<br>
To avoid any conflicts with Pipewire or pipewire-pulse, you should uninstall PulseAudio completely from your system. To remove pulseaudio from Arch-based systems, run:
<pre><code>
     sudo pacman -Rns pulseaudio
     
</pre></code>
<br>
To disable PulseAudio services, you can run:
<pre><code>
     systemctl --user --now disable pulseaudio.service pulseaudio.socket
     
</pre></code>
<br>
To disable PulseAudio services, you can run:
<pre><code>
    systemctl --user mask pulseaudio
     
</pre></code>
<br>
Finally enable PipeWire audio server and WirePlumber session manager
<pre><code>
     systemctl --user --now enable pipewire pipewire-pulse wireplumber
     systemctl --user --now enable pipewire pipewire-pulse pipewire-media-session
     
</pre></code>
</details>

<details>

<summary><b><code>Spotify and Spicetify</code></b></summary>
<br>
Download spotify and spicetify
<pre><code>
     sudo pacman -S spotify-launcher
     curl -fsSL https://raw.githubusercontent.com/khanhas/spicetify-cli/master/install.sh | sh
     
</pre></code>
<br>
Authorize Spicetify and modify your Spotify
<pre><code>
     sudo chmod a+wr /opt/spotify
     sudo chmod a+wr /opt/spotify/Apps -R
     
</pre></code>

<pre><code>
     cd ~/spicetify-cli
     ./spicetify backup apply enable-devtool
     
</pre></code>
<br>
Downloading new themes
<pre><code>
    git clone https://github.com/morpheusthewhite/spicetify-themes.git
    cd spicetify-themes
    cp -r * ~/.config/spicetify/Themes
     
</pre></code>
Once installed, the themes are stored in “~/.config/spicetify/Themes/”.
     
<br>
Applying the new themes
<pre><code>
     cd ~/spicetify-cli”
     ./spicetify config current_theme THEMENAME
     ./spicetify apply
     ./spicetify config color_scheme SCHEMENAME
     ./spicetify apply
     
</pre></code>

<h3>List of spicetify themes</h3>
https://spicetify.app/docs/advanced-usage/themes/

I'm currently using https://github.com/Comfy-Themes/Spicetify?tab=readme-ov-file
![demo](/assets/spicetify.png)

</details>


<details>

<summary><b><code>Discord and BetterDiscord</code></b></summary>
<br>
Nobody wants to have the experience of opening discord and being presented with the beautiful news that discord needs to be updated.
Therefore, the ideal is to install the AUR discord-arch-electron and discord-update-skip-git.
"A simple script to fix Discord wanting to update while the update isn't in the repos." - discord-update-skip-git
<br>
<pre><code>
     git clone https://aur.archlinux.org/discord_arch_electron.git
     cd discord_arch_electron
     makepkg -si
     
</pre></code>
<pre><code>
     git clone https://aur.archlinux.org/discord-update-skip-git.git
     cd discord-update-skip-git
     makepkg -si
     
</pre></code>
     
<h3>BetterDiscordctl</h3>
<pre><code>
     $ curl -O https://raw.githubusercontent.com/bb010g/betterdiscordctl/master/betterdiscordctl
     $ chmod +x betterdiscordctl
     $ sudo mv betterdiscordctl /usr/local/bin
     $ sudo betterdiscordctl self-upgrade
     
</pre></code>

<h3>BetterDiscord</h3>
Replace [COMMAND] with install to install BD for the first time, reinstall to reinstall BD after a Discord update, or uninstall to uninstall an existing installation.
<pre><code>
    $ betterdiscordctl [COMMAND]
     
</pre></code>

<h3>List of betterdiscord themes</h3>
https://betterdiscord.app/themes

I'm currently using https://github.com/refact0r/midnight-discord/blob/master/flavors/midnight-catppuccin-macchiato.theme.css
I changed the theme css. If you installed the .config that I made available, you will have access to the theme in ~/.config/BetterDiscord/themes/
![demo](/assets/discord.png)

</details>
     
## 💾Download

<div style="background-color: black; color: white; padding: 10px;">
<pre><code>
 Git/ 
 └── cd paulo-dotfiles/
      ├── cp -r config/* ~/.config/
      ├── cp -r firefox/* ~/.mozilla/firefox # More informations "about:support" only firefox
      ├── cp -r fonts/* /usr/share/fonts
      ├── cp -r icons/* /usr/share/icons
      ├── cp -r slice/* /usr/share/sddm/themes # Only sddm theme 
      ├── cp -r glorius/* /usr/share/lightdm-webkit/themes/ # Only Lighdm 
      ├── cp -r minegrub/* /boot/grub/themes/
      ├── cp -r eww/* ~/.local/bin/
      └── cp -r .zshrc/* ~/
</code></pre>
</div>

## 💾Removed

<div style="background-color: black; color: white; padding: 10px;">
<pre><code>
 delete only the git directory/ 
 └──  sudo rm -r paulo-dotfiles 

 delete everything and even the directories for the theme/
 └──  to delete everything do install but using "rm -r"  
</code></pre>
</div>

## 📦Packages

<div style="background-color: black; color: white; padding: 10px;">
<pre><code>
# use paru or your package manager (Possibly it only works in arch, if you try it in another distro let me know)
Packages/
├── BSPWM/
│   ├── Sxhkdrc
    ├── Dunst
    ├── Polybar
    ├── Eww
    ├── Feh
    ├── Picom
    ├── Firefox
├── Terminal/
│    ├── Alacritty
├── Audio/
│    ├── pipewire
     ├── pipewire-alsa
     ├── wireplumber
     ├── pipewire-media-session
     ├── pipewire-pulse
├── Menu/
│   ├── Rofi
├── AMD/
│   ├── AMDctl
    ├── Corectrl
    ├── Supergfxctl
├── Features/
    ├── Discord
    ├── Spotify
    ├── Spicetify
    ├── BetterDiscord
    ├── Tomato.c
    ├── tty-clock
    ├── cbonsai
    ├── sysfetch
    ├── neofetch
    ├── fairyglade
    ├── lightdm (Glorious)
    ├── pipes.sh
    └── Arch
</code></pre>
</div>

# 🌿Contact Me

- [Github](https://github.com/paulo-barbosa2006/)
- [Linkelind]()

## 🌿Thanks

- ☕ [Arch](https://archlinux.org/)
- ☕ [Unixporn](https://www.reddit.com/r/unixporn/)
- ☕ [Shentxt](https://github.com/Shentxt/NordicBreeze)

## 🌿Based in 

- ☕ [Gh0stzk](https://github.com/gh0stzk/dotfiles)
