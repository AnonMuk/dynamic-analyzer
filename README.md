# dynamic-analyzer

This is a dynamic analyzer based on `adb`, `emulator`, and `avdmanager` from the Android SDK. The current AVD target is an Android 16 install.

The tool takes the APK to test, spins up a fresh AVD, installs the APK, and then throws inputs at it using `monkey` included in the Android OS. It does this twice and stores network traces as a pcap file.

This uses **Python 3**, I haven't checked for Python 2 compatibility.

## Usage

```txt
python .\dynamicanalyzer.py -h
usage: dynamicanalyzer.py [-h] [-n NAME] [-d | -b] APK

positional arguments:
  APK                   APK to install

optional arguments:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  name of emulator
  -d, --demo            run demo
  -b, --bulk
```
