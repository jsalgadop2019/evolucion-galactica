# 🚀 Análisis de Escalabilidad y Rendimiento HPC

Este repositorio contiene las herramientas de análisis y visualización para evaluar la escalabilidad y el rendimiento de la ejecución de un modelo numérico implementado con el protocolo **MPI (Message Passing Interface)** en entornos de Computación de Alto Rendimiento (HPC).

El análisis se centra en las métricas clave de la paralelización: **Tiempo de Ejecución**, **Speedup**, y **Eficiencia**.

---

## 📂 Archivo Principal de Análisis

| Archivo | Tipo | Descripción |
| :--- | :--- | :--- |
| **`Evolución_Galáctica_Análisis_de_Rendimiento_del_Modelo.ipynb`** | Jupyter Notebook (`.ipynb`) | Contiene el código Python completo para ingestar los datos, realizar los cálculos de **Speedup** y **Eficiencia**, y generar gráficas interactivas con estilo oscuro (`Dark Mode`) y controles de visibilidad (**`ipywidgets`**). |

---

## 💻 Despliegue y Uso

Para el despliegue interactivo y la ejecución de este análisis, la plataforma más sencilla y recomendada es **Google Colab**.

### 1. Requerimiento de Datos (`Datos.csv`)

El análisis requiere que el archivo de datos de rendimiento se cargue en el entorno de ejecución.

* **Nombre Requerido:** **`Datos.csv`**
* **Contenido:** El archivo debe tener una columna de procesos (`proceso`) y columnas de tiempo de ejecución ($T_{EJ}$) para diferentes tamaños de problema fijos (ej: `1K`, `2K`, `4K`, etc.).

### 2. Pasos para el Despliegue en Google Colab

1.  **Abrir el Notebook:** Sube el archivo `Evolución_Galáctica_Análisis_de_Rendimiento_del_Modelo.ipynb` a tu Google Drive y ábrelo con Google Colab.
2.  **Cargar `Datos.csv`:** Utiliza el panel de archivos de Colab para cargar el archivo **`Datos.csv`** a la raíz de la sesión.
3.  **Ejecución:** Ejecuta las celdas del Notebook de forma secuencial. Las gráficas (Tiempo, Speedup, Eficiencia) se generarán con sus respectivos controles interactivos.

---

## 📈 Análisis Cubierto

El notebook incluye las siguientes visualizaciones y diagnósticos:

* **Tiempo de Ejecución ($T_{EJ}$):** Gráfica interactiva log-log con separación por tamaño de problema.
* **Speedup ($S_P$):** Gráfica interactiva de la ganancia de rendimiento, comparada con la curva ideal ($S_P = P$).
* **Eficiencia ($E_P$):** Gráfica interactiva para evaluar la sobrecarga de comunicación, comparada con la curva ideal ($E_P = 1$). El eje Y está configurado en escala logarítmica (0.10 a 10).
* **Diagnóstico de Escalabilidad Fuerte:** Análisis automatizado de la Eficiencia en el máximo número de procesos. 
