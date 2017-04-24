# webrtc mobile static build

Scripts to generate static versions of webrtc library for android and ios.   It is 99% based on excelent @saghul script used in [react-native-webrtc project].

Status:
* Android: Working (apparently)
* iOS: Not done yet

## How to use it

### Android

Prerequirements: Linux with some basic packages installed (git, tar...).   I use docker to build this:
```
docker run -it --volume=$(pwd):/opt/workspace ubuntu bash
apt-get install python git lbzip2 lbs-release sudo locales
```
```
python build-webrtc.py --setup --android ~/src/
python build-webrtc.py --build --android ~/src/
python build-webrtc.py --package --android ~/src/
````

### iOS
Pending