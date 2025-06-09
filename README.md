🧠 Análisis de Procesos Activos del Sistema
Proyecto desarrollado por Erick Quiroz y Blas Batista

📌 Descripción
Este proyecto en Python tiene como objetivo principal la recopilación y análisis de procesos activos del sistema operativo (compatible con Windows, Linux y macOS). Está diseñado con fines de monitoreo del sistema y como primer paso hacia la clasificación de procesos legítimos y potencialmente maliciosos.

Utilizando las bibliotecas de Python, se genera un dataset detallado con múltiples métricas de procesos, que luego es analizado estadísticamente para identificar patrones de comportamiento.

🎯 Objetivo
Aplicar conocimientos prácticos sobre:

La creación de datasets desde el sistema operativo.

El análisis estadístico de procesos activos.

La visualización de correlaciones para identificar relaciones entre métricas clave.

⚙️ Cómo Funciona
El proyecto se compone de dos scripts principales:

process_data_collector.py
📥 Función: Recopila información detallada sobre todos los procesos activos.

⏱ Monitoreo: Realiza 4 capturas (snapshots) de procesos, cada una separada por 15 segundos.

📊 Datos Recopilados:

PID, nombre del proceso, ruta del ejecutable

Usuario propietario, uso de CPU y RAM

Número de hilos, estado, tiempo de creación

Argumentos de línea de comandos

Conexiones de red, archivos abiertos

Lectura/escritura de E/S, porcentaje de memoria utilizada

📄 Salida: Archivo CSV llamado process_data_multi_snapshot_raw.csv.

process_data_analyzer.py
📈 Función: Carga y analiza el dataset generado.

🔍 Análisis:

Estadísticas básicas: media, mediana, moda, desviación estándar.

Matriz de correlación entre variables numéricas.

Visualización con mapa de calor (seaborn).

📁 Entrada: process_data_multi_snapshot_raw.csv.

🧰 Requisitos
Asegúrate de tener Python 3.x y las siguientes bibliotecas instaladas:

bash
Copy
Edit
pip install psutil pandas matplotlib seaborn
▶️ Uso
Clona este repositorio o descarga los archivos.

Ejecuta el script de recopilación de procesos:

bash
Copy
Edit
python process_data_collector.py
Esto generará el archivo process_data_multi_snapshot_raw.csv.

Luego, ejecuta el script de análisis:

bash
Copy
Edit
python process_data_analyzer.py
Verás en consola las estadísticas y un mapa de calor con la correlación entre métricas de procesos.

🔐 Consideraciones de Privacidad
El archivo CSV generado puede contener información sensible como nombres de usuario, rutas de programas y procesos en ejecución. Aunque no incluye credenciales ni datos directamente explotables, te recomendamos anonimizar o filtrar los datos si piensas compartirlos públicamente.

