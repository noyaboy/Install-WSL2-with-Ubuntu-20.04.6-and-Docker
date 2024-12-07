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
![image](https://github.com/user-attachments/assets/cd8ec24d-a22e-47bb-9572-ced6aa340b8d)
確認輸出GPU型號
```
lspci | grep -i nvidia
```
![image](https://github.com/user-attachments/assets/cf7c0e12-ef7e-4ec6-bb23-aadd0db52af1)
```
```

```
```




Install flow: https://medium.com/@misscoming/%E5%9C%A8-windows-10-%E4%B8%8A%E8%B7%91-ubuntu-18-04-92f80b2d725b
