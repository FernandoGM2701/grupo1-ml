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
Desarrollar un modelo de regresión que prediga la **tasa de tamizajes positivos del mes siguiente (t+1)** a nivel departamental.

### Objetivos Específicos
- Analizar la distribución de tamizajes y tasas históricas.  
- Realizar limpieza, transformación y balanceo de datos.  
- Entrenar y evaluar modelos de regresión con métricas robustas.  
- Implementar una interfaz visual interactiva con Streamlit para interpretación.  

---

## 💡 Dominio y Motivación

- **Dominio:** Salud pública predictiva (programas de salud mental).  
- **Problema:** Dificultad en anticipar regiones o etapas con mayor incidencia de casos.  
- **Solución:** Predicción mensual basada en datos históricos y factores sociodemográficos.  
- **Palabras clave:** salud mental, predicción, aprendizaje supervisado, MINSA, regresión.  

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

| Aspecto | Descripción |
|----------|-------------|
| **Tipo** | Supervisado |
| **Algoritmo** | RandomForestRegressor |
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

1. Histograma de registros por grupo de tamizaje.  
2. Histograma de casos totales por grupo.  
3. Heatmap de correlación: tipo de tamizaje × grupo etario.  
4. Heatmap de correlación: departamento × grupo.  

Permite observar patrones espaciales, demográficos y estacionales.

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
├── notebooks/           # Análisis exploratorio y experimentos
│   └── tamizajes_presentacion_parcial.ipynb
├── .gitignore           # Archivos a excluir
├── LICENSE.txt          # Documento de licencia
└── README.md            # Documentación principal
```

---

## 🧾 Licencia

Proyecto del grupo 1 
© 2025 - Curso Machine Learning y Big Data – UNMSM.
