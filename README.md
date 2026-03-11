# Seguridad de la información
## Taller 1

# Taller de Seguridad de la Información

Este repositorio documenta el desarrollo completo del **Primer Taller de Seguridad de la Información** realizado en la Fundación Universitaria Compensar. Se aplicaron herramientas de auditoría, escaneo y análisis en Kali Linux, con evidencias visuales y explicaciones detalladas por cada punto.

---

## Verificación de herramientas

Antes de iniciar, se verificó que todas las herramientas estuvieran instaladas correctamente. En Kali Linux vienen preinstaladas, pero se validó su presencia en el sistema.

![Verificación de herramientas](Imagenes/Verificación.png)
[Verificación de herramientas](Imagenes/Respuesta_Verificación.png)

---

## Punto 1: Escaneo con Nmap

### a) Descubrimiento de hosts activos
Se identificaron múltiples IPs activas y direcciones MAC, reconociendo fabricantes como Aruba, HP y Dell.

![Hosts activos](Imagenes/Respuesta_Tercer_punto_C_1.png)

### b) Escaneo de puertos y servicios
Con `nmap -sV 127.0.0.1` se detectaron puertos abiertos y servicios activos.

![Puertos y servicios](Imagenes/Respuesta_Tercer_punto_C_2.png)

### c) Scripts NSE para vulnerabilidades
Se aplicó `nmap --script vuln 127.0.0.1` para detectar vulnerabilidades comunes.

![Scripts NSE](Imagenes/Respuesta_Verificación.png)

### d) Timing templates
Se compararon escaneos con `-T0` y `-T4`.

![Timing templates](Imagenes/Segundo_punto.png)

### e) Puertos filtrados
Se escanearon puertos específicos. El estado “filtered” indica bloqueo por firewall.

![Puertos filtrados](Imagenes/Tercer_punto.png)

### f) Captura de banners
Detalles precisos de versiones y configuraciones.

![Captura de banners](Imagenes/Tercer_punto_B.png)

### g) Scripts para servicios web
Se aplicaron scripts como `http-title`, `http-server-header`, `http-methods`.

![Scripts HTTP](Imagenes/Tercer_punto_C.png)

---

## Punto 2: Auditoría con Lynis

Se ejecutó `sudo lynis audit system` para evaluar la seguridad local.

![Resumen Lynis](Imagenes/Respuesta_Verificación.png)

---

## Conclusión

Este taller permitió aplicar técnicas reales de escaneo, auditoría y detección de amenazas en un entorno Kali Linux.



