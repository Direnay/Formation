# Installation Ubuntu pour pointbar

## À faire

- protonmail vpn
- nextcloud
- lanceur
- emacs vs vi - git merge
- Latex avec emojis et css
- video proj : hdmi
- signature manuscrite
- ssh-agent
- carte 4g en usb

## questions

- snap ?
- perdu le -look- de libre office ? (feature)
- ubuntu-restricted-extra ?

## Suggestions

### Whalebird

Comme client mastodon
- pntbr > eldritch.cafes

### point médian

Dans _pays et langue_ :
Passer le clavier en _français_ puis _français_
Puis alt-gr et la touche :/ produit ·

### git

`
$ git config --global core.excludesfile '~/.gitignore'  
$ git config --global core.editor 'vim'
`

### node

`
$ curl -sL https://deb.nodesource.com/setup_11.x | sudo -E bash -
$ sudo apt-get install -y nodejs

$ mkdir ~/.npm-global
$ npm config set prefix '~/.npm-global'
Open .zshrc
$ export PATH=~/.npm-global/bin:$PATH
\$ source .zshrc
`

### alias

`alias open='xdg-open'`

### Disque dur externe

`$ /media/pntbr/<disk>`

### Installation de zoom.us

- Téléchargement de l'application via logiciel ubuntu

### couper le micro avec un raccourci

- paramètres > périphériques > clavier = raccourcis clavier  
- ajouter un raccourci : +
- "toggle micro" et pointage vers un script
- maj + super + M (par exemple)

`
#!/bin/bash

 amixer set Capture toggle  | grep '\[off\]' && notify-send 'MIC OFF' || notify-send 'MIC ON'
`

### Téléphonie

`$ sudo apt install linphone`

SIP - Ovh
Téléphone : 0972141256

Login : 0033972141256
MdP: https://www.ovhtelecom.fr/manager/
Authorization user name : 0033972141256
Domain: sip5.ovh.fr

### copie écran - Kazam

Via: "logiciels ubuntu"
Pour faire des screencasts

### bluetooth

https://doc.ubuntu-fr.org/bluetooth

- périphérique "non configuré"
  `$ sudo /etc/init.d/bluetooth restart`

### dictionnaire FR

- code speller et French code speller

### Convertir markdown en PDF

Extension Visual Studio Code : vscode-pdf

https://code.visualstudio.com/Docs/languages/markdown#_markdown-preview

#### Solution à base de Visual Studio Code et pandoc

Extension :

- Github Markdown Preview
  - Markdown Preview Github Styling
  - Markdown Emoji
  - Markdown Checkboxes
  - Markdown yaml Preamble

Installation de pandoc :
`$ sudo apt install pandoc $ sudo apt install pandoc-citeproc $ sudo apt install texlive`
https://athisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/

#### Solutions avec des extensions visual studio code

### terminal

- ctrl-c ctrl-v vs maj-ctrl-c et maj -ctrl-v
- préferences : lancer une commande à la place de mon shell : zsh

#### oh-my-zsh

`$ sudo apt install zsh $ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
https://github.com/robbyrussell/oh-my-zsh

### emojis

`sudo apt install fonts-emojione`

Installation de noto-color-emoji
https://launchpad.net/~ubuntu-desktop/+archive/ubuntu/transitions/+files/fonts-noto-color-emoji_0~20170913-0ubuntu1~bionic1_all.deb

https://discourse.ubuntu.com/t/try-color-emoji-in-18-04/1492

### mail

- création d'un compte proton mail : pntbr@protonmail.fr
- installation de geary et paramètrage : stephane.langlois@scopyleft.fr via : "logiciel ubuntu"

### Pinta - retouche photo

Via: "logiciels ubuntu"

### Gnome timer

Via: "logiciels ubuntu"  
Pour avoir Montréal en têt

### Gestion des PDF

- test avec -libre-office-draw-

### VLC

Via: "logiciels ubuntu"

### visual studio share

Installation de l'extension et test entre deux machines

### Keybase

`$ curl -O https://prerelease.keybase.io/keybase_amd64.deb $ sudo apt install libgconf-2-4 $ sudo apt --fix-broken install $ sudo dpkg -i keybase_amd64.deb $ sudo apt-get install -f $ run_keybase`

Authtification par périphérique

### gitlab et github

- clé ssh

### SSH

- ssh-keygen
  http://www.linux-france.org/prj/edu/archinet/systeme/ch13s03.html

### Visual Studio Code

- Téléchargement de l'application via logiciel ubuntu :
`$ ln -s /usr/share/hunspell ~/.config/Code/Dictionaries`

### apt

- sudo apt update
- curl
- git

### slack

- Téléchargement de l'application via logiciel ubuntu
- ajout des comptes : dtc-innovation, startups-detat, pomtp, oisiflorus, la-zone-discussion,

### Installation sans histoire

- spotify
- bluetooth: libratone
- 4g: pntbr

### Firefox_dev

Téléchargement et installation dans /opt  
Création d'un fichier -desktop-
~/.local/share/applications/firefox_dev.desktop

`[Desktop Entry] Name=Firefox Developer GenericName=Firefox Developer Edition Exec=/opt/firefox_dev/firefox %u Terminal=false Icon=/opt/firefox_dev/browser/chrome/icons/default/default128.png Type=Application Categories=Application;Network;X-Developer; Comment=Firefox Developer Edition Web Browser.`

chmod +x

https://askubuntu.com/questions/548003/how-do-i-install-the-firefox-developer-edition
