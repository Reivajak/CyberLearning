
#  Honeypot Simple en Python + Analizador de Conexiones

Este proyecto fue desarrollado como parte de mi formación en ciberseguridad. Consiste en un **honeypot simple** que simula un servidor falso y registra intentos de conexión, y un **script de análisis en Python** que procesa esos registros para extraer información útil.

---

##  ¿Qué hace este proyecto?

### 🔸 `honeypot_simple.py`
- Escucha conexiones en el puerto **2222**.
- Simula un servidor con el nombre `tarjetas_clientes_2025`.
- Registra:
  - IP del visitante
  - Puerto remoto
  - Fecha y hora
  - Datos enviados
- Guarda los datos en `registros_honeypot.csv`.

### 🔸 `analizador_registros.py`
- Lee los registros del archivo `.csv`.
- Muestra:
  - Número total de conexiones registradas
  - Conexiones que enviaron datos
  - Cantidad de intentos por IP
  - Puertos remotos usados por los clientes

---

##  Cómo ejecutarlo

### 1. Ejecutar el honeypot:  python3 honeypot_simple.py

- Desde otra terminal o equipo en la red local, conéctate con:

    nc <IP-del-servidor> 2222

    Ejemplo:  nc 192.168.1.93 2222


### 2. Ejecutar el analizador:  python3 analizador_registros.py


---

##  Ejemplo de salida (honeypot)

```
[+] Servidor tarjetas_clientes_2025 activo en el puerto 2222
[*] Esperando conexiones...
[!] Conexión detectada de 192.168.1.75:54089 a las 2025-06-10 18:22:37
    ↳ Datos recibidos: Hola
```

---

##  Ejemplo de contenido del archivo `registros_honeypot.csv`

```
fecha_hora,ip,puerto,dato_recibido
2025-06-10 18:22:37,192.168.1.75,54089,Hola
2025-06-10 18:22:40,192.168.1.75,54090,[Sin datos enviados]
```

---


##  Ejemplo de salida (analizador)

```
 Registros cargados: 15 filas

 Conexiones con datos enviados: 5

 Conexiones por dirección IP:
192.168.1.75    12
192.168.1.88     3

 Puertos remotos usados:
54089    4
54090    3
...
```

---

##  Lo que aprendí

- Uso de `sockets` para crear servidores TCP.
- Registro estructurado de conexiones en `.csv`.
- Análisis de eventos con `pandas`.
- Primer acercamiento al monitoreo de actividad en red.

---

##  Posibles mejoras

- Visualizaciones con `matplotlib` o `seaborn`.
- Exportar resultados como PDF o gráficos.
- Automatizar alertas por múltiples intentos sospechosos.
- Implementar múltiples honeypots con diferentes puertos y respuestas.

---

## 👨‍💻 Autor

**Javier Ávila Andrade**  
Estudiante de Ingeniería en Comunicaciones y Electrónica – IPN  
Enfocado en ciberseguridad, automatización y análisis de datos.
