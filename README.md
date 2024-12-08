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
[systemd install](https://github.com/DamionGans/ubuntu-wsl2-systemd-script)  

Reboot Ubuntu, after install systemd
```
wsl -t Ubuntu-20.04
wsl -d Ubuntu-20.04
systemd
ps aux # check existence of systemd process
```


