ANSIBLE-ROLE-OPENJDK
====================

Ansible role install Openjdk.


## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: git+https://github.com/redbeard28/ansible-role-openjdk.git
  version: master
  name: ansible-role-openjdk
````

or
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: redbeard28.openjdk
````
More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible 2.9+


Role Variables
--------------

```yaml
---
openjdk_version: 8
```

Dependencies
------------

 - redbeard28.bootstrap

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redbeard28.openjdk, tags: mytags }


Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
image=debian tag="buster" molecule converge 
image=debian tag="buster" molecule verify 
```

Author Information
------------------

Jeremie CUADRADO[¹](mailto:info@redbeard-consulting.fr) from Redbeard-Consulting
