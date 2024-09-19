# Install Arduino IDE

## Installation Steps

* Open Terminal
* Install dependency packages

```bash
sudo add-apt-repository universe
```

```bash
sudo apt install libfuse2
```

* Download Arduino IDE Package from <https://www.arduino.cc/en/software>

* Go to the downloaded path of the package

```bash
cd ~/<downloaded path>
```

* Extract the TAR

```bash
tar xvf <filename>
```

* Install from the package

```bash
sudo sh install.sh
```

* Add permissions to open port

```bash
sudo usermod -a -G dialout $USER
```

```bash
groups
```

```bash
ls -l /dev/ttyUSB*
```
