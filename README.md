Role Name
=========

This Ansible Simple Role just ensure apt-get is up to date and install language packs.

Take a look to this role in Ansible Galaxy website: https://galaxy.ansible.com/list#/roles/2465

To take in account:
* This role may be compatible with other operating systems than Ubuntu, but it hasn't been tested on no one else.
* This role has been tested on Ansible 1.8 but it could be compatible with lower version as well.

Requirements
------------

None.

Installation
------------

```bash
$ ansible-galaxy install aramirez-es.common
```

Role Variables
--------------

You just should define **language** variable if you want to install any language package, for instance:

```yml
common_languages:
  - language-pack-es
  - language-pack-en
```

By default, **language-pack-en** is installed.

Dependencies
------------

None.

Example Playbook
----------------

Just add **common** role in your playbook and enjoy!

```yml
- hosts: servers
  sudo: true
  roles:
    - role: common
```

If you want to install other language pack besides **language-pack-en**:

```yml
- hosts: servers
  sudo: true
  roles:
    - role: common
      common_languages:
        - language-pack-es
        - language-pack-en
```

License
-------

MIT
