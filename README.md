# CCminer for Termux and userland

Based on: https://github.com/Oink70/CCminer-ARM-optimized

Termux 

Proceed with installation, configuration & compilation:

1. Installing clang and dependencies:
```
yes | pkg update && pkg upgrade -y
```
```
yes | pkg install libjansson build-essential clang binutils git -y
```
2. Fix environment & clone repo:
```
cp /data/data/com.termux/files/usr/include/linux/sysctl.h /data/data/com.termux/files/usr/include/sys
```
```
git clone https://github.com/codlindor/ccminer.git
```
```
cd ccminer
```
```
chmod +x build.sh configure.sh
```
```
chmod +x autogen.sh start.sh
```
3. Edit Arch & Cores:
```
nano configure.sh
```

4. Compile ccminer:
```
CXX=clang++ CC=clang ./build.sh
```
5. Change your pools, address, and miner name with:
```
nano config.json
```
6. Finally run the miner with:
```
~/ccminer/start.sh
```

# ccminer for ARM Userland 




1. Installing clang and dependencies:
```
sudo apt-get update
```
```
sudo apt-get full-upgrade
```
```
sudo apt-get install build-essential
```
```
sudo apt-get install clang
```
```
sudo apt-get install git
```
```
git clone https://github.com/codlindor/ccminer.git
```
```
cd ccminer
```
```
chmod +x build.sh configure.sh
```
```
chmod +x autogen.sh start.sh
```
3. Edit Arch & Cores:
```
nano configure.sh
```

4. Compile ccminer:
```
CXX=clang++ CC=clang ./build.sh
```
5. Change your pools, address, and miner name with:
```
nano config.json
```
6. Finally run the miner with:
```
~/ccminer/start.sh
```
