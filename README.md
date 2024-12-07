# Reinstall 
In Window power shell run as administrator
```
wsl --list --verbose
wsl --unregister Ubuntu-20.04
wsl --install -d Ubuntu-20.04
exit
wsl -d Ubuntu-20.04
```
# Virtual Environment 
In Ubuntu 20.04.6 LTS
```
python3 --version
pip3 --version
sudo apt update
sudo apt install python3
sudo apt install python3-pip
venv --version
sudo apt install python3-venv
python3 -m venv traccc
source traccc/bin/activate
deactivate
```
# traccc Requirement
In Ubuntu 20.04.6 LTS
```
sudo apt update
sudo apt install -y build-essential cmake g++ gcc libboost-all-dev
```
reinstall gcc
```
gcc --version
sudo apt remove --purge gcc
sudo apt autoremove --purge -y
wget http://ftp.gnu.org/gnu/gcc/gcc-9.3.0/gcc-9.3.0.tar.gz
tar -xvzf gcc-9.3.0.tar.gz
cd gcc-9.3.0
sudo apt update
sudo apt install -y build-essential libgmp-dev libmpfr-dev libmpc-dev
./configure --prefix=/usr/local/gcc-9.3.0 --enable-languages=c,c++ --disable-multilib
make -j$(nproc)
sudo make install
sudo update-alternatives --install /usr/bin/gcc gcc /usr/local/gcc-9.3.0/bin/gcc 100
sudo update-alternatives --install /usr/bin/g++ g++ /usr/local/gcc-9.3.0/bin/g++ 100
gcc --version
g++ --version
```
desired output gcc (Ubuntu 9.3.0-17ubuntu1~20.04) 9.3.0
```
```




Install flow: https://medium.com/@misscoming/%E5%9C%A8-windows-10-%E4%B8%8A%E8%B7%91-ubuntu-18-04-92f80b2d725b
