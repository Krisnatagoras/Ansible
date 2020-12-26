create_user
=========

Create an user on a remote host and upload the ssh public key for remote access.

Requirements
------------

No specific requirements for Ansible
Need a default ssh key 

Role Variables
--------------

-> Define the user to create
user_name: default

-> Define the user state: present or absent
user_state: present

-> Define the path for the SSH KEY
~/.ssh/id_rsa.pub


Dependencies
------------

None

Example Playbook
----------------

    ---
    - hosts: all
      tasks:
        - include_role:
            name: create_user
          vars:
            user_name: krisnatagoras
            ssh_key: ~/.ssh/id_rsa.pub

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
