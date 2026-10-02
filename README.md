# TSI-203 Seguridad de Redes
## Infraestructura 3 – Acceso HTTPS y VPN Remote-Site

**Estudiante:** Jennifer López  
**Matrícula:** 20240860  

## 🎥 Video de demostración

🔗 **Enlace:** Pendiente de agregar

---

## Objetivo

Implementar una infraestructura de Seguridad de Redes utilizando
un FortiGate y un router Cisco, separando la red de usuarios de
la red de servidores.

La infraestructura está diseñada para permitir acceso HTTPS al
servidor sin necesidad de VPN y restringir el acceso administrativo
SSH mediante una VPN Remote-Site.

## Características principales

- 1 FortiGate.
- 1 router Cisco.
- Red de usuarios /25.
- VLAN 10.
- DHCP.
- Red de servidores /28.
- Direccionamiento WAN público simulado.
- Servidor HTTPS y SSH.
- Acceso HTTPS sin VPN.
- Acceso SSH mediante VPN Remote-Site.
- Políticas de seguridad y control de acceso.

## Direccionamiento

| Dispositivo | Interfaz | Dirección |
|---|---|---|
| R-USER | Fa0/0 | 200.20.86.1/30 |
| R-USER | Fa1/0.10 | 10.86.0.1/25 |
| PC1-USER | VLAN 10 | 10.86.0.10/25 (DHCP) |
| FortiGate | port1 | 200.20.86.2/30 |
| FortiGate | port2 | 10.86.1.1/28 |
| WEB-SERVER | eth0 | 10.86.1.2/28 |

## Diseño de seguridad

El diseño separa el acceso público al servicio web del acceso
administrativo al servidor.

- HTTPS utiliza TCP/443.
- SSH utiliza TCP/22.
- SSH no debe exponerse directamente mediante la WAN.
- El acceso administrativo se realiza mediante la VPN Remote-Site.

## Validaciones realizadas

Durante la implementación se verificaron:

- Interfaces WAN y LAN.
- VLAN 10.
- Asignación de direccionamiento mediante DHCP.
- Comunicación R-USER ↔ FortiGate.
- Comunicación FortiGate ↔ WEB-SERVER.
- Direccionamiento de la red SERVER.
- Enrutamiento y conectividad básica.

También se realizó troubleshooting relacionado con la administración
HTTPS del FortiGate y la instalación de servicios en el servidor.

## Documentación

La documentación técnica completa, incluyendo configuración,
evidencias y troubleshooting, se encuentra dentro de este repositorio.

## Evidencias

Las capturas y resultados obtenidos durante la práctica se encuentran
documentados y explicados en la documentación técnica.
