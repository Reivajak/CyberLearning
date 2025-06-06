# Port Scanner en Python

Este proyecto es un escáner de puertos sencillo hecho con Python. Su objetivo es detectar qué puertos están abiertos en una IP o dominio dentro de un rango (del 20 al 1024). Está pensado como una práctica básica para entender cómo funcionan los puertos y los servicios que corren en ellos.

---

## ¿Para qué sirve?

Los escáneres de puertos se usan mucho en ciberseguridad, tanto para defender como para encontrar vulnerabilidades. Este tipo de herramienta ayuda a:

- Detectar servicios que están abiertos sin necesidad o por error.
- Saber qué tan expuesto está un sistema en red.
- Prepararse para análisis más avanzados en entornos reales.

---

## Cómo usarlo

1. Ejecuta el script `port_scanner.py`.
2. Ingresa una IP o dominio cuando se te pida (por ejemplo: `google.com` o `scanme.nmap.org`).
3. El programa te mostrará qué puertos están abiertos en ese host.

---

## ¿Qué aprendí?

Con este proyecto aprendí varias cosas importantes sobre redes y ciberseguridad:

- Entendí mejor qué son los puertos y cómo los servicios como SSH, HTTP o FTP se comunican a través de ellos.
- Aprendí a usar la librería `socket` de Python para abrir conexiones TCP y saber si un puerto está abierto o cerrado.
- Me di cuenta de lo importante que es usar un tiempo de espera (`timeout`) para que el programa no se quede congelado.
- También vi cómo automatizar este tipo de tareas sin necesidad de usar herramientas externas como Nmap.

Además, me ayudó a mejorar la forma en que escribo y documento mis scripts, y me dejó una buena base para seguir aprendiendo cosas más avanzadas como detección de servicios o pruebas de fuerza bruta en un entorno controlado.

---


