htpasswd
========

A role for managing htpasswd files.

Compatibility
-------------

  - CentOS 6
  - CentOS 7
  - Ubuntu 12.04
  - Ubuntu 14.04
  - Ubuntu 16.04
  - Debian 8
  - Debian 9

Role Variables
--------------

- htpasswd_files

This variable is a list containing informations about each htpasswd files you want to deploy.
Some keys are optionals, you can see their default values.
When create_folder is set, the owner/group set will be the same as the htpasswd file.

```YAML
htpasswd_files:
  - path: /path/to/htpasswd/file
    create_folder: yes            # default to no
    owner: nobody                 # default to ansible_user_uid
    group: nobody                 # default to ansible_user_gid
    mode: 0444                    # default to 0644
    users:
      - name: user1
        password: password1
      - name: user2
        password: password2
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-htpasswd }

License
-------

MIT

Author Information
------------------

Sofiane MEDJKOUNE
