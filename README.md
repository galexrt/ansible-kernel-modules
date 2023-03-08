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
# Module dummy will be added to autoload and loaded immediately
  - name: dummy
# This module will be loadedn but not autoloaded
  - name: dummy
    autoload: false
# Module will be loaded with params
  - name: dummy
    params: 'numdummies=2'
# Module will be unloaded and blacklisted
  - name: dummy
    unload: true
    blacklist: true
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
