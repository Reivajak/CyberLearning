# Escáner de Puertos con Hilos en Python 

Este proyecto es la tercera versión de un escáner de puertos que he ido mejorando paso a paso.  
En esta versión, optimicé el rendimiento usando **hilos (multithreading)** para escanear muchos puertos al mismo tiempo, lo que lo hace mucho más rápido que las versiones anteriores.

---

## ¿Qué hace este script?

- Escanea los puertos del 20 al 1024 en una IP o dominio
- Muestra cuáles están abiertos
- Intenta identificar qué servicio suele usar cada puerto (como HTTP, FTP, SSH, etc.)
- Todo esto de forma **paralela**, gracias a los hilos

---

## ¿Qué aprendí?

- Cómo funciona el uso de hilos en Python con `threading`
- Cómo hacer que el escaneo de puertos sea mucho más eficiente
- Cómo capturar e identificar servicios comunes en los puertos detectados
- Lo importante que es manejar bien los tiempos de espera (`timeout`) para evitar cuelgues
- Y cómo documentar un script para que sea entendible y reutilizable

---

## ¿Cómo usarlo?

1. Abre tu terminal
2. Ejecuta el script: threaded_port_scanner.py
3. Escribe la IP o dominio cuando lo pida (por ejemplo: scanme.nmap.org)
4. Verás en tiempo real qué puertos están abiertos y qué servicio hay detrás

👨‍💻 Autor

Javier Ávila
Estudiante de Ingeniería en Comunicaciones y Electrónica – IPN
Apasionado por la ciberseguridad y la automatización