# 🧠 Análisis de Procesos Activos del Sistema

> Proyecto desarrollado por **Erick Quiroz**, **Blas Batista** y... posiblemente **Gemini** 👀

---

## 📘 Descripción

Este proyecto en Python permite la **recopilación y análisis estadístico de procesos activos** del sistema operativo (compatible con **Windows**, **Linux** y **macOS**). 

Está diseñado como una herramienta educativa y de monitoreo inicial, con el potencial de extenderse hacia la **detección de comportamiento anómalo o malicioso** mediante técnicas de Machine Learning.

---

## 🎯 Objetivo

- Construir un dataset de procesos del sistema operativo utilizando Python.
- Analizar dicho dataset mediante estadísticas descriptivas y correlaciones.
- Visualizar relaciones entre variables para detectar patrones de uso de recursos.

---

## 🧩 Estructura del Proyecto

El proyecto se compone de dos scripts principales:

### 📍 `process_data_collector.py`

> 🔍 Recopila múltiples snapshots de los procesos activos.

- Captura datos cada 15 segundos, 4 veces (1 minuto total).
- Guarda la información en `process_data_multi_snapshot_raw.csv`.

#### ✅ Datos Recopilados:

- PID, nombre, ruta del ejecutable
- Usuario, CPU, RAM (MB), %RAM
- Número de hilos, estado del proceso
- Tiempo de inicio, argumentos de línea de comandos
- Archivos abiertos, conexiones de red
- Bytes leídos/escritos por E/S

---

### 📍 `process_data_analyzer.py`

> 📊 Carga y analiza el dataset generado.

#### Análisis Realizado:

- Estadísticas: media, mediana, moda, desviación estándar
- Matriz de correlación entre métricas numéricas
- Visualización: mapa de calor con `seaborn`

---

## 🖼️ Capturas de Ejemplo

### 🔥 Mapa de Calor de Correlaciones

> Visualización generada con `seaborn` a partir del CSV

![Mapa de Calor de Correlaciones](images/heatmap_example.png)

---

### 📟 Terminal Ejecutando el Análisis

![Salida de la terminal](images/terminal_output.png)

---

## 🧪 Requisitos

Asegúrate de tener **Python 3.x** instalado y luego ejecuta:

```bash
pip install psutil pandas matplotlib seaborn
