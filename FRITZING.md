


* [Web Fritzing](https://fritzing.org/)
* [History Changes](https://fritzing.org/download/history-changes/)
* [Download](https://fritzing.org/download/)
![Picture](/images/05.png)


# Install Linux (Ubuntu 20.02)

Install dependences:
```console
sudo apt install libqt5printsupport5 libqt5xml5 libqt5sql5 libqt5serialport5 libqt5sql5-sqlite
```

```console
mkdir ~/fritzing
cp fritzing-0.9.6.linux.AMD64.tar.bz2 ~/fritzing/
cd ~/fritzing/
tar -xvjf fritzing-0.9.6.linux.AMD64.tar.bz2
cd fritzing-0.9.6.linux.AMD64/
./install_fritzing.sh
```

![Picture](/images/06.png)

![Picture](/images/07.png)


The Program is installed into _~/.local/share/fritzing_


# Install on Ubuntu 16.04 - 18.04
[Reference](https://askubuntu.com/questions/1126893/how-to-install-openssl-1-1-1-and-libssl-package)


[Download openssl-1.1.XX](https://www.openssl.org/source/)

Compile and Install:
```console
sudo mkdir /opt/openssl
sudo tar xfvz ~/Downloads/openssl-1.1.1k.tar.gz --directory /opt/openssl
export LD_LIBRARY_PATH=/opt/openssl/lib
cd /opt/openssl/openssl-1.1.1k/
sudo ./config --prefix=/opt/openssl --openssldir=/opt/openssl/ssl
sudo make
sudo make test #Optional
sudo make install
sudo updatedb  #rebuild cache
#executable is in: /opt/openssl/bin/openssl
```

Add to Path:
```console
sudo touch /etc/profile.d/openssl.sh
sudo vi /etc/profile.d/openssl.sh
```
Add this text:
```console
#!/bin/sh
export PATH=/opt/openssl/bin:${PATH}
export LD_LIBRARY_PATH=/opt/openssl/lib:${LD_LIBRARY_PATH}
```

```console
sudo chmod +x /etc/profile.d/openssl.sh
source /etc/profile.d/openssl.sh
```

Test:
```console
which openssl
openssl version
openssl version
```

### Create custom Part
[creating-custom-parts](https://fritzing.org/learning/tutorials/creating-custom-parts)


