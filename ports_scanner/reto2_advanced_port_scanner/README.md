# Escáner de Puertos con Servicios en Python

Este es un escáner de puertos que desarrollé como parte de mi formación en ciberseguridad. A diferencia del escáner básico, este no solo detecta qué puertos están abiertos en un host, también identifica qué servicio suele trabajar en ese puerto (como HTTP, SSH, FTP, etc.).

---

## ¿Para qué sirve?

Conocer qué puertos están abiertos en un servidor o dispositivo es clave en ciberseguridad. Permite detectar posibles puntos débiles y servicios que podrían representar un riesgo si están mal configurados o innecesariamente expuestos.

Este script ayuda a:
- Detectar puertos abiertos
- Saber qué servicios están corriendo detrás
- Practicar escaneo básico con Python puro (sin Nmap u otras herramientas externas)

---

## ¿Cómo funciona?

1. Ejecuta el script: advanced_port_scanner.py
2. Ingresa una IP o dominio (como `scanme.nmap.org` o una IP local)
3. El programa escaneará los puertos del 20 al 1024 e imprimirá los que están abiertos, junto con su nombre de servicio

---

## ¿Qué aprendí con este proyecto?

- Cómo detectar puertos abiertos usando sockets en Python
- Cómo identificar el servicio asociado a un puerto usando `getservbyport`
- La importancia del tiempo de espera (`timeout`) para evitar que el programa se trabe
- Cómo estructurar un script más completo, con errores controlados y mensajes claros

Este ejercicio me ayudó a seguir desarrollando mis habilidades en redes, escaneo y automatización de tareas simples pero útiles dentro del mundo de la ciberseguridad.

---

## 👨‍💻 Autor

Javier Ávila  
Estudiante de Ingeniería en Comunicaciones y Electrónica – IPN  
Especializándome en ciberseguridad y redes
