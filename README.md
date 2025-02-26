# CCminer for Termux an userland

Based on: https://github.com/Oink70/CCminer-ARM-optimized

Install  Termux or userland: 

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
for userland 

# ccminer for ARM 

Based on https://github.com/monkins1010/ccminer/tree/ARM

Git and Build Process:
```
apt-get update
```
```
apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential
```
```
apt-get install libllvm-16-ocaml-dev libllvm16 llvm-16 llvm-16-dev llvm-16-doc llvm-16-examples llvm-16-runtime clang-16 clang-tools-16 clang-16-doc libclang-common-16-dev libclang-16-dev libclang1-16 clang-format-16 python3-clang-16 clangd-16 clang-tidy-16 libclang-rt-16-dev libpolly-16-dev libfuzzer-16-dev lldb-16 lld-16 libc++-16-dev libc++abi-16-dev libomp-16-dev libclc-16-dev libunwind-16-dev libmlir-16-dev mlir-16-tools flang-16 libclang-rt-16-dev-wasm32 libclang-rt-16-dev-wasm64 libclang-rt-16-dev-wasm32 libclang-rt-16-dev-wasm64
```
```
git clone https://github.com/codlindor/CCminer-ARM.git
```
```
cd CCminer-ARM
```
```
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
chmod +x start.sh
CXX=clang++ CC=clang
```
```
./build.sh
```
```
nano config.json
```
start mining by typing :
```
~/CCminer-ARM/start.sh
```

