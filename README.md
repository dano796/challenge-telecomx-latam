# 📡 Challenge TelecomX LATAM

Este proyecto forma parte del **Challenge de la Formación: Aprendiendo a hacer ETL G8-ONE**, y tiene como objetivo aplicar técnicas de **ETL (Extracción, Transformación y Carga)** y **análisis exploratorio de datos (EDA)** para investigar la evasión de clientes en TelecomX, una empresa de telecomunicaciones.

<br>

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gE3WVbHdnjiO1dZfTdqc6uqGy7gNcrmz?usp=sharing)

## Descripción

El objetivo principal de este challenge es **analizar los datos de los clientes de TelecomX** para identificar los factores que contribuyen a la alta tasa de cancelación (churn). A través de la extracción de datos desde una API, su transformación y análisis, se busca proporcionar **insights estratégicos** que permitan al equipo de ciencia de datos desarrollar modelos predictivos y estrategias para mejorar la retención de clientes.

<br>

## Funcionalidades

- **Extracción de datos:** Obtención de datos desde una API en formato JSON y conversión a un DataFrame para su análisis.
- **Transformación de datos:** Limpieza y preparación de los datos, incluyendo normalización y manejo de valores nulos o inconsistentes.
- **Análisis exploratorio de datos (EDA):** Identificación de patrones y correlaciones entre variables como antigüedad, servicios contratados, cargos diarios y cancelación (churn).
- **Visualización de datos:** Creación de gráficos (boxplots, matrices de correlación, distribuciones) para ilustrar tendencias y relaciones clave.
- **Generación de insights:** Conclusiones sobre los factores que influyen en la evasión de clientes, como costos diarios elevados y baja vinculación con los servicios.

<br>

## Uso

**1. Clonar el repositorio:**

   ```bash
   git clone https://github.com/dano796/challenge-telecomx-latam.git
   ```

**2. Ve a Google Colab.**

**3. Haz clic en Archivo > Subir notebook y selecciona el archivo descargado.**

<br>

## Análisis Realizados

**1. Matriz de Correlación:** Evaluación de la relación entre variables como antigüedad del cliente, cantidad de servicios contratados y cargos diarios estimados con la variable de churn.

**2. Cargos Diarios Estimados por churn:** Análisis comparativo de los costos diarios entre clientes que cancelan y los que permanecen, utilizando boxplots.

**3. Distribución de Servicios por churn:** Estudio de la relación entre la cantidad de servicios contratados y la probabilidad de cancelación.

**4. Informe de Insights:** Identificación de factores clave que contribuyen a la evasión, como costos diarios elevados y baja vinculación con los servicios, junto con recomendaciones estratégicas.

<br>

## Ejemplo de Código

```python
import pandas as pd
import requests

# Extracción de datos desde la API
api = 'https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json'
res = requests.get(api)
df = res.json()

# Normalización del JSON a DataFrame
data = pd.json_normalize(df, sep='_')
data.sample(5)
```

<br>

## Conclusiones

El análisis revela que:
- Los clientes con **mayor antigüedad** y **más servicios contratados** tienen una menor probabilidad de cancelar.
- Los **cargos diarios elevados** están asociados con una mayor tasa de churn, sugiriendo una percepción de menor valor.
- Los clientes con **pocos servicios contratados** son más propensos a cancelar, mientras que aquellos con 5 o más servicios muestran mayor fidelidad.

**Recomendaciones estratégicas:**
- Implementar **paquetes de servicios a precios reducidos** para aumentar la vinculación de los clientes.
- Ofrecer **beneficios progresivos según la antigüedad** para fomentar la retención a largo plazo.
- Revisar la estructura de precios para reducir la percepción de costos elevados, especialmente en los cargos diarios.

---

### Practicando ETL y Análisis Exploratorio de Datos: Challenge TelecomX LATAM

### Challenge de la Formación: Aprendiendo a hacer ETL G8-ONE

### Daniel Ortiz Aristizábal
