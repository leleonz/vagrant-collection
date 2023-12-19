# ubuntu-dotnetsdk
Pre-configured vagrant provisioning for .Net development on Ubuntu machine.
Ubuntu version (default): v22/ jammy64
.Net SDK version (default): v7.0

How to change Ubuntu version:
```
config.vm.box = "ubuntu/{ubuntu version}"
```

How to change .Net SDK version:
```
apt-get install -y dotnet-sdk-{version number}
```