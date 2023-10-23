Ansible Role: AD Constrained Delegation.
=========

An Ansible role to enable constrained delegation attack on a number of computers in the domain.

Requirements
------------

Needs to be run on the DC.

Role Variables
--------------

```yml
num_delegation_computers: 3
delegation_spns:
  - CIFS/pdc01
  - LDAP/pdc01.ad01.bufu-sec.com
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: pdc01
  roles:
    - role: xbufu.ad_constrained_delegation
      vars:
        num_delegation_computers: 3
        delegation_spns:
          - CIFS/pdc01
          - LDAP/pdc01.ad01.bufu-sec.com
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
