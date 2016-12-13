gchiesa.docker
==================

Setup the docker engine with docker-compose support on Oracle Linux 7 machines

It also creates a shared folder /docker where to build docker containers and accessible for all users part of the docker group

This playbook will restart the machine (if required) because docker uses a more recent kernel than the one shipped with the standard distribution

Role Variables
--------------
```
# proxy server to use to install packages
proxy: ""

# storage driver to use for docker engine
docker_storage_driver_options: "--storage-driver=devicemapper"

# iptable configuration file
iptables_config: "/etc/sysconfig/iptables"

# disable selinux
disable_selinux: false
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: docker-servers
      roles:
         - { role: gchiesa.docker, proxy: "http://www.proxy.com" }

License
-------

BSD
