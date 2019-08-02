---
layout: post
tag: [nodejs, npm, install, installation, peerflix, mpv]
---
## Node (LTS version)
```
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
sudo apt-get install -y nodejs
```

[source](https://websiteforstudents.com/install-the-latest-node-js-and-nmp-packages-on-ubuntu-16-04-18-04-lts/)


# Peerflix

```
sudo npm install -g peerflix
```

## Usage
```
peerflix "Lien torrent ou Magnet" --mpv
```

[source](http://www.webupd8.org/2014/03/peerflix-stream-torrents-with-vlc-or.html)

# mpv (latest)
```
sudo add-apt-repository ppa:mc3man/mpv-tests
sudo apt update
sudo apt install mpv
```

[source](https://mpv.io/)
