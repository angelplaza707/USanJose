# 🧠 Proyecto Final – Análisis de Bancarización de Beneficiarios de Programas Sociales 🇨🇴

**Autor:** _[Tu nombre completo]_  
**Diplomado:** Ciencia de Datos y Machine Learning  
**IDE:** Visual Studio Code + extensión Jupyter  
**Fuente de datos:** [Datos Abiertos de Colombia – Prosperidad Social](https://www.datos.gov.co/resource/xfif-myr2.json)

---

## 🎯 Objetivo del Proyecto

Desarrollar un modelo de **clasificación supervisada** para predecir si un beneficiario de un programa social del gobierno colombiano se encuentra **bancarizado** o no, utilizando información pública del portal **Datos Abiertos de Colombia**.

El proyecto implementa todo el ciclo de vida del análisis de datos en un **solo notebook**:
1. Obtención de datos desde la API pública.
2. Limpieza y transformación de datos.
3. Análisis exploratorio y visualización.
4. Entrenamiento y evaluación de modelos (Árbol de Decisión y Random Forest).
5. Generación de conclusiones e interpretación.

---

## 🧩 Fuente de Datos

**API:** `https://www.datos.gov.co/resource/xfif-myr2.json`  
**Entidad:** Departamento de Prosperidad Social  

**Principales columnas del dataset:**
- `bancarizado` (variable objetivo)  
- `genero`, `nivelescolaridad`, `discapacidad`, `etnia`, `rangoedad`  
- `tipoasignacionbeneficio`, `tipopoblacion`, `estadobeneficiario`  
- `cantidaddebeneficiarios`, `fechainscripcionbeneficiario`, `fechaultimobeneficioasignado`

---

## 🧰 Tecnologías Utilizadas

- **Python 3.10+**
- **Pandas**, **NumPy** → limpieza y manipulación de datos  
- **Matplotlib**, **Seaborn** → visualización  
- **Scikit-learn** → modelado y evaluación  
- **Requests** → conexión a API pública  
- **VS Code + Jupyter Notebook** → desarrollo y ejecución

---

## 🧮 Metodología General

### 1️⃣ Ingesta y Preparación
Se realizó la descarga paginada del dataset desde la API y su almacenamiento en formato `.parquet`.  
Se aplicaron limpiezas, normalización de nombres y detección automática de tipos (`int`, `datetime`, `object`).

### 2️⃣ Análisis Exploratorio
- Distribuciones de variables numéricas y categóricas.  
- Conteos por departamento y municipio.  
- Correlaciones y tendencias temporales.  
- Identificación de variables relevantes.

### 3️⃣ Modelado Predictivo
Se entrenaron dos modelos:
| Modelo | Accuracy | Precision | Recall | F1 Score |
|--------|-----------|-----------|---------|-----------|
| Árbol de Decisión | _ver notebook_ | | | |
| Random Forest | _ver notebook_ | | | |

➡️ El **Random Forest** mostró un F1 Score superior, demostrando mejor equilibrio entre precisión y recall.

### 4️⃣ Visualización de Resultados
- Matrices de confusión comparativas.  
- Gráfico de importancia de variables.  
- Tabla resumen de métricas.

---

## 📊 Conclusiones

- El modelo confirma que la **bancarización** está fuertemente influenciada por variables socioeducativas.  
- Beneficiarios con **mayor nivel de escolaridad y beneficios recurrentes** presentan más probabilidades de estar bancarizados.  
- El **Random Forest** fue el modelo con mejor rendimiento global y estabilidad.  
- Se sugiere utilizar estos hallazgos para orientar estrategias de **inclusión financiera** dentro de los programas sociales.

---

## 🗂️ Estructura del Repositorio

