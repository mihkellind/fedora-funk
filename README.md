# Fedora Funk
Mitä tapahtui asennuksen jälkeen - Fedora 25

**Rauta**

- HP EliteBook 2570p
- 500 GB
- 8 GB

## Powerline ja TMUX

**Powerline**

```
sudo dnf install powerline
```
Määritin Powerlinen oletukseksi lisämällä seuraavan ~/.bashrc tiedostoon

```
if [ -f `which powerline-daemon` ]; then
  powerline-daemon -q
  POWERLINE_BASH_CONTINUATION=1
  POWERLINE_BASH_SELECT=1
  . /usr/share/powerline/bash/powerline.sh
fi
```
**TMUX**

```
sudo dnf install tmux-powerline
```

Lisäsin seuraavan ~/.tmux.conf tiedostoon

```
source "/usr/share/tmux/powerline.conf"
```
**Lähde:** https://fedoramagazine.org/add-power-terminal-powerline/

Otin käyttöön valmiin asetustiedoston osoitteesta https://github.com/gpakosz/.tmux . Asensin asetustiedoston ohjeiden mukaan eikä siinä ilmennyt mitään ongelmia.

## Jekyll

Asensin Jekyll -generaattorin suorittamalla seuraavat komennot:

```
sudo dnf install ruby-devel  
sudo dnf install redhat-rpm-config
sudo gem install jekyll

sudo dnf group install "C Development Tools and Libraries"
sudo dnf install rubygems-devel
sudo dnf install nodejs
sudo gem install bundler
```

**Lähde:** http://linuxsuperuser.com/install-jekyll-on-fedora-23/

## Gulp

```
sudo npm install --global gulp-cli
```
Komentotulkki ilmoitti, että Gulp asentui hakemistoon
```/usr/lib/node_modules/gulp-cli/bin/gulp.js```
