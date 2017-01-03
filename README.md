Manage Openvpn
==============


Openvpn server
--------------

1. Create and configure openvpn (server and client)

  `ansible-playbook -i hosts --become --ask-become-pass --tags ovpn_init vpnserver_playbook.yml`

  or

  `ansible-playbook -i hosts --become --ask-become-pass --tags server_init vpnserver_playbook.yml`
  
  `ansible-playbook -i hosts --become --ask-become-pass --tags client_init vpnserver_playbook.yml`


2. Stop and remove container

  * This step is necessary before running the container by Docker Compose tool
  * The configuration is kept into the Docker volume

  `ansible-playbook -i hosts --become --ask-become-pass --tags ovpn_remove vpnserver_playbook.yml`
