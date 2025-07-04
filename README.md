# Proyecto ML: Clasificación de Ritmo Cardíaco con SVM

## Objetivo

El objetivo de este proyecto es **clasificar registros de ritmo cardíaco** (Normal vs. AFib) a partir de características extraídas de señales ECG, utilizando modelos de machine learning clásicos como SVM. El flujo incluye exploración de datos, visualización, entrenamiento y evaluación de modelos.

---

## Estructura del repositorio

```
Project_ML/
│
├── data/
|   |__Datos_Proyecto
|       |_ ACÁ LOS DATOS .MAT Y .HEA
│   └── ecg_rr_features_curado.csv      # 
│
├── notebooks/
│   ├── etapa1_explorar_y_visualizar.ipynb   # Análisis exploratorio y visualización de datos
│   └── etapa2_modelo_basico.ipynb           # Entrenamiento y evaluación de modelo SVM
│
└── README.md
```

---

## Descripción de los datos y procesamiento

- **Fuente de datos:** Registros ECG en formato WFDB (`.mat` y `.hea`)
- **Procesamiento:** Extracción de características RR utilizando NeuroKit2 
- **Muestras procesadas:** 54 registros (27 Normal, 27 AFib)
- **Características extraídas:**
  - `mean_rr`: Promedio del intervalo RR (tiempo entre latidos)
  - `std_rr`: Desviación estándar del intervalo RR
  - `skew_rr`: Asimetría de la distribución de intervalos RR
  - `kurt_rr`: Curtosis de la distribución de intervalos RR

---

## Requisitos

- Python 3.8 o superior
- Recomendado: entorno virtual (venv, conda, etc.)

### Instalación de dependencias

```bash
pip install pandas numpy scipy scikit-learn matplotlib wfdb neurokit2 seaborn

## Ejecución

### 1. Análisis exploratorio y visualización

Abre y ejecuta el notebook:

```
notebooks/etapa1_explorar_y_visualizar.ipynb
```

Aquí encontrarás:
- Estadísticas descriptivas
- Distribución de clases
- Visualización de variables por clase
- Identificación de variables más relevantes

### 2. Entrenamiento y evaluación del modelo

Abre y ejecuta el notebook:

```
notebooks/etapa2_modelo_basico.ipynb
```

Incluye:
- Separación de datos en entrenamiento y prueba
- Estandarización de variables
- Entrenamiento de un modelo SVM
- Evaluación con métricas (accuracy, F1, precision, recall)
- Visualización de la matriz de confusión
- Análisis e interpretación de resultados

---

## Instrucciones rápidas

1. Clona el repositorio o descarga los archivos
2. Instala las dependencias
3. Abre los notebooks en Jupyter o VS Code
4. Ejecuta las celdas en orden

---

## Resultados esperados

- El modelo SVM logra una precisión general de aproximadamente 0.83
- El recall y la precisión para la clase AFib también son altos (~0.83 y ~0.87 respectivamente)
- El análisis muestra que el modelo es bueno detectando casos normales y tiene buena sensibilidad para AFib, aunque el tamaño de muestra es limitado

---

## Notas adicionales

- El dataset es pequeño y entregado por el profesor, por lo que los resultados pueden variar si se amplía la muestra
- Puedes modificar los notebooks para probar otros modelos o ajustar hiperparámetros
- Si tienes dudas sobre el flujo, revisa los comentarios y análisis incluidos en cada notebook

---

## Autor

Proyecto realizado para fines educativos en Machine Learning