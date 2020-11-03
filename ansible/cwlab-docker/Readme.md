# CWLab ansible playbook

This ansible playbook installs docker on ubuntu 18.04 hosts and deploys the cwlab service via
docker. It mounts a host directory to the container.

# Usage

Create a `hosts` file, e.g.

```
# hosts
cwlab-test
```

Run the playbook

```
# install docker commands
ansible-galaxy collection install community.general

# run playbook
ansible-playbook -i hosts install_cwlab.yml
```
