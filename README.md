# Pre-compiled CCMiner for Termux:
This is a WIP repo for pre-compiled ccminer binaries with latest termux(v0.118.0) and latest clang(v17.0.4).

**`This is for ARM Cortex-A73 & Cortex-A53`**

# Installation:
1. Install latest arm64-v8a [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk):
```
https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk
```
2. Get Termux ready:
```
pkg update -y && pkg upgrade -y
pkg install wget nano -y
```
3. Download ccminer, config, start:
```
mkdir ccminer
cd ccminer
wget https://raw.githubusercontent.com/Darktron/pre-compiled/main/ccminer
wget https://raw.githubusercontent.com/Darktron/pre-compiled/main/config.json
wget https://raw.githubusercontent.com/Darktron/pre-compiled/main/start.sh
chmod +x ccminer start.sh
```
# Usage:

1. Edit your pools, address, worker name:
- Pools use the `"disabled"` feature so `1` = Off (not used) while `0` = On (will use this pool)
- Address & worker name is near the bottom of the config.json in format `"address here"."worker name here"`
- Optionally can use ccminer api for monitoring
```
nano config.json
```
2. Start ccminer with:
```
~/ccminer/start.sh
```
3. Close ccminer with:
```
CTRL + c
```
