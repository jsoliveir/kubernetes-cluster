# Dependencies

## Software
    * Vagrant (https://www.vagrantup.com/)
    * VirtualBox (https://www.virtualbox.org/)

### Vagrant vbox-guest pluging

```bash
vagrant plugin install vagrant-vbguest
```

# Spin up the cluster

```bash
cd tests/cluster
vagrant up
```

# Destroy the cluster
```bash
cd tests/cluster
vagrant destroy -f
```