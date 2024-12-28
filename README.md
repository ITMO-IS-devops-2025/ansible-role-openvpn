# ansible-role-openvpn

Installs open-vpn server and get its config file on Ubuntu. Role created within educational process and for educational purposes.

Requirements
------------

- Target machine is Ubuntu.

Role Variables
--------------

- openvpn_configuration_directory: path to directory where all required files would init
- openvpn_result_directory: path to directory in wich config would init (local)
- openvpn_local_server_ip: host ip
- openvpn_forwarding_name: forward name for ufw configuration
- openvpn_forwarding_value: forward value for ufw configuration
- openvpn_server_ip: local ip for openvpn server
- openvpn_server_port: openvpn server port
- openvpn_server_mask: openvpn server mask
- openvpn_client_dns: openvpn client dns
- openvpn_server_dhcp: openvpn server dhcp
- openvpn_required_packages: packages to install for openvpn
- openvpn_key_files: files with keys for server up
- openvpn_client_key_files: files for client for openvpn connect to create connect
- openvpn_ufw_before_rules_content: ufw before rules configuration content
- openvpn_key_country: country for CA
- openvpn_key_province: province for CA
- openvpn_key_city: city for CA
- openvpn_key_org: organisation for CA
- openvpn_key_email: email for CA
- openvpn_key_size: key size for CA keys
- openvpn_key_ou: organisation unit for CA


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
