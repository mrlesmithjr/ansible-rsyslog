Role Name
=========

Installs rsyslog (Configurable and remote syslog server ready)

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

````
configure_rsyslog: false  #defines if rsyslog should be reconfigured
pri_domain_name: example.org  #defines primary domain name...define here or globally in group_vars/all
syslog_servers: []  #defines remote syslog servers...define here or globally in group_vars/all
#  - name: 'graylog.{{ pri_domain_name }}'
#    proto: udp
#    port: 514
#  - name: 'logstash.{{ pri_domain_name }}'
#    proto: tcp
#    port: 514
````

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: mrlesmithjr.rsyslog }

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com
