# Miscellany

This page stores some relatively random extra things that I install (or want to uninstall). 
It's much less thought out.

## Stuff to Install from the Ubuntu Sofware Centre

* Spotify
* Google Chrome 
* Gimp
* Skype

## Other Stuff to Install

### Dropbox

Either go [here](https://www.dropbox.com/install-linux), point and click; or

Do it from the command line:

```{bash}
cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -
~/.dropbox-dist/dropboxd
```

### Foxit PDF Reader

Go [here](https://www.foxitsoftware.com/downloads/) and download Foxit reader. 
Once downloaded double click to launch the install.

!!! warning
    I have nonstop issues at the moment with Foxit freezing on Ubuntu 19.10. 
    Switched to Okular to basix pdf viewing

### Slack

```
sudo snap install slack --classic
```

Updating Slack (sometimes they force it on you):

```{bash}
sudo apt-get update
sudo apt-get upgrade slack-desktop
```


## Uninstalling Dropbox from the Command Line

Sometimes one wants to remove Dropbox from the command line. 
Follow this recipe to remove the app:

```{bash}
dropbox stop
dropbox status  # Should report "not running"
rm -rf ~/.dropbox-dist
rm -rf /var/lib/dropbox
rm -rf ~/.dropbox*
sudo apt-get remove nautilus-dropbox
sudo apt-get remove dropbox
rm /etc/apt/source.d/dropbox
```

The above does not remove the files in your system. 
If you want to do that:

```{bash}
rm -rv ~/Dropbox
```