# ansible template
An example how to deploy kubernetes ressources with Ansible.

The application consists of three services:
- React client which is reachable through localhost:3000
- Flask backend reachable through localhost:5001
- Express backend reachable through localhost:5002
All services are exposed through NodePort

## requirements
If you are on Linux, you can just install Ansible. If you are on Windows, you need to use wsl. Docs how to setup Ansible on difference operating systems:
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

After installing Ansible you need to install Kubernetes core extension.
```
ansible-galaxy collection install kubernetes.core
```
If you are interested, here is how to setup from docs:
https://galaxy.ansible.com/kubernetes/core
## how to start
create molecule role
```
molecule create
```

let molecule role run
```
molecule converge
```

destroy molecule environment
```
molecule destroy
```

check k8s ressources
```
kubectl get all
```

