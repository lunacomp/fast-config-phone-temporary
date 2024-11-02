# fast-config-phone-temporary
Configurasi cepat untuk mining verus di cloud phone

# 1. Installing clang and dependencies:
```
yes | pkg update && pkg upgrade
yes | pkg install libjansson build-essential clang binutils git wget
```
# 2. Fix environment & clone repo:
```
cp /data/data/com.termux/files/usr/include/linux/sysctl.h /data/data/com.termux/files/usr/include/sys
git clone https://github.com/Darktron/ccminer.git
cd ccminer
chmod +x build.sh configure.sh autogen.sh start.sh
```
# 3. Compile ccminer:
```
CXX=clang++ CC=clang ./build.sh
```
# 4. Download your pools, address, and miner name with:
```
cd ccminer
wget -O ~/ccminer/run.sh https://raw.githubusercontent.com/lunacomp/fast-config-phone-temporary/refs/heads/main/config-solo && chmod +x run.sh
cd
curl -o start.sh -k https://raw.githubusercontent.com/lunacomp/ccminer-lunacomp/main/start.sh && chmod +x start.sh
```
# 5. Start Mining
```
cd
./start.sh
```
