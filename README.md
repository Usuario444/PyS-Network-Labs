<div align="center">

# 🌐 PyS-Network-Labs

### 🛡️ **Laboratorios prácticos de redes y ciberseguridad**

Implementación, configuración y documentación de escenarios de networking orientados al aprendizaje de **CCNA 200-301**, utilizando **GNS3** y entornos Cisco emulados.

<br />

![GNS3](https://img.shields.io/badge/GNS3-Network_Emulation-2F6DB5?style=for-the-badge&logo=gns3&logoColor=white)
![Cisco IOS](https://img.shields.io/badge/Cisco-IOS-049FD9?style=for-the-badge&logo=cisco&logoColor=white)
![CCNA](https://img.shields.io/badge/CCNA-200--301-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Networking](https://img.shields.io/badge/Focus-Networking-163A5F?style=for-the-badge)
![Cybersecurity](https://img.shields.io/badge/Focus-Cybersecurity-00A6A6?style=for-the-badge)

</div>

---

## 🧭 Navegación

- 🔎 [Sobre el proyecto](#-sobre-el-proyecto)
- 🧰 [Tecnologías y herramientas](#-tecnologías-y-herramientas)
- 🗂️ [Contenido del repositorio](#-contenido-del-repositorio)
- 📁 [Estructura del repositorio](#-estructura-del-repositorio)
- 📝 [Documentación de los laboratorios](#-documentación-de-los-laboratorios)
- 📊 [Progreso](#-progreso-del-repositorio)
- 🎯 [Objetivos de aprendizaje](#-objetivos-de-aprendizaje)
- 👨‍💻 [Autor y propósito](#-autor-y-propósito)

---

## 🔎 Sobre el proyecto

**PyS-Network-Labs** es un repositorio personal de laboratorios de redes y ciberseguridad desarrollados principalmente en **GNS3**. Reúne topologías, configuraciones de dispositivos y documentación técnica de prácticas orientadas a consolidar conocimientos de networking.

El repositorio sigue un enfoque práctico:

1. 📐 **Diseñar** una topología según el objetivo del laboratorio.
2. ⚙️ **Implementar** las tecnologías y configuraciones necesarias.
3. 🔍 **Verificar** el comportamiento de la red mediante comandos y pruebas.
4. 📄 **Documentar** el procedimiento, los resultados y las observaciones.

```mermaid
flowchart LR
    A["📐 Diseñar topología"] --> B["⚙️ Configurar dispositivos"]
    B --> C["🔍 Verificar funcionamiento"]
    C --> D["📄 Documentar resultados"]

    classDef step fill:#163A5F,stroke:#049FD9,stroke-width:2px,color:#ffffff,font-weight:bold;
    class A,B,C,D step;
```

El contenido toma como referencia los temas de **CCNA 200-301** y puede ampliarse hacia escenarios de infraestructura y seguridad de redes.

---

## 🧰 Tecnologías y herramientas

Las herramientas principales identifican el entorno de trabajo. Las demás tecnologías representan áreas que pueden utilizarse de acuerdo con el objetivo y alcance de cada laboratorio; sus badges no significan que estén implementadas en todos los escenarios publicados.

### 🖥️ Entorno principal

<p>
  <img src="https://img.shields.io/badge/GNS3-Entorno_principal-2F6DB5?style=flat-square&logo=gns3&logoColor=white" alt="GNS3" />
  <img src="https://img.shields.io/badge/Cisco_IOS-Dispositivos_emulados-049FD9?style=flat-square&logo=cisco&logoColor=white" alt="Cisco IOS" />
  <img src="https://img.shields.io/badge/CCNA-200--301-1BA0D7?style=flat-square&logo=cisco&logoColor=white" alt="CCNA 200-301" />
</p>

### 🛠️ Tecnologías de referencia

<p>
  <img src="https://img.shields.io/badge/Networking-Concepts-163A5F?style=flat-square" alt="Networking" />
  <img src="https://img.shields.io/badge/TCP%2FIP-Protocols-245B8F?style=flat-square" alt="TCP/IP" />
  <img src="https://img.shields.io/badge/VLANs-Switching-2878A8?style=flat-square" alt="VLANs" />
  <img src="https://img.shields.io/badge/Routing_%26_Switching-Infrastructure-245B8F?style=flat-square" alt="Routing and Switching" />
  <img src="https://img.shields.io/badge/SSH-Remote_Access-333333?style=flat-square&logo=openssh&logoColor=white" alt="SSH" />
  <img src="https://img.shields.io/badge/Linux-CLI_%26_Networking-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Wireshark-Traffic_Analysis-1679A7?style=flat-square&logo=wireshark&logoColor=white" alt="Wireshark" />
  <img src="https://img.shields.io/badge/Cybersecurity-Network_Security-008B8B?style=flat-square" alt="Cybersecurity" />
</p>

> [!NOTE]
> **Nota:** la presencia de una tecnología en esta sección indica que forma parte del alcance de aprendizaje del repositorio. Consulta el README de cada laboratorio para conocer exactamente qué se configuró y verificó.

---

## 🗂️ Contenido del repositorio

Las siguientes son **categorías de organización y trabajo**. No representan una afirmación de que todos los laboratorios estén publicados o completados.

| 📌 Área | 📖 Temas considerados |
| :--- | :--- |
| 🔀 **Switching** | Configuración de switches y fundamentos de conmutación. |
| 🏷️ **VLANs y Trunking** | Creación de VLANs, asignación de puertos y enlaces troncales 802.1Q. |
| 🌉 **Inter-VLAN Routing** | Comunicación entre VLANs mediante Router-on-a-Stick o SVI, según el escenario. |
| 🔗 **EtherChannel y LACP** | Agrupación de enlaces y negociación mediante LACP. |
| 🌳 **STP y RSTP** | Prevención de loops, elección de Root Bridge y roles/estados de puertos. |
| 🧭 **Routing** | Rutas estáticas y protocolos de enrutamiento dinámico. |
| 📡 **OSPF** | Vecindades, anuncio de redes y verificación de rutas. |
| 🖧 **DHCP** | Asignación dinámica de direcciones y servicios relacionados. |
| 🛡️ **HSRP** | Redundancia de gateway y alta disponibilidad. |
| 🚧 **ACL** | Filtrado de tráfico mediante Access Control Lists. |
| 🔐 **SSH y seguridad** | Acceso remoto seguro y endurecimiento básico de dispositivos. |
| 🧩 **Integración CCNA** | Escenarios que combinan varias tecnologías en una misma topología. |

---

## 📁 Estructura del repositorio

La siguiente estructura es una **propuesta de organización** para mantener los laboratorios ordenados a medida que el repositorio crezca. Los directorios opcionales se incorporan solo cuando el laboratorio los necesite.

```text
PyS-Network-Labs/
│
├── README.md
│
├── LAB-01/
│   ├── README.md
│   ├── LAB-01.gns3project
│   ├── topology.png
│   │
│   ├── configurations/
│   │   ├── R1.txt
│   │   ├── SW-CORE.txt
│   │   ├── SW1.txt
│   │   ├── SW2.txt
│   │   ├── SW3.txt
│   │   └── SW4.txt
│   │
│   └── evidence/
│       ├── etherchannel.png
│       ├── dhcp.png
│       └── connectivity.png
│
└── LAB-02/
    └── ...
```

Cada carpeta de laboratorio puede incluir los archivos que correspondan a su escenario: proyecto de GNS3, configuraciones, capturas, diagramas o material complementario. No es necesario crear directorios vacíos ni duplicar archivos que GNS3 ya gestione dentro del proyecto.

---

## 📝 Documentación de los laboratorios

Cada laboratorio contará con un documento propio (`README.md`) que explique qué se construyó y cómo se comprobó su funcionamiento. Según el alcance de la práctica, la documentación puede incluir:

| 🧩 Elemento | 📋 Contenido |
| :--- | :--- |
| 🎯 **Objetivo** | Qué se busca implementar o comprobar. |
| 🗺️ **Topología** | Dispositivos, conexiones y descripción del escenario. |
| ⚙️ **Tecnologías** | Protocolos, servicios y funciones utilizadas. |
| 🌐 **Direccionamiento IP** | Subredes, interfaces, gateways y asignaciones relevantes. |
| 💻 **Configuración** | Comandos y parámetros aplicados, organizados por dispositivo cuando corresponda. |
| 🔍 **Verificación** | Comandos `show`, pruebas de conectividad y validaciones realizadas. |
| 📈 **Resultados** | Comportamiento observado, incidencias y soluciones aplicadas. |

La documentación debe permitir comprender el escenario y reproducir la práctica sin asumir configuraciones que no estén descritas.

---

## 📊 Progreso del repositorio

El avance se actualizará conforme se incorporen y documenten laboratorios. Para evitar métricas sin sustento, no se muestran cantidades ni porcentajes globales hasta contar con un inventario verificable.

Los estados sugeridos para cada laboratorio son:

| 🚦 Estado | 📌 Criterio |
| :--- | :--- |
| 🗓️ **Planificado** | Tema identificado para una práctica futura. |
| 🚧 **En desarrollo** | Topología o configuración en construcción. |
| 🧪 **Verificado** | Se realizaron pruebas y se registraron los resultados. |
| ✅ **Documentado** | La documentación y los archivos correspondientes están publicados en el repositorio. |

---

## 🎯 Objetivos de aprendizaje

- 🏗️ Comprender el diseño y funcionamiento de arquitecturas de red.
- ⌨️ Configurar y administrar dispositivos Cisco en escenarios emulados.
- 🔄 Implementar y verificar protocolos, servicios y funciones de networking.
- 🛠️ Diagnosticar y resolver problemas de conectividad.
- 🔒 Aplicar buenas prácticas de acceso y seguridad en dispositivos de red.
- 📚 Desarrollar documentación técnica clara, ordenada y reproducible.

---

## 👨‍💻 Autor y propósito

**PyS-Network-Labs** es un proyecto personal de aprendizaje práctico y documentación técnica. Su propósito es registrar el proceso de estudio, implementación y verificación de tecnologías de **redes y ciberseguridad**, construyendo una referencia que pueda evolucionar junto con nuevos laboratorios y conocimientos.

---

<div align="center">

<kbd>📐 **Learn**</kbd> · <kbd>⚙️ **Configure**</kbd> · <kbd>🔍 **Verify**</kbd> · <kbd>📄 **Document**</kbd>

<br /><br />

<sub>🚀 Construido como laboratorio de aprendizaje continuo en networking y cybersecurity.</sub>

</div>