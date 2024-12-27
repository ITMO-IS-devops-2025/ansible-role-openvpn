# ansible-role-openvpn

Installs open-vpn server and get its config file on Ubuntu. Role created within educational process and for educational purposes.

Requirements
------------

- Target machine is Ubuntu.

Role Variables
--------------

- openvpn_configuration_directory: path to directory where all required files would init
- openvpn_result_directory: path to directory in wich config would init

Dependencies
------------

No dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - openvpn


    - hosts: servers
      roles:
        - role: openvpn
          vars:
            openvpn_configuration_directory:
                ./openvpn/
            openvpn_result_directory:
                ./

License
-------

MIT

Author Information
------------------

Roman Soloviev
