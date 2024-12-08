# Install WSL2 with Ubuntu 20.04.6

SVM mode
```
step1 When booting up, press F2 to enter the BIOS.
step2 Press F7 to switch to Advanced Mode.
step3 Set SVM to "Enabled."
step4 Set UMA Frame Buffer Size to "Auto."
step5 Press F10 and confirm by selecting OK.
```

Windows Linux Subsystem
```
step1 Control Panel
step2 Programs
step3 Programs and Features
step4 Turn Windows features on or off
step5 Enable Windows Subsystem for Linux
step6 Enable Windows Hypervisor

```

In Window power shell running as administrator
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

WSL, in Window power shell running as administrator
```
wsl --install
```

WSL2 after rebooting
```
wsl --install -d Ubuntu-20.04
wsl --set-version Ubuntu-20.04 2
wsl --list --verbose
exit
wsl -d Ubuntu-20.04
```

Remove
```
wsl --unregister Ubuntu-20.04
```


