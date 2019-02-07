Role Name
=========

This should be downloaded into the roles folder: default of /etc/ansible/roles/

Uses the raw command to install python as required for ansible. Should be inserted as a role for the very first run on the target.

The main play in /etc/ansible/playbooks/ must have gather_facts:false for this to work since gather_facts pieces uses python.

You can run this with other roles just fine, as long as this role is specified first (so it installs python before going to the commands that use python):

---
- hosts: all
  remote_user: your_user
  gather_facts: false
  become: true
  roles:
    - first_run
    - second role
    - third role

Author Information
------------------
Steven Craig
