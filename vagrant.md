## vagrant
_learning by cheatsheet_

#### proxy conf
from https://github.com/tmatilai/vagrant-proxyconf
```vagrant plugin install vagrant-proxyconf```
in $HOME/.vagrant.d/Vagrantfile
```Vagrant.configure("2") do |config|
  if Vagrant.has_plugin?("vagrant-proxyconf")
    config.proxy.http     = "http://192.168.0.2:3128/"
    config.proxy.https    = "http://192.168.0.2:3128/"
    config.proxy.no_proxy = "localhost,127.0.0.1,.example.com"
  end
  # ... other stuff
end```