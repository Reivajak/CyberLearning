# nmap_auto_scan.py – Escaneo automatizado de red con Nmap

Este script en Python realiza un escaneo automático de red usando Nmap y genera estadísticas útiles de los dispositivos conectados. Desarrollé este proyecto combinando escaneo activo, registro en CSV y visualización de datos.

## ¿Qué hace?

- Escanea la red local con `nmap -sn` para detectar dispositivos activos.
- Obtiene IP, dirección MAC y fabricante (si está disponible).
- Guarda los resultados automáticamente en un archivo CSV con nombre único.
- Muestra en consola:
  - Una tabla limpia de dispositivos detectados.
  - Estadísticas por fabricante en texto.
- Genera una gráfica circular con la distribución por fabricante.

## Archivos generados

- `logs_scan_YYYYMMDD_HHMMSS.csv`: contiene los resultados del escaneo.
- La gráfica se muestra en tiempo real al ejecutar el script.

##  Cómo ejecutarlo

1. Activa tu entorno virtual:  
   `source venv_nmap/bin/activate`

2. Corre el script:  
   `python3 nmap_auto_scan.py`

3. Listo. Verás los resultados en consola y la gráfica al final.

## Tecnologías usadas

- Python 3.13  
- Nmap  
- pandas  
- matplotlib  

## ✍️ Autor

Javier Ávila Andrade  
Estudiante de Ingeniería en Comunicaciones y Electrónica – IPN  
Apasionado por la ciberseguridad, la automatización y el aprendizaje constante.
