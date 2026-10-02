# Topología – Infraestructura 3

La Infraestructura 3 fue desarrollada en GNS3 utilizando un
router Cisco, un firewall FortiGate, switches Ethernet y un
servidor Ubuntu.

## Red USER

- Red: 10.86.0.0/25
- VLAN: 10
- Gateway: 10.86.0.1
- PC1-USER: 10.86.0.10/25
- Asignación mediante DHCP

## Red WAN

- R-USER: 200.20.86.1/30
- FortiGate port1: 200.20.86.2/30

## Red SERVER

- Red: 10.86.1.0/28
- FortiGate port2: 10.86.1.1/28
- WEB-SERVER: 10.86.1.2/28

## Diseño de seguridad

El servicio HTTPS está destinado al acceso web sin VPN.

El servicio SSH se mantiene separado del acceso público y está
destinado a utilizarse mediante una conexión VPN Remote-Site.

La segmentación permite mantener separados los usuarios, la red
WAN y el servidor.
