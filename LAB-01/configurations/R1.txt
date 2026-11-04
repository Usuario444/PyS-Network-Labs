! ============================================================
! CONFIGURACION-PyS-R1
! Proyecto: Laboratorio personal de redes y ciberseguridad
! Plataforma: Cisco IOS en GNS3 (entorno de práctica, no producción)
! Funciones: Router on a Stick (ROAS), DHCPv4 y acceso SSHv2
! ============================================================

ACCESO-Y-MODO-GLOBAL
---------------------------------------
> enable
# configure terminal
(config)#

IDENTIDAD-Y-SEGURIDAD-BASICA
---------------------------------------
(config)# hostname PyS-R1
(config)# ip domain-name lab-local
(config)# no ip domain-lookup
(config)# service password-encryption
(config)# enable secret admin
(config)# banner motd # ACCESO AUTORIZADO UNICAMENTE - PyS Networks #

LINEA-CONSOLA
---------------------------------------
(config)# line console 0
(config-line)# password admin
(config-line)# login
(config-line)# logging synchronous
(config-line)# exec-timeout 10 0
(config-line)# exit

ROAS-INTERFAZ-FISICA-TRONCAL
---------------------------------------
(config)# interface g0/0
(config-if)# description TRONCAL-HACIA-SW-CORE
(config-if)# no ip address
(config-if)# no shutdown
(config-if)# exit

ROAS-SUBINTERFACE-VLAN-99-GESTION
---------------------------------------
(config)# interface g0/0.99
(config-subif)# description GATEWAY-GESTION-SSH
(config-subif)# encapsulation dot1Q 99
(config-subif)# ip address 192.168.10.121 255.255.255.248
(config-subif)# exit

ROAS-SUBINTERFACE-VLAN-10-DESARROLLO
---------------------------------------
(config)# interface g0/0.10
(config-subif)# description GATEWAY-DESARROLLO
(config-subif)# encapsulation dot1Q 10
(config-subif)# ip address 192.168.10.1 255.255.255.192
(config-subif)# exit

ROAS-SUBINTERFACE-VLAN-20-SOPORTE-TI
---------------------------------------
(config)# interface g0/0.20
(config-subif)# description GATEWAY-SOPORTE-TI
(config-subif)# encapsulation dot1Q 20
(config-subif)# ip address 192.168.10.65 255.255.255.224
(config-subif)# exit

ROAS-SUBINTERFACE-VLAN-30-ADMINISTRACION
---------------------------------------
(config)# interface g0/0.30
(config-subif)# description GATEWAY-ADMINISTRACION
(config-subif)# encapsulation dot1Q 30
(config-subif)# ip address 192.168.10.97 255.255.255.240
(config-subif)# exit

ROAS-SUBINTERFACE-VLAN-40-GERENCIA
---------------------------------------
(config)# interface g0/0.40
(config-subif)# description GATEWAY-GERENCIA
(config-subif)# encapsulation dot1Q 40
(config-subif)# ip address 192.168.10.113 255.255.255.248
(config-subif)# exit

ROAS-SUBINTERFACE-VLAN-999-NATIVA
---------------------------------------
(config)# interface g0/0.999
(config-subif)# description VLAN-NATIVA-SIN-IP
(config-subif)# encapsulation dot1Q 999 native
(config-subif)# no ip address
(config-subif)# exit

INTERFAZ-SIN-USO-WAN-FUTURA
---------------------------------------
(config)# interface g0/1
(config-if)# description INTERFAZ-WAN-FUTURA-APAGADA
(config-if)# no ip address
(config-if)# shutdown
(config-if)# exit

DHCPv4-DIRECCIONES-EXCLUIDAS
---------------------------------------
(config)# ip dhcp excluded-address 192.168.10.1
(config)# ip dhcp excluded-address 192.168.10.65
(config)# ip dhcp excluded-address 192.168.10.97
(config)# ip dhcp excluded-address 192.168.10.113

DHCPv4-POOL-DESARROLLO-VLAN-10
---------------------------------------
(config)# ip dhcp pool POOL-DESARROLLO
(dhcp-config)# network 192.168.10.0 255.255.255.192
(dhcp-config)# default-router 192.168.10.1
(dhcp-config)# exit

DHCPv4-POOL-SOPORTE-TI-VLAN-20
---------------------------------------
(config)# ip dhcp pool POOL-SOPORTE-TI
(dhcp-config)# network 192.168.10.64 255.255.255.224
(dhcp-config)# default-router 192.168.10.65
(dhcp-config)# exit

DHCPv4-POOL-ADMINISTRACION-VLAN-30
---------------------------------------
(config)# ip dhcp pool POOL-ADMINISTRACION
(dhcp-config)# network 192.168.10.96 255.255.255.240
(dhcp-config)# default-router 192.168.10.97
(dhcp-config)# exit

DHCPv4-POOL-GERENCIA-VLAN-40
---------------------------------------
(config)# ip dhcp pool POOL-GERENCIA
(dhcp-config)# network 192.168.10.112 255.255.255.248
(dhcp-config)# default-router 192.168.10.113
(dhcp-config)# exit

SSHv2-ADMINISTRACION-REMOTA
---------------------------------------
(config)# crypto key generate rsa modulus 2048
(config)# username admin privilege 15 secret admin
(config)# ip ssh version 2
(config)# line vty 0 15
(config-line)# login local
(config-line)# transport input ssh
(config-line)# exit

GUARDAR-CONFIGURACION
---------------------------------------
(config)# end
# write memory
