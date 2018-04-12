# k8s-inception-ansible

This ansible role deploys a jupyter notebook that interfaces with a tensorflow
server using a tensorflow client to classify images of cats from
http://thecatapi.com.


The script to deploy tensorflow serving containers are derived from this
[repository](https://github.com/markgoddard/magnum-tools/tree/master/k8s-demo).

This role was originally conceived as a component of this
[repository](https://github.com/stackhpc/kubespray).

After the notebook is deployed, a hyperlink to the notebook will be
shown on the ansible logs as the final task.

# Pre-requisite:

Ensure that you cofigure your `~/.ssh.config` includes something similar to
the following configuration where `ilab-gate` is your gateway node which
is on the same subnet as your kubernetes cluster.

```
Host ilab-gate
  User hpckunw1
  HostName alaska-gate.vss.cloud.cam.ac.uk
  IdentityFile ~/.ssh/id_rsa
  ForwardAgent yes 
Host 10.60.253.*
  User fedora
  ProxyCommand ssh -q -W %h:%p ilab-gate
  IdentityFile ~/.ssh/k8s_ilab
  StrictHostKeyChecking no
  UserKnownHostsFile /dev/null
```

# Usage:

```
  ansible-playbook -i hosts.ini k8s-inception-demo.yml
```
