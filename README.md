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

[WSL2 Update](https://samiouob.github.io/2019/06/17/WSL2/)
[Install flow](https://medium.com/@misscoming/%E5%9C%A8-windows-10-%E4%B8%8A%E8%B7%91-ubuntu-18-04-92f80b2d725b)
