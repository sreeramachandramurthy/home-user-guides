# Android SDK

## Instation Steps

* Open Terminal
* Install ADB

```bash
sudo apt install android-tools-adb
```

* Install Android SDK

```bash
sudo apt install android-sdk android-sdk-helper
```

* Install Android Command Line Tools

```bash
cd ~/Documents
mkdir sdk
wget https://dl.google.com/android/repository/tools_r25.2.3-linux.zip
unzip tools_r25.2.3-linux.zip -d /sdk
cd sdk/tools
./android update sdk
```

* Install necessary SDK's

* Close and re-open Terminal
* Add new directories to the PATH

```bash
export ANDROID_HOME=$HOME/Documents/sdk
export PATH=${PATH}:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools:$ANDROID_HOME/build-tools/29.0.3/
```
