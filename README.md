Nombre del Proyecto: Análisis de Procesos Activos del Sistema
Descripción del Proyecto
Este proyecto de Python se enfoca en la recopilación y análisis de datos de procesos activos en un sistema operativo (Windows, Linux, macOS) para fines de monitoreo y un estudio inicial sobre la clasificación de procesos legítimos y potencialmente maliciosos. Utiliza las capacidades de Python para interactuar con el sistema, generar un conjunto de datos (dataset) y aplicar técnicas de análisis estadístico.

Objetivo
Aplicar los conocimientos sobre la creación de datasets utilizando Python y el análisis de estos, centrándose en métricas clave de los procesos del sistema para identificar patrones de comportamiento.

Cómo Funciona
El proyecto consta de dos scripts principales:

process_data_collector.py:

Función: Recopila información detallada sobre todos los procesos que se están ejecutando en el sistema.
Detalles: Toma múltiples "capturas" (snapshots) de los procesos. Por defecto, realiza 4 capturas cada 15 segundos, sumando un minuto de monitoreo.
Datos Recopilados: Incluye el PID, nombre del proceso, ruta del ejecutable, usuario, uso de CPU y memoria (en MB), número de hilos, estado, tiempo de creación, argumentos de línea de comandos, así como datos más avanzados como el número de conexiones de red, número de archivos abiertos, bytes de lectura/escritura de E/S y porcentaje de memoria RAM utilizada por el proceso.
Salida: Genera un archivo CSV llamado process_data_multi_snapshot_raw.csv con todos los datos recopilados.
process_data_analyzer.py:

Función: Carga y analiza el dataset generado por el script anterior.
Análisis:
Estadísticas Básicas: Calcula la media, mediana, moda y desviación estándar para todas las variables numéricas de los procesos (uso de CPU, memoria, hilos, conexiones, E/S, etc.).
Correlación entre Variables: Genera una matriz de correlación para identificar relaciones lineales entre las variables numéricas.
Visualización: Muestra la matriz de correlación como un mapa de calor utilizando seaborn para una interpretación más sencilla.
Entrada: Utiliza el archivo process_data_multi_snapshot_raw.csv.

