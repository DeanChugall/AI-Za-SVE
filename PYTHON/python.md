# Build, compile and install Python from source code on Linux *(Ubuntu-Debian)

> [REFERENCE TO GENERATE CODE FOR INSTALLATION](https://www.build-python-from-source.com/)

- ✓ Compile, build and install Python 2.7 or 3.x binaries from source code
- ✓ Use the generated copy & paste bash script
- ✓ Don’t worry, the shipped Python in your Linux box is going to keep untouched


## Python 3.11.1
```bash
cd /tmp/
wget https://www.python.org/ftp/python/3.11.1/Python-3.11.1.tgz
tar xzf Python-3.11.1.tgz
cd Python-3.11.1

sudo ./configure --prefix=/opt/python/3.11.1/ --enable-optimizations --with-lto --with-computed-gotos --with-system-ffi --enable-shared
sudo make -j "$(nproc)"
sudo make altinstall
sudo rm /tmp/Python-3.11.1.tgz
```


## Python 3.10.9
```bash
cd /tmp/
wget https://www.python.org/ftp/python/3.10.9/Python-3.10.9.tgz
tar xzf Python-3.10.9.tgz
cd Python-3.10.9

sudo ./configure --prefix=/opt/python/3.10.9/ --enable-optimizations --with-lto --with-computed-gotos --with-system-ffi
sudo make -j "$(nproc)"
sudo make altinstall
sudo rm /tmp/Python-3.10.9.tgz
```