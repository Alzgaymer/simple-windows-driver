# Requirements

- [Visual Studio 2019](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=16)

- [WDK](https://go.microsoft.com/fwlink/?linkid=2128854)

- [Windows 10 Enterprise](https://go.microsoft.com/fwlink/p/?LinkID=2208844&clcid=0x409&culture=en-us&country=US)

- [Virtual Box](https://www.virtualbox.org/)

Follow this [video](https://www.youtube.com/watch?v=JT8EXoobjSc&ab_channel=ProgrammingKnowledge2) for correct download 

# simple-windows-driver

Firstly run cmd.exe as administrator to turn test signature mode after reloading

```console
bcdedit /set testsigning on
```

Run cmd.exe as administrator after compiling project

This comman create folder in regestry editor HKLM\System\CurrentControlSet\Services\sample

```console
sc create sample type= kernel binPath= [<u> ** your path to repo ** </u>]\simple-windows-driver\x64\debug\sample.sys
```

## Run driver

cmd.exe must be runned as andministrator

```console
sc start sample
```

## Stop driver

cmd.exe must be runned as andministrator

```console
sc stop sample
```
