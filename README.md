# 🧠 Modelo Predictivo de Tasa de Positividad Mensual en Tamizajes de Salud Mental – MINSA Perú

### 👨‍🎓 Integrantes del Grupo
- **Urtecho Quezada, Brandon Lee**
- **Mantilla Canedo, Melanie**
- **Vásquez Cauper, Alex**
- **Gutierrez Mejía, Fernando Alberto**
- **Huacausi Cahuana, Ciprian**

📅 **Fecha:** 25/10/2025  
🏫 **Universidad Nacional Mayor de San Marcos – Escuela de Ingeniería de Software**

---

## 🧩 Descripción General del Proyecto

Este proyecto aplica **Machine Learning supervisado (regresión)** para **predecir la tasa mensual de tamizajes positivos en salud mental** a nivel **departamental**, usando datos abiertos del **Ministerio de Salud del Perú (MINSA)**.

La finalidad es apoyar la **gestión preventiva de recursos** y **la detección temprana** en programas de salud mental pública, anticipando variaciones en los indicadores de positividad mediante un modelo predictivo desplegable con **Streamlit**.

---

## 🎯 Objetivos

### Objetivo General
  Desarrollar un modelo de aprendizaje supervisado que prediga la tasa de tamizajes positivos en un mes dado a nivel departamental en los programas de salud mental del MINSA, empleando variables sociodemográficas, temporales y de grupo etario. El sistema busca apoyar la planificación preventiva de recursos y personal en los centros de salud, anticipando variaciones en la incidencia de casos.
  
### Dominio o proceso que se busca mejorar
  Gestión de recursos y detección temprana en programas de salud mental pública.

### Palabras clave
- Salud mental.  
- Predicción
- Aprendizaje supervisado
- MINSA
- Regresión

### Justificación rápida

  Permite identificar de forma anticipada aumentos en las tasas de casos positivos, ayudando al MINSA a tomar decisiones informadas sobre campañas y estrategias preventivas regionales.


### Objetivos Específicos
- Analizar la distribución de tamizajes y tasas históricas.  
- Realizar limpieza, transformación y balanceo de datos.  
- Entrenar y evaluar modelos de regresión con métricas robustas.  
- Implementar una interfaz visual interactiva con Streamlit para interpretación.  

---

## 📊 Dataset

- **Origen:** Portal de Datos Abiertos del MINSA.  
- **Formato:** CSV tabular (~20k registros).  
- **Cobertura:** Datos agregados por **departamento, sexo, grupo etario y diagnóstico**.  
- **Variable objetivo:**  
  - `tasa_positivos (%)` o número proyectado de casos positivos.  
  - Tipo: **Numérico continuo (regresión)**.  

### Variables principales
| Categoría | Variables |
|------------|------------|
| Temporales | Año, NroMes |
| Ubicación | Ubigeo, Departamento, Provincia, Distrito |
| Demográficas | Sexo, Etapa |
| Servicio | GrupoTamizaje, DetalleTamizaje |
| Medición | Casos (conteos) |

---

## ⚙️ Modelo de Machine Learning

Tipo de Machine Learning: Supervisado
Tipo de modelo: Regresión (modelo base: Random Forest Regressor)
Campo de ML: Medicina predictiva / Salud pública
Herramientas empleadas: Python (Google Colab), Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn.


| Aspecto | Descripción |
|----------|-------------|
| **Tipo** | Supervisado |
| **Algoritmo** | Regresión (RandomForestRegressor) |
| **Campo** | Medicina predictiva / salud pública |
| **Lenguaje** | Python |
| **Entorno** | Google Colab / Jupyter Notebook |

### Librerías utilizadas
- **pandas**, **NumPy** → limpieza y manipulación.  
- **scikit-learn** → modelado, métricas, SMOTE.  
- **matplotlib**, **seaborn** → visualización y EDA.  
- **Streamlit** → despliegue web interactivo.

---

## 📈 Análisis Exploratorio (EDA)

1. Histograma: distribución de registro por grupo de tamizaje.
2. Histograma: suma total de casos por grupo de tamizaje.
3. Heatmap de correlación: casos por tipo de tamizaje y grupo.
4. Heatmap de correlación: casos por departamento y grupo. 

---

## 🧮 Evaluación del Modelo

| Métrica | Descripción | Justificación |
|----------|--------------|----------------|
| **MAE** | Error absoluto medio | Mide la desviación promedio entre valores reales y predichos |
| **R²** | Coeficiente de determinación | Evalúa qué porcentaje de la varianza es explicado por el modelo |

> Estas métricas son las más adecuadas para **regresión predictiva**, permitiendo medir precisión y estabilidad.

---

## 📦 Estructura del Repositorio

```
├── data/                # Dataset
│   └── tamizajes.csv
├── models/              # Modelo
│   └── modelo_final.pkl
├── notebooks/           # Análisis exploratorio y experimentos
│   └── tamizajes_presentacion_parcial.ipynb
├── .gitattributes       # Reglas para el LFS
├── .gitignore           # Archivos a excluir
├── LICENSE.txt          # Documento de licencia
└── README.md            # Documentación principal
```

---


## 🚀 Guía de Despliegue Completa en Google Colab

Puedes ejecutar este proyecto sin instalar nada en tu computadora siguiendo estos pasos:

---

### Paso 1. Abrir el Notebook en Google Colab

1. Ingresar a la ruta dentro del repositorio:
```
notebooks/tamizajes_presentacion_parcial.ipynb
```

2. Presionar el botón **Abrir en Colab**  
Si no aparece el botón, puedes cargarlo manualmente desde:
https://colab.research.google.com

---

### Paso 2. Subir el dataset requerido a Colab

En la barra lateral izquierda:

📁 Icono de carpeta → **Subir archivo**

Seleccionar el archivo:
```
data/tamizajes.csv
```

Este archivo contiene los registros utilizados para realizar las predicciones.

---

### Paso 3. Instalar dependencias en Colab

Ejecutar esta celda al inicio del notebook:

```python
!pip install pandas numpy scikit-learn seaborn matplotlib joblib
```

---

### Paso 4. Ejecutar todas las celdas del notebook

En el menú seleccionar:
```
Entorno de ejecución → Ejecutar todo
```

✔ Se cargará el dataset  
✔ Se aplicará el procesamiento  
✔ Se generarán predicciones  
✔ Se mostrarán gráficos y métricas  


## 🧾 Licencia

Proyecto del grupo 1 
© 2025 - Curso Machine Learning y Big Data – UNMSM.
