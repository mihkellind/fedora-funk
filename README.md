# Fedora Funk
Mitä tapahtui asennuksen jälkeen - Fedora 25

**Rauta**

- HP EliteBook 2570p
- 500 GB
- 8 GB

## Powerline ja tmux

```
sudo dnf install powerline
```
Powerline oletukseksi lisämällä seuraava ~/.bashrc tiedostoon

```
if [ -f `which powerline-daemon` ]; then
  powerline-daemon -q
  POWERLINE_BASH_CONTINUATION=1
  POWERLINE_BASH_SELECT=1
  . /usr/share/powerline/bash/powerline.sh
fi
```

```
sudo dnf install tmux-powerline
```

Lisää seuraava ~/.tmux.conf tiedostoon

```
source "/usr/share/tmux/powerline.conf"
```
**Lähde:** https://fedoramagazine.org/add-power-terminal-powerline/

