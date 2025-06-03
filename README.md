# Port Scanner en Python

Este proyecto escanea los puertos de un host (IP o dominio) usando Python puro. Permite identificar qué puertos están abiertos en un rango determinado (20-1024).

## ¿Para qué sirve?

Los escáneres de puertos son herramientas comunes en ciberseguridad ofensiva y defensiva para:

- Detectar servicios inseguros o abiertos por error
- Evaluar la exposición de un sistema en red

## Cómo usarlo

1. Ejecuta el script: port_scanner.py
2. Ingresa una IP o dominio cuando lo pida (por ejemplo: `google.com` o `scanme.nmap.org`).

## Qué aprendí

- Cómo funcionan los puertos y los sockets
- Cómo detectar servicios abiertos en red
- Principios básicos de un escaneo de red seguro

Con este proyecto entendí conceptos clave de redes y ciberseguridad relacionados con los puertos, los protocolos de comunicación, y el uso de sockets en Python. Aprendí que cada servicio (como un servidor web, SSH o FTP) se comunica a través de un puerto específico, y que escanear estos puertos permite identificar qué servicios están activos en una máquina.

También aprendí a utilizar la biblioteca estándar de Python socket para abrir conexiones TCP y detectar si un puerto está abierto o cerrado, lo que es esencial en tareas de análisis de vulnerabilidades.

Además, comprendí la importancia de limitar el tiempo de espera (timeout) para evitar que el script se quede congelado y cómo automatizar un escaneo de puertos sin depender de herramientas externas como Nmap.

Este ejercicio me enseñó a estructurar un script limpio, documentado y funcional, y me dio una base para futuros proyectos más avanzados como escaneos con detección de servicios o ataques de fuerza bruta controlados.

