# Seguridad de la información
## Taller 1

# Taller de Seguridad de la Información

Este repositorio documenta el desarrollo completo del **Primer Taller de Seguridad de la Información** realizado en la Fundación Universitaria Compensar. Se aplicaron herramientas de auditoría, escaneo y análisis en Kali Linux, con evidencias visuales y explicaciones detalladas por cada punto.

---

## Verificación de herramientas

Antes de iniciar, se verificó que todas las herramientas estuvieran instaladas correctamente. En Kali Linux vienen preinstaladas, pero se validó su presencia en el sistema.

![Verificación de herramientas](Imagenes/Verificación.png)
![Verificación de herramientas](Imagenes/Respuesta_Verificación.png)

---

## Punto 1: Escaneo con Nmap

### a) Descubrimiento de hosts activos
Se identificaron múltiples IPs activas y direcciones MAC, reconociendo fabricantes como Aruba, HP y Dell.

![Hosts activos](Imagenes/Primer_punto_A.png)

![Hosts activos](Imagenes/Respuesta_primer_punto_A.png)

### b) Escaneo de puertos y servicios
Con `nmap -sV 127.0.0.1` se detectaron puertos abiertos y servicios activos.

![Puertos y servicios](Imagenes/primer_punto_B.png)

![Puertos y servicios](Imagenes/Respuesta_primer_punto_B.png)

### c) Scripts NSE para vulnerabilidades
Se aplicó `nmap --script vuln 127.0.0.1` para detectar vulnerabilidades comunes.

![Scripts NSE](Imagenes/primer_punto_C.png)

![Scripts NSE](Imagenes/Respuesta_primer_punto_C.png)

### d) Timing templates
Se compararon escaneos con `-T0` y `-T4`.

![Timing templates](Imagenes/primer_punto_D.png)

![Timing templates](Imagenes/Respuesta_primer_punto_D.png)

### e) Puertos filtrados
Se escanearon puertos específicos. El estado “filtered” indica bloqueo por firewall.

![Puertos filtrados](Imagenes/primer_punto_E.png)

![Puertos filtrados](Imagenes/Respuesta_primer_punto_E.png)

### f) Captura de banners
Detalles precisos de versiones y configuraciones.

![Captura de banners](Imagenes/primer_punto_F.png)

![Captura de banners](Imagenes/Respuesta_primer_punto_F.png)

### g) Scripts para servicios web
Se aplicaron scripts como `http-title`, `http-server-header`, `http-methods`.

![Scripts HTTP](Imagenes/primer_punto_G.png)

![Scripts HTTP](Imagenes/Respuesta_primer_punto_G.png)

---

## Punto 2: Auditoría con Lynis

Se ejecutó `sudo lynis audit system` para evaluar la seguridad local.

![Resumen Lynis](Imagenes/Segundo_punto.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_1.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_2.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_3.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_4.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_5.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_6.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_7.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_8.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_9.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_10.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_11.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_12.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_13.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_14.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_15.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_16.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_17.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_18.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_19.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_20.png)


![Resumen ](Imagenes/Respuesta_Segundo_punto_21.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_22.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_23.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_24.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_25.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_26.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_27.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_28.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_29.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_30.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_31.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_32.png)

![Resumen ](Imagenes/Respuesta_Segundo_punto_33.png)

---

## Punto 3: Detección de malware y análisis de integridad

En esta fase se aplicaron herramientas de búsqueda de software malicioso (Rootkits), análisis de conexiones de red y escaneo de virus para identificar posibles brechas de seguridad en el sistema Kali Linux.

### a) Búsqueda de Rootkits con chkrootkit y rkhunter

Se utilizaron los dos motores de detección más conocidos en sistemas Unix/Linux. El objetivo fue identificar binarios modificados o módulos del kernel sospechosos.

* **chkrootkit:** Durante el escaneo se detectó un mensaje de alerta en la interfaz `eth0` relacionado con un "PACKET SNIFFER". Esto es común en Kali Linux cuando herramientas de monitoreo de red (como NetworkManager) están activas.

![Resumen ](Imagenes/Tercer_punto.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_1.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_2.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_3.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_4.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_5.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_6.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_7.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_8.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_9.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_10.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_11.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_12.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_13.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_14.png)



