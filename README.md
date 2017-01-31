ansible-kernel-modules
======================

Ansible role for simple management of kernel modules including persisting module loading, blacklisting.

Requirements
------------

No special requirements.

Role Variables
--------------

```
kernel_modules:
  - name: dummy
    autoload: false
  - name: dummy
    params: 'numdummies=2'
  - name: dummy
    unload: yes
    blacklist: yes
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

An example playbook on how to use this role:

```
- hosts: servers
  roles:
     - { role: galexrt.kernel-modules, x: 42 }
```

License
-------

MIT

Author Information
------------------

If you have problems with the role, feel free to create an issue on Github or contact me by mail.
