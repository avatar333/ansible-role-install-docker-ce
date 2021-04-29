ansible-role-install-docker-ce
=========

This role installs the basic Docker CE suite

Requirements
------------

- Basic CentOS/RHEL OS
- All other package requirements are installed as part of the role

Role Variables
--------------
 **raw_device**:  the name of the raw device (e.g. sdc), to be used to mount against /var/lib/docker. This is prefered, as docker images and containers could consume large amounts of disk. If not supplied, the role will halt execution. If you wish to use the default location of /var/lib/docker that hangs off root (/), please refer to the instructions below

    DEFAULT VALUE:
    - ""

Dependencies
------------

None.

Example Playbook
----------------

Creating a topic **spurs**:

    - hosts: servers
      roles:
         - { role: ansible-role-create-kafka-topic, kafka_topic: "spurs" }

License
-------

BSD

Author Information
------------------

Kevin Pillay
