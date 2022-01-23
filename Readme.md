# Dependencies

## Software
    * Vagrant (https://www.vagrantup.com/)
    * VirtualBox (https://www.virtualbox.org/)

### Vagrant vbox-guest pluging

```bash
vagrant plugin install vagrant-vbguest
```

# Spinning up the cluster

```bash
cd tests/cluster
vagrant up
```

# Interacting with the cluster

## Adding the cluster dns entry to the hosts file

Linux
```bash
echo "127.0.0.1     master.kubernetes.local >> /etc/hosts"
```

Windows
```powershell
Add-Content "$env:SystemRoot\system32\etc\hosts" -Value "127.0.0.1     master.kubernetes.local" 
```

## Checking if the cluster is up and running
```bash
kubectl --kubeconfig=kube.config get nodes 
```

# Destroying the cluster
```bash
cd tests/cluster
vagrant destroy -f
```