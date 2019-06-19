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

# Usage:

```
  ansible-playbook -i test/hosts.ini test/k8s-inception-demo.yml
```
