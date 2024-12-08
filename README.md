# Install WSL2 with Ubuntu 20.04.6

SVM mode.
```
step1 When booting up, press F2 to enter the BIOS.
step2 Press F7 to switch to Advanced Mode.
step3 Set SVM to "Enabled."
step4 Set UMA Frame Buffer Size to "Auto."
step5 Press F10 and confirm by selecting OK.
```

Windows Linux Subsystem - 1
```
step1 Control Panel
step2 Programs
step3 Programs and Features
step4 Turn Windows features on or off
step5 Enable Windows Hypervisor
```

In Window power shell running as administrator, then reboot.
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Windows Linux Subsystem - 2
```
step1 Control Panel
step2 Programs
step3 Programs and Features
step4 Turn Windows features on or off
step5 Enable Windows Subsystem for Linux
step6 Enable Virtual Machine Platform
```


WSL, in Window power shell running as administrator, then reboot.
```
wsl --install
wsl --version
wsl --set-default-version 2
```

Install Ubuntu
```
wsl --install -d Ubuntu-20.04
exit
wsl --list --verbose
wsl --set-version Ubuntu-20.04 2
```

Remove Ubuntu if needed
```
wsl --unregister Ubuntu-20.04
```

Check systemd
```
wsl -d Ubuntu-20.04
systemd
```
Install systemd if needed
```
sudo apt install git
git clone https://github.com/DamionGans/ubuntu-wsl2-systemd-script.git
cd ubuntu-wsl2-systemd-script/
bash ubuntu-wsl2-systemd-script.sh
# Enter your password and wait until the script has finished
systemctl
```

Reboot Ubuntu, after install systemd
```
wsl -t Ubuntu-20.04
wsl -d Ubuntu-20.04
systemd
ps aux # check existence of systemd process
```

Install Docker
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo docker run hello-world
```





