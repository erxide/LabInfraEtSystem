# LABO INFRASTRUCTURE & RESEAU 2022 2023 – TP DNS DHCP
- 1 Trouvez l’adresse réseau, broadcast, masque sous-réseau, nombre de client possible, plages 
des clients possibles sur les réseaux suivants:
   - 192.168.0.0/24
     ```
     192.168.0.0
     192.168.0.255
     255.255.255.0
     (2^8)-2 = 254
     192.168.0.1 - 192.168.0.254
     ```
    - 10.0.0.0/8
      ```
      10.0.0.0
      10.255.255.255
      255.0.0.0
      (2^24)-2 = 16 777 214
      10.0.0.1 - 10.255.255.254
      ```
    - 172.16.0.0/255.255.0.0
      ```
      172.16.0.0
      172.16.255.255
      255.255.0.0
      (2^16)-2 = 65 534
      172.16.0.1 - 172.16.255.254
      ```
    - 192.168.255.0/30
      ```
      192.168.255.0
      192.168.255.3
      255.255.255.252
      (2^2)-2= 2
      192.168.255.1 - 192.168.255.2
      ```
    - 10.50.0.0/22
      ```
      10.50.0.0
      10.50.3.255
      255.255.252.0
      (2^10)-2 = 1 022
      10.50.0.1 - 10.50.3.254
      ```
    - 172.28.0.0/255.248.0.0
      ```
      172.4.0.0
      172.7.255.255
      255.248.0.0
      (2^19)-2 = 524 286
      172.28.0.1 - 172.7.255.254
      ```
- 2 Mise en place d’un serveur DHCP et DNS :
  - 2.1 Prérequis :
     -  4 machines virtuelles :
     
     ![vm](/pics/vm.png)
    - Configurer ces machines pour utiliser le FQDN [nom explicite].lab.ingesup 
( /etc/hostname puis reboot )
       - dhcp 
       - client01
       - client02
       - dns
  - 2.2 OpenSSH :
    - Modifier le fichier de configuration du serveur SSH ( /etc/ssh/sshd_config ) :

