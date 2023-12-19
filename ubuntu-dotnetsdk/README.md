# ubuntu-dotnetsdk
Pre-configured vagrant provisioning for .Net development on Ubuntu machine.
- Ubuntu version (default): v22/ jammy64
- .Net SDK version (default): v7.0

## How to change Ubuntu version
1. Go to Vagrantfile
2. Look for ```config.vm.box``` property and update to your chosen ubuntu version
```
config.vm.box = "ubuntu/{ubuntu version}"
```

## How to change .Net SDK version
**Using inline script:**
1. Go to Vagrantfile
2. Look for following line and update dotnet sdk installation to your chosen sdk version
```
apt-get install -y dotnet-sdk-{version number}
```
*or*
**Using external script:**
1. Go to Vagrantfile
2. Use either hardcoded or variable script path
3. Look for ```s.args``` property and update the arguments (in an array) to your chosen sdk version
```
config.vm.provision "shell" do |s|
  s.path = "scripts/bootstrap.sh"
  s.args = ["{version number}"]
```
