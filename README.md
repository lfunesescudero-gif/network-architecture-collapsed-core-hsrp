# Arquitectura de Red Empresarial — Segmentación y Alta Disponibilidad

Diseño e implementación de topología corporativa Collapsed Core con redundancia física completa, segmentación por VLANs y alta disponibilidad de gateway mediante HSRP, verificada con pruebas de failover.

## Puntos clave de la implementación

- **Diseño de topología jerárquica Collapsed Core:** 2 switches L3 Core/Distribución fusionados, 2 switches L2 de Acceso y malla física completa para redundancia de enlace.
- **Segmentación en 4 VLANs (Administración, Usuarios, DMZ, OT):** Aislamiento de la red OT del tráfico IT por perfil de riesgo y criticidad operativa.
- **Trunking 802.1Q y Spanning Tree:** Configuración de enlaces troncales de punta a punta con mitigación de bucles mediante bloqueo activo de rutas redundantes.
- **Routing Inter-VLAN:** Configuración de Interfaces Virtuales de Switch (SVIs) en ambos cores con IP routing activo para interconectar los segmentos.
- **Redundancia de gateway con HSRP:** IP virtual por VLAN, asignación de prioridades y función preempt para tolerar fallas de hardware en tiempo real.
- **Prueba de alta disponibilidad:** Simulación de interrupción en el core principal, confirmación de conmutación automática Active/Standby y recuperación de servicio sin pérdida de tráfico.
- **Diagnóstico y resolución:** Corrección de inconsistencias en gateway por metodología de descarte.