* **rkhunter:** Se realizó una auditoría exhaustiva de los comandos del sistema. Aunque la mayoría de los binarios arrojaron un estado "OK", se identificaron advertencias en la configuración de SSH y permisos del sistema de archivos que requieren endurecimiento (Hardening).


* **Análisis detallado de Malware:** El escaneo profundo no encontró firmas de rootkits conocidos como *Slapper*, *Vampire* o *T0rn*, confirmando la integridad de los módulos del kernel analizados.



### b) Análisis de conexiones de red sospechosas

Utilizando el comando `sudo netstat -tupan`, se supervisaron las conexiones activas. Este análisis es fundamental para detectar "beacons" o comunicaciones de malware con servidores de Comando y Control (C2). Se verificó que los procesos en ejecución correspondieran a servicios autorizados por el usuario.

![Resumen ](Imagenes/Tercer_punto_B.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_B.png)

### c) Escaneo con Antivirus (ClamAV)

Se procedió a actualizar la base de datos de firmas con `freshclam` y se ejecutó un escaneo recursivo sobre el directorio personal. Esta capa de seguridad adicional permite identificar archivos infectados que no necesariamente son rootkits, sino scripts o ejecutables maliciosos.

![Resumen ](Imagenes/Tercer_punto_C.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_C_1.png)

![Resumen ](Imagenes/Respuesta_Tercer_punto_C_2.png)

---

### Análisis de hallazgos (Warnings)

Durante las pruebas se detectaron los siguientes puntos críticos que deben ser corregidos para mejorar la postura de seguridad:
1.  **SSH Root Access:** El acceso root por SSH está permitido, lo cual es una vulnerabilidad ante ataques de fuerza bruta.
2.  **Suspicious Shared Memory:** Se detectaron segmentos de memoria compartida inusuales que deben ser investigados.
3.  **File Properties:** Advertencias en `/dev/` sobre tipos de archivos sospechosos y directorios ocultos.



## Conclusión

El desarrollo del taller permitió comprender de manera práctica cómo las herramientas de auditoría y detección fortalecen la seguridad de un sistema operativo Linux. A través de Nmap, Lynis, chkrootkit, rkhunter y ClamAV se evidenció que cada fase del proceso aporta un nivel distinto de visibilidad sobre la infraestructura:

Reconocimiento de red con Nmap  
El escaneo de hosts, puertos y servicios demostró la importancia de identificar dispositivos activos y configuraciones expuestas. La detección de banners y métodos HTTP permitió reflexionar sobre cómo un atacante puede aprovechar información aparentemente básica para planear un ataque más sofisticado.

Auditoría local con Lynis  
Los resultados mostraron que, aunque el sistema no presentaba advertencias críticas, sí existían múltiples sugerencias de mejora. Esto evidencia que la seguridad no es un estado absoluto, sino un proceso continuo de endurecimiento (hardening). La obtención de un índice de seguridad intermedio refuerza la necesidad de aplicar buenas prácticas como la gestión de contraseñas, la configuración de servicios y el monitoreo constante.

Detección de malware y rootkits  
Las herramientas chkrootkit y rkhunter confirmaron que, aunque no se encontraron infecciones directas, sí se generaron advertencias que deben ser interpretadas con criterio técnico. Esto enseña que la detección de malware no siempre es concluyente y que el análisis debe complementarse con la revisión manual de procesos y configuraciones sospechosas.

Escaneo con ClamAV y análisis de conexiones  
La actualización de firmas y el intento de escaneo resaltan la importancia de mantener las bases de datos al día. El análisis de conexiones activas con netstat mostró cómo incluso procesos legítimos (como DHCP) pueden ser interpretados en clave de seguridad, ayudando a diferenciar entre tráfico normal y potencialmente malicioso.

Evaluación de configuraciones y servicios  
La revisión de Apache, SSH, SNMP, PHP y otros servicios evidenció que muchas configuraciones estaban ausentes o deshabilitadas, lo cual reduce la superficie de ataque pero también plantea la necesidad de un control más granular. El bastionado del kernel y la verificación de parámetros de red mostraron discrepancias con los valores esperados, lo que constituye un área crítica de mejora



