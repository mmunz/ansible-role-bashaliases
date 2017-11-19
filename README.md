Bash aliases
============

This role creates bash aliases that are available for all users.
It adds a file /etc/bash_aliases_ansible which is included in
/etc/bash.bashrc.


Role Variables
--------------


One variable can be set : bashalias_aliases

It is a list of aliases to define. Each element is a string in the form
alias="command".

Example :
bashalias_aliases:
  - ll='ls -hl'
  - la='ls -hal'


Example Playbook
----------------

Example :

  ---
  - hosts: servers
    roles:
      - role: c1.ansible-bashalias
        bashalias_aliases:
          - ll='ls -hl'
          - la='ls -hal'

License
-------

BSD
