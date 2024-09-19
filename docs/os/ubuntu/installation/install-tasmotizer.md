 ~ ▓▒░ pip3 install --upgrade wheel                                                                        ░▒▓ ✔ 
Defaulting to user installation because normal site-packages is not writeable
Requirement already satisfied: wheel in /usr/lib/python3/dist-packages (0.37.1)
Collecting wheel
  Downloading wheel-0.42.0-py3-none-any.whl (65 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 65.4/65.4 kB 353.3 kB/s eta 0:00:00
Installing collected packages: wheel
  WARNING: The script wheel is installed in '/home/ram/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed wheel-0.42.0

[notice] A new release of pip is available: 23.0.1 -> 23.3.2
[notice] To update, run: python3 -m pip install --upgrade pip
 ~ ▓▒░ python3 -m pip install --upgrade pip                                                           ░▒▓ ✔  22s 
Defaulting to user installation because normal site-packages is not writeable
Requirement already satisfied: pip in /usr/local/lib/python3.10/dist-packages (23.0.1)
Collecting pip
  Downloading pip-23.3.2-py3-none-any.whl (2.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.1/2.1 MB 4.8 MB/s eta 0:00:00
Installing collected packages: pip
  WARNING: The scripts pip, pip3 and pip3.10 are installed in '/home/ram/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed pip-23.3.2

[notice] A new release of pip is available: 23.0.1 -> 23.3.2
[notice] To update, run: python3 -m pip install --upgrade pip
 ~ ▓▒░ pip --version                                                                                  ░▒▓ ✔  10s 
pip 23.3.2 from /home/ram/.local/lib/python3.10/site-packages/pip (python 3.10)
 ~ ▓▒░ pip3 install tasmotizer                                                                             ░▒▓ ✔ 
Defaulting to user installation because normal site-packages is not writeable
Collecting tasmotizer
  Downloading tasmotizer-1.2.1-py3-none-any.whl (196 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 196.8/196.8 kB 189.8 kB/s eta 0:00:00
Collecting pyserial>=3.0 (from tasmotizer)
  Downloading pyserial-3.5-py2.py3-none-any.whl (90 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 90.6/90.6 kB 254.2 kB/s eta 0:00:00
Requirement already satisfied: PyQt5>=5.10 in /usr/lib/python3/dist-packages (from tasmotizer) (5.15.6)
Requirement already satisfied: PyQt5-sip<13,>=12.8 in /usr/lib/python3/dist-packages (from PyQt5>=5.10->tasmotizer) (12.9.1)
Installing collected packages: pyserial, tasmotizer
  WARNING: The scripts pyserial-miniterm and pyserial-ports are installed in '/home/ram/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed pyserial-3.5 tasmotizer-1.2.1
 ~ ▓▒░ tasmotizer.py                                                                                   ░▒▓ ✔  8s 
zsh: command not found: tasmotizer.py
 ~ ▓▒░ python3 -m tasmotizer.py                                                                        ░▒▓ 127 х 
Traceback (most recent call last):
  File "/usr/lib/python3.10/runpy.py", line 187, in _run_module_as_main
    mod_name, mod_spec, code = _get_module_details(mod_name, _Error)
  File "/usr/lib/python3.10/runpy.py", line 110, in _get_module_details
    __import__(pkg_name)
  File "/home/ram/.local/lib/python3.10/site-packages/tasmotizer.py", line 16, in <module>
    from PyQt5.QtSerialPort import QSerialPortInfo, QSerialPort
ModuleNotFoundError: No module named 'PyQt5.QtSerialPort'
 ~ ▓▒░ sudo apt-get install python3-pyqt5.qtserialport                                               ░▒▓ 1 х  5s 
[sudo] password for ram: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libcommon-sense-perl libjson-perl libjson-xs-perl libtext-csv-perl libtext-csv-xs-perl
  libtypes-serialiser-perl
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  libqt5serialport5
The following NEW packages will be installed:
  libqt5serialport5 python3-pyqt5.qtserialport
0 upgraded, 2 newly installed, 0 to remove and 4 not upgraded.
Need to get 64.2 kB of archives.
After this operation, 266 kB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://in.archive.ubuntu.com/ubuntu jammy/universe amd64 libqt5serialport5 amd64 5.15.3-1 [34.6 kB]
Get:2 http://in.archive.ubuntu.com/ubuntu jammy/universe amd64 python3-pyqt5.qtserialport amd64 5.15.6+dfsg-1ubuntu3 [29.6 kB]
Fetched 64.2 kB in 11s (5,882 B/s)                   
Selecting previously unselected package libqt5serialport5:amd64.
(Reading database ... 330941 files and directories currently installed.)
Preparing to unpack .../libqt5serialport5_5.15.3-1_amd64.deb ...
Unpacking libqt5serialport5:amd64 (5.15.3-1) ...
Selecting previously unselected package python3-pyqt5.qtserialport.
Preparing to unpack .../python3-pyqt5.qtserialport_5.15.6+dfsg-1ubuntu3_amd64.deb ...
Unpacking python3-pyqt5.qtserialport (5.15.6+dfsg-1ubuntu3) ...
Setting up libqt5serialport5:amd64 (5.15.3-1) ...
Setting up python3-pyqt5.qtserialport (5.15.6+dfsg-1ubuntu3) ...
Processing triggers for libc-bin (2.35-0ubuntu3.6) ...
 ~ ▓▒░ python3 -m tasmotizer.py                                                                    ░▒▓ ✔  1m 31s 
/usr/bin/python3: Error while finding module specification for 'tasmotizer.py' (ModuleNotFoundError: __path__ attribute not found on 'tasmotizer' while trying to find 'tasmotizer.py'). Try using 'tasmotizer' instead of 'tasmotizer.py' as the module name.
 ~ ▓▒░ python3 -m tasmotizer                                                                             ░▒▓ 1 х 
Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
 ~ ▓▒░ python3 -m tasmotizer                                                                       ░▒▓ ✔  1m 10s 
Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
esptool.py v2.8
Serial port /dev/ttyUSB0
 ~ ▓▒░ sudo python3 -m tasmotizer                                                                     ░▒▓ ✔  60s 
[sudo] password for ram: 
/usr/bin/python3: No module named tasmotizer
 ~ ▓▒░ sudo pip3 install tasmotizer                                                                  ░▒▓ 1 х  6s 
Collecting tasmotizer
  Downloading tasmotizer-1.2.1-py3-none-any.whl (196 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 196.8/196.8 kB 1.1 MB/s eta 0:00:00
Collecting pyserial>=3.0
  Downloading pyserial-3.5-py2.py3-none-any.whl (90 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 90.6/90.6 kB 532.5 kB/s eta 0:00:00
Requirement already satisfied: PyQt5>=5.10 in /usr/lib/python3/dist-packages (from tasmotizer) (5.15.6)
Requirement already satisfied: PyQt5-sip<13,>=12.8 in /usr/lib/python3/dist-packages (from PyQt5>=5.10->tasmotizer) (12.9.1)
Installing collected packages: pyserial, tasmotizer
Successfully installed pyserial-3.5 tasmotizer-1.2.1
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv

[notice] A new release of pip is available: 23.0.1 -> 23.3.2
[notice] To update, run: python3 -m pip install --upgrade pip
 ~ ▓▒░ sudo python3 -m tasmotizer                                                                     ░▒▓ ✔  43s 
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting....
Chip is ESP8266EX
Features: WiFi
Crystal is 26MHz
Uploading stub...
Running stub...
Stub running...
Read 1048576 bytes at 0x0 in 98.6 seconds (85.1 kbit/s)...
Hard resetting via RTS pin...
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting........_____....._____....._____....._____....._____....._____....._____
QIODevice::write (QSerialPort): device not open
qt.xkb.compose: failed to create compose table
 ~ ▓▒░ sudo python3 -m tasmotizer                                                                  ░▒▓ ✔  16m 4s 
[sudo] password for ram: 
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting....
Chip is ESP8266EX
Features: WiFi
Crystal is 26MHz
Uploading stub...
Running stub...
Stub running...
Read 1048576 bytes at 0x0 in 98.6 seconds (85.1 kbit/s)...
Hard resetting via RTS pin...
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting........_____....._____....._____....._____....._____....._____....._____
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting........_____....._____....._____....._____....._____....._____....._____
QIODevice::write (QSerialPort): device not open
esptool.py v2.8
Serial port /dev/ttyUSB0
esptool.py v2.8
Serial port /dev/ttyUSB1
Connecting........_____....._____....._____....._____....._____....._____....._____
esptool.py v2.8
Serial port /dev/ttyUSB1
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting........_____....._____....._____....._____....._____....._____....._____
esptool.py v2.8
Serial port /dev/ttyUSB1
Connecting........_____....._____....._____....._____....._____....._____....._____
esptool.py v2.8
Serial port /dev/ttyUSB0
Connecting....
Chip is ESP8266EX
Features: WiFi
Crystal is 26MHz
Uploading stub...
Running stub...
Stub running...
Configuring flash size...
Auto-detected Flash size: 1MB
Erasing flash (this may take a while)...
Chip erase completed successfully in 0.0s
Compressed 652928 bytes to 466263...
Wrote 652928 bytes (466263 compressed) at 0x00000000 in 49.2 seconds (effective 106.2 kbit/s)...
Hash of data verified.

Leaving...
Hard resetting via RTS pin...
QIODevice::write (QSerialPort): device not open
