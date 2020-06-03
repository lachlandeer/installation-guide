## Web Scraping Using an Automated Browser

Install Google Chrome for Debian/Ubuntu by pasting the following and then pressing Return

```{bash}
sudo apt-get install libxss1 libappindicator1 libindicator7
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome*.deb
sudo apt-get install -f
```

Install xvfb so chrome can run 'headless' by pasting the following and then pressing Return

```{bash}
sudo apt-get install xvfb
```

Install Chromedriver by pasting the following and then pressing Return (do check for the latest version and that it matches the version of chrome you have installed on your machine):

```{bash}
sudo apt-get install unzip 
wget -N https://chromedriver.storage.googleapis.com/78.0.3904.105/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
chmod +x chromedriver

sudo mv -f chromedriver /usr/local/share/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/local/bin/chromedriver
sudo ln -s /usr/local/share/chromedriver /usr/bin/chromedriver
```

If your install worked, you should get ChromeDriver 7X.0.XXXX.XXX returned if the installation was successful - where the version must match the version of Chrome you have installed.

```{bash}
chromedriver --version
```