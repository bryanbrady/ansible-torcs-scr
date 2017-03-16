TORCS Simulated Car Racing Championship
=======================================

Install TORCS Simulated Car Racing Championship

https://arxiv.org/abs/1304.1672

Getting started:
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


