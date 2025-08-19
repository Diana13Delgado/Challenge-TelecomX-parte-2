# 📊 Challenge TelecomX - Analisis de Evasión de clientes - Parte 2.

Este proyecto analiza la **cancelación de clientes (churn)** en la empresa TelecomX, utilizando técnicas de **machine learning** y análisis exploratorio de datos.  

---

## 🚀 Objetivo
Identificar los principales factores que influyen en la cancelación de clientes y construir modelos predictivos que permitan anticipar el churn, con el fin de diseñar **estrategias de retención** efectivas.

---

## 📂 Flujo del proyecto

1. **Limpieza de datos**
   - Eliminación de valores nulos y vacíos.
   - Estandarización de valores como `"No internet service"` → `"No"`.
   - Conversión de variables categóricas a formato numérico (One-Hot Encoding).

2. **Análisis Exploratorio (EDA)**
   - Distribución de cancelación (churn vs no churn).
   - Boxplots y countplots para explorar relación entre:
     - Tenure × Cancelación.
       <img width="687" height="462" alt="image" src="https://github.com/user-attachments/assets/5b0faf05-aa88-404a-943d-f1143a925627" />

     - Total Charges × Cancelación.
     - <img width="716" height="466" alt="image" src="https://github.com/user-attachments/assets/787e0bdd-7f8d-4c04-b3c2-c47e153c9725" />
     - Contract × Cancelación.
     -  <img width="709" height="470" alt="image" src="https://github.com/user-attachments/assets/8bf21533-b2c0-44f3-a25b-7b86d39c8e14" />

   - Matriz de correlación para identificar variables más relacionadas con churn.
<img width="469" height="272" alt="image" src="https://github.com/user-attachments/assets/3c983a5c-1e02-4f89-9d38-46034a2308ac" />     <img width="473" height="265" alt="image" src="https://github.com/user-attachments/assets/25250bab-03d1-4ef3-9a00-5cb5994a12bd" />



3. **Preprocesamiento**
   - División de datos en **80% entrenamiento / 20% prueba**.
   - Balanceo de clases con **SMOTE** para manejar el desbalance entre clientes que cancelan y los que permanecen.

4. **Modelos aplicados**
   - **Regresión Logística** (con normalización).
   - **Random Forest** (sin normalización).
   - Ajuste de hiperparámetros (`max_depth`, `n_estimators`, `min_samples_split`, `min_samples_leaf`).

5. **Evaluación de modelos**
   - Métricas: Accuracy, Precision, Recall, F1-Score, Matriz de confusión.
   - Comparación de desempeño entre Logistic Regression y Random Forest.

6. **Interpretación de variables**
   - **Regresión Logística:** análisis de coeficientes.
   - **Random Forest:** análisis de importancia de variables (feature importance).

7. **Informe final**
     - Comparación de métricas.
     - Gráficos de importancia de variables.
     - Boxplots de Tenure y Total Charges.
     - Countplot de tipo de contrato.
     - Estrategias de retención basadas en los resultados.

---

## 📈 Principales hallazgos

- **Factores que aumentan el churn:**
  - Internet Service: **Fiber optic**.
  - Gasto total alto (Total Charges).
  - Método de pago: **Electronic check**.
  - Facturación electrónica (Paperless Billing).
  - Clientes Senior Citizens.

- **Factores que reducen el churn:**
  - **Mayor antigüedad (tenure)**.
  - Contratos de largo plazo (1 o 2 años).
  - Servicios adicionales como **TechSupport** y **OnlineSecurity**.
  - Clientes con dependientes en su perfil.

---

## 🛠 Estrategias de retención recomendadas

1. **Programas de lealtad por antigüedad.**
2. **Incentivar contratos de largo plazo** (con descuentos y beneficios).
3. **Atención especial a clientes de alto valor** (fibra óptica, cargos altos).
4. **Mejorar la experiencia de pago electrónico**, reduciendo errores de *electronic check*.
5. **Campañas dirigidas a senior citizens** con soporte y comunicación personalizada.
6. **Promover activamente servicios de soporte** (TechSupport y OnlineSecurity).

---

## 📊 Resultados de los modelos

| Modelo               | Accuracy | Recall (Churn) | F1 (Churn) |
|----------------------|----------|----------------|------------|
| Logistic Regression  | 0.74     | 0.79           | 0.62       |
| Random Forest        | 0.76     | 0.77           | 0.63       |

- **Conclusión:** Random Forest ofrece mejor equilibrio entre precisión y recall, siendo el modelo recomendado para producción.  
- La Regresión Logística aporta mayor interpretabilidad de los factores.

---

## 📑 Archivos entregables

- `Challenge_TelecomX_parte_2.ipynb`: contiene todo el flujo del análisis.
- Código en Python con:
  - Limpieza y preprocesamiento.
  - Entrenamiento y evaluación de modelos.
  - Visualizaciones y reportes.

---

## 🖥 Tecnologías utilizadas

- **Python** (pandas, numpy, scikit-learn, imbalanced-learn, matplotlib, seaborn).
- **Machine Learning:** Logistic Regression, Random Forest.
- **Visualización:** Matplotlib, Seaborn.

---

## 👨‍💻 Autor

Diana Delgado — Proyecto **Challenge TelecomX parte 2**
