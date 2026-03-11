# Seguridad\_de\_la\_información

Taller\_1



\# Taller de Seguridad de la Información



Este repositorio documenta el desarrollo completo del \*\*Primer Taller de Seguridad de la Información\*\* realizado en la Fundación Universitaria Compensar. Se aplicaron herramientas de auditoría, escaneo y análisis en Kali Linux, con evidencias visuales y explicaciones detalladas por cada punto.



---



\## 🔍 Verificación de herramientas



Antes de iniciar, se verificó que todas las herramientas estuvieran instaladas correctamente. En Kali Linux vienen preinstaladas, pero se validó su presencia en el sistema.



!\[Verificación de herramientas](Imagenes/verificacion.png)



---



\## 🖥️ Punto 1: Escaneo con Nmap



\### a) Descubrimiento de hosts activos

Se ejecutó `nmap -sn 192.168.1.0/24` en una red corporativa. Se identificaron múltiples IPs activas y direcciones MAC, reconociendo fabricantes como Aruba, HP y Dell.



!\[Hosts activos](Imagenes/punto\_a.png)



\### b) Escaneo de puertos y servicios

Con `nmap -SV 127.0.0.1` se detectaron puertos abiertos y servicios activos. El escaneo agresivo con `sudo nmap -O` permitió estimar el sistema operativo.



!\[Puertos y servicios](Imagenes/punto\_b.png)



\### c) Scripts NSE para vulnerabilidades

Se aplicó `nmap --script vuln 127.0.0.1` para detectar vulnerabilidades comunes. Este tipo de escaneo es útil para identificar configuraciones inseguras.



!\[Scripts NSE](Imagenes/punto\_c.png)



\### d) Timing templates

Se compararon escaneos con `-T0` (paranoico) y `-T4` (agresivo). Los templates lentos ayudan a evadir detección, mientras que los rápidos aceleran resultados.



!\[Timing templates](Imagenes/punto\_d.png)



\### e) Puertos filtrados

Se escanearon puertos específicos con `sudo nmap -sS -p 80,443,22,25,110,143,8080`. El estado “filtered” indica bloqueo por firewall o dispositivo de seguridad.



!\[Puertos filtrados](Imagenes/punto\_e.png)



\### f) Captura de banners

Con `nmap -sV --version-intensity 9` se obtuvieron detalles precisos de versiones y configuraciones de servicios.



!\[Captura de banners](Imagenes/punto\_f.png)



\### g) Scripts para servicios web

Se levantó un servidor con `python3 -m http.server 8080` y se aplicaron scripts como `http-title`, `http-server-header`, `http-methods`.



!\[Scripts HTTP](Imagenes/punto\_g.png)



---



\## 🛡️ Punto 2: Auditoría con Lynis



Se ejecutó `sudo lynis audit system` para evaluar la seguridad local. Se analizaron advertencias, sugerencias y el índice de endurecimiento.



\### Resultados generales

\- Hardening Index: 62

\- Tests realizados: 268

\- Plugins activos: 1



!\[Resumen Lynis](Imagenes/lynis\_resumen.png)



\### Advertencias y sugerencias

Se detectaron configuraciones débiles en SSH, banners, cron, y módulos de seguridad deshabilitados.



!\[Advertencias](Imagenes/lynis\_advertencias.png)

!\[Sugerencias](Imagenes/lynis\_sugerencias.png)

!\[Recomendaciones adicionales](Imagenes/lynis\_recomendaciones.png)



---



\## 🦠 Punto 3: Detección de malware



\### a) Rootkits

Se utilizaron `chkrootkit` y `rkhunter` para buscar rootkits. Se detectaron advertencias leves y configuraciones inseguras.



!\[Rootkits chkrootkit](Imagenes/rootkit\_chkrootkit.png)

!\[Rootkits rkhunter](Imagenes/rootkit\_rkhunter.png)

!\[Rootkits adicionales](Imagenes/rootkit\_adicionales.png)



\### b) Conexiones sospechosas

Con `sudo netstat -tupan` se identificó una conexión UDP entre el host local y el servidor DHCP.



!\[Netstat conexión](Imagenes/netstat\_conexion.png)



\### c) Escaneo con ClamAV

Se actualizó la base de datos con `sudo freshclam` y se intentó escanear `/home/usuario`, aunque el directorio no existía.



!\[Actualización ClamAV](Imagenes/clamav\_update.png)

!\[Escaneo ClamAV](Imagenes/clamav\_scan.png)



---



\## 🧠 Análisis de configuración y servicios



Se revisaron configuraciones de Apache, SSH, SNMP, PHP, logging, servicios inseguros, tareas programadas, contenedores, frameworks de seguridad y bastionado del kernel.



!\[Apache y SSH](Imagenes/apache\_ssh.png)

!\[PHP y SNMP](Imagenes/php\_snmp.png)

!\[Logging y servicios](Imagenes/logging\_servicios.png)

!\[Servicios inseguros](Imagenes/servicios\_inseguros.png)

!\[Tareas y criptografía](Imagenes/tareas\_criptografia.png)

!\[Frameworks de seguridad](Imagenes/frameworks\_seguridad.png)

!\[Integridad y malware](Imagenes/integridad\_malware.png)

!\[Permisos y cron](Imagenes/permisos\_cron.png)

!\[Bastionado kernel](Imagenes/bastionado\_kernel.png)

!\[Bastionado red](Imagenes/bastionado\_red.png)



---



\## ✅ Conclusión



Este taller permitió aplicar técnicas reales de escaneo, auditoría y detección de amenazas en un entorno Kali Linux. La documentación detallada, junto con las evidencias visuales, demuestra el dominio de herramientas clave en seguridad informática y fortalece la capacidad de análisis crítico ante configuraciones inseguras.





