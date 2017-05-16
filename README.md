TORCS Simulated Car Racing Championship
=======================================

Install TORCS Simulated Car Racing Championship

https://arxiv.org/abs/1304.1672

This was tested in VirtualBox using Desktop Ubuntu 16.04.2 LTS.

Getting Started
---------------

Installing TORCS:
1. Create `inventory.yml` and add the following:
    ```
    [servers]
    server ansible_port=22 ansible_host=<ip addr>
    ```

2. Create `torcs-scr-playbook.yml` and add the following:
    ```
    - hosts: servers
      roles:
        - { role: ansible-torcs-scr}
    ```

3. Run this command (update the user as necessary):

    ```
    ansible-playbook -i inventory.yml -K --user=torcs torcs-scr-playbook.yml
    ```


Running TORCS:
1. Run TORCS: `torcs`
2. Select Race->Quick Race->New Race
3. In a second terminal, run: `$HOME/torcs-1.3.5/scr-client-cpp/client`

Requirements
------------

None

Role Variables
--------------

Defaults

    torcs_version: 1.3.5
    torcs_src_dir: "{{ansible_env.HOME}}/torcs-{{ torcs_version }}"

Dependencies
------------

Requires sudo.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-torcs-scr}

License
-------

BSD

Author Information
------------------


