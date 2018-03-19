# k8s-tensorflow-app

This ansible role deploys a tensorflow notebook which accesses tensorflow serving based inception architecture to classify images of cats from http://thecatapi.com. The script to deploy tensorflow serving containers are derived from this [repository](https://github.com/markgoddard/magnum-tools/tree/master/k8s-demo).

After the notebook is deployed, a hyperlink to the notebook will be shown on the Ansible logs as the final task.
