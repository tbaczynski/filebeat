Role Name
=========

Install and setup filebeat.

Requirements
------------


Role Variables
--------------

```yaml
es_filebeat_logstash_hosts:
  - 'logstash.example.com'
es_filebeat_logstash_port: 5444
es_filebeat_main_tags:
  - '{{ inventory_dir|basename }}'
es_filebeat_inputs:
  - name: filebeat
  - name: openstack
  - name: ceph
  - name: libvirt
```

see in defaults/main.yaml

If set monitoring to ES, you need to set up `es_elastic_coordination` variable.


Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - role: filebeat
```

License
-------

BSD

Author Information
------------------

Tomasz <bul> Baczyński
Michał <warf> Łuczak
