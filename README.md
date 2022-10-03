# deploy-container-registry role for Ansible
This repo hosts ansible role for container registry. It will be deployed by using podman.
You can access the registry as follows:
```
$ curl -u user:<PASSWD> -k https://localhost:5000/v2/
$ curl -u user:<PASSWD> -k https://localhost:5000/v2/_catalog
{"repositories":[~~]}
```

## Verification env
- RHEL 8.5
- podman: 4.1.1
- ansible
    ```
    ansible [core 2.13.4]
    config file = /etc/ansible/ansible.cfg
    configured module search path = ['/root/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
    ansible python module location = /root/miniconda3/envs/dev/lib/python3.9/site-packages/ansible
    ansible collection location = /root/.ansible/collections:/usr/share/ansible/collections
    executable location = /root/miniconda3/envs/dev/bin/ansible
    python version = 3.9.13 (main, Aug 25 2022, 23:26:10) [GCC 11.2.0]
    jinja version = 3.1.2
    libyaml = True
    ```

## Collections 
```
(dev)$ ansible-galaxy collection list

# /root/.ansible/collections/ansible_collections
Collection        Version
----------------- -------
ansible.posix     1.4.0  
community.crypto  2.7.0  
community.general 5.6.0  
community.libvirt 1.2.0  
containers.podman 1.9.3  
containers.podman 1.9.3  
```