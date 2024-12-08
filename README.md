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
sudo apt install libboost-all-dev
dpkg -s libboost-all-dev | grep Version
sudo apt install cmake
cmake --version
sudo apt install software-properties-common
sudo add-apt-repository 'deb https://root.cern/download/cling apt main'
wget https://root.cern/download/cling/keys/ROOT.gpg.key
sudo apt-key add ROOT.gpg.key
sudo apt update
sudo apt install root-system-bin
```
新增下行至.bashrc
```
source /usr/lib/root/bin/thisroot.sh
```
```
source ~/.bashrc
root
```
檢查
```
`dpkg -s libboost-all-dev
cmake --version
root
```




Install flow: https://medium.com/@misscoming/%E5%9C%A8-windows-10-%E4%B8%8A%E8%B7%91-ubuntu-18-04-92f80b2d725b
