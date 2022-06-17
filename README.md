# poc_vagrant

##### Running vagrant at 42.
Vagrant and bsdtar are now installed by default on the linux dump.
So only need to change vbox path for VMs to avoid flood home space usage.

Choose either `tmp` or `goinfre` folder:
```shell
vboxmanage setproperty machinefolder ~/goinfre
```
However logout mean lost of VMs...
If persistance matter, try into your server goinfre folder `~/sgoinfre/`
```shell
vboxmanage setproperty machinefolder ~/sgoinfre
```
But server goinfre probably means VMs slow AF...

#### install vagrant autocomplete (and other autocomplete stuff...)
```shell
  git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```

Then add it to FPATH in your .zshrc by adding the following line before source `$ZSH/oh-my-zsh.sh`:
```shell
fpath+=${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions/src
```

#### install kubectl in our home for part 3
```shell

mkdir -p ~/bin
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

mv kubectl ~/bin/
```

- https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/ 

#### Sources :

##### Vagrant
- [vagrant doc](https://www.vagrantup.com/docs)
- [vagrantfile tips](https://www.vagrantup.com/docs/vagrantfile/tips)
- [vagrant boxes](https://app.vagrantup.com/boxes/search)
- [multi machines](https://www.vagrantup.com/docs/multi-machine)

##### k3s
- [k3s multinode install](https://projectcalico.docs.tigera.io/getting-started/kubernetes/k3s/multi-node-install)
