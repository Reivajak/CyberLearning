# 🛡️ Honeypot Simple en Python

Este proyecto lo desarrollé como parte de mi formación en ciberseguridad. Es un honeypot simple: un servidor falso que simula ofrecer un servicio "atractivo" y registra cualquier intento de conexión. Me ayudó a entender mejor cómo funcionan los sockets, la comunicación en red, y la importancia del registro de actividad.

---

## 1️⃣ ¿Qué hace este honeypot?

- Escucha conexiones entrantes en el puerto **2222**.
- Simula un servidor con un nombre llamativo: `Servidor tarjetas_clientes_2025`.
- Registra cada intento de conexión, incluyendo:
  - Dirección IP del visitante
  - Puerto remoto
  - Fecha y hora
  - Datos enviados (si los hay)
- Guarda toda la información en un archivo `.csv` llamado `registros_honeypot.csv`.

---

## 2️⃣ ¿Cómo lo probé?

- Ejecuté el honeypot en una máquina virtual con Linux.
- Me conecté desde:
  - La **misma máquina** usando `netcat`.
  - Una **MacBook conectada a la misma red local**.
- Las conexiones fueron detectadas correctamente y registradas tanto en consola como en el archivo `.csv`.

---

## 3️⃣ ¿Cómo se ejecuta?

1. Asegúrate de tener Python 3 instalado.
2. Descarga el archivo `honeypot_simple.py`.
3. Abre una terminal y ejecuta:     python3 honeypot_simple.py
4. Desde otra terminal o computadora en la misma red, conéctate con:    nc <IP-del-servidor> 2222
   Ejemplo: nc 192.168.1.93 2222
5. Escribe algo como `Hola` y presiona Enter.
6. Verás la conexión reflejada en la consola y guardada en el archivo `.csv`.

---

## 4️⃣ Ejemplo de salida en consola

```
[+] Servidor tarjetas_clientes_2025 activo en el puerto 2222
[*] Esperando conexiones...

[!] Conexión detectada de 192.168.1.75:54089 a las 2025-06-10 18:22:37
    ↳ Datos recibidos: Hola
```

---

## 5️⃣ Ejemplo de contenido del archivo `registros_honeypot.csv`

```
fecha_hora,ip,puerto,dato_recibido
2025-06-10 18:22:37,192.168.1.75,54089,Hola
2025-06-10 18:22:40,192.168.1.75,54090,[Sin datos enviados]
```

---

## 6️⃣ ¿Qué aprendí?

- Crear un servidor TCP en Python usando sockets.
- Detectar y registrar conexiones en red.
- Guardar registros en formato `.csv` de forma estructurada.
- Simular un entorno de monitoreo básico, similar al de un analista SOC.

---

## 7️⃣ Posibles mejoras futuras

- Mostrar estadísticas por IP (reintentos, volumen).
- Visualizar conexiones en gráficos (con matplotlib).
- Simular múltiples servicios falsos en distintos puertos.
- Alertas en tiempo real por terminal o notificaciones.

---

## 🧑‍💻 Autor

Javier Ávila Andrade

Estudiante de Ingeniería en Comunicaciones y Electrónica – IPN

Apasionado por la ciberseguridad y la automatización