Role Name
=========

Backup the configuration from various network-devices to git.

Requirements
------------

[Cisco IOS Collection](https://galaxy.ansible.com/cisco/ios)<br>
[Cisco NXOS Collection](https://galaxy.ansible.com/cisco/nxos)<br>
[Community Network Collection](https://galaxy.ansible.com/community/network)

Role Variables
--------------

- git\_dest
- git\_repo
- git\_version

Dependencies
------------

None.

Example Playbook
----------------

    ---
    - name: backup config from target to git
      hosts: "{{ target }}"
      gather_facts: false

      roles:
        - role: network_backup
          tags: backup
          when: not ansible_check_mode

License
-------

BSD

Author Information
------------------

Jørn Ivar Holland
