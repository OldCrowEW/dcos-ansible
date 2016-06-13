# dcos-ansible

This repo uses [Ansible](https://www.ansible.com/) to configure a [Mesosphere](https://mesosphere.com/) stack following the [DC/OS Advanced Installation Guide](https://dcos.io/docs/1.7/administration/installing/custom/advanced/)

Currently all IPs are hardcoded. This will be updated to dynamic variables in the future. For now you must modify the following files with the correct values:

- [hosts.ini](https://github.com/OldCrowEW/dcos-ansible/blob/master/hosts.ini)
- [roles/dcos-bootstrap/templates/config.yaml.j2](https://github.com/OldCrowEW/dcos-ansible/blob/master/roles/dcos-bootstrap/templates/config.yaml.j2)
- [roles/bootstrap-mesos-master/tasks/main.yml](https://github.com/OldCrowEW/dcos-ansible/blob/master/roles/bootstrap-mesos-master/tasks/main.yml)
- [roles/bootstrap-mesos-slave/tasks/main.yml](https://github.com/OldCrowEW/dcos-ansible/blob/master/roles/bootstrap-mesos-slave/tasks/main.yml)

## Usage
```
ansible-playbook -i hosts.ini playbook-dcos.yaml -u centos --private-key=key.pem
```