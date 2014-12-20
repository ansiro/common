Role Name
=========

This Ansible Simple Role just ensure apt-get is up to date and install language packs.

Requirements
------------

None.

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
  roles:
    - role: common
```

If you want to install other language pack besides **language-pack-en**:

```yml
- hosts: servers
  roles:
    - role: common
      common_languages:
        - language-pack-es
        - language-pack-en
```

License
-------

MIT
