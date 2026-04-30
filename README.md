# Inteligencia Artificial - Trabajo Práctico

Este repositorio contiene un trabajo práctico de Inteligencia Artificial enfocado en **análisis de sentimientos** utilizando el **Large Movie Review Dataset v1.0** (IMDB Reviews).

## 📁 Estructura del Repositorio

```
inteligencia_artificial_tp/
├── 01_EDA.ipynb                 # Exploratory Data Analysis (EDA)
│                                # Análisis exploratorio del dataset
├── 02_log_reg.ipynb             # Modelo de Regresión Logística
│                                # Implementación y evaluación
├── 03_Baseline.ipynb            # Modelo Baseline
│                                # Comparación de rendimiento
├── imdb_reviews.csv             # Dataset IMDB en formato CSV
│                                # Contiene reviews y sentimientos
├── paper_files/                 # Archivos de referencia y recursos
│                                # Información del dataset original
├── LICENSE                      # Licencia MIT
└── README.md                    # Este archivo
```

## 📊 Contenido de los Notebooks

### 1️⃣ **01_EDA.ipynb** - Análisis Exploratorio
- Carga y exploración del dataset
- Análisis estadístico de las reseñas
- Distribución de sentimientos
- Visualizaciones de datos

### 2️⃣ **02_log_reg.ipynb** - Regresión Logística
- Preprocesamiento de texto
- Vectorización de features (TF-IDF)
- Entrenamiento del modelo de Regresión Logística
- Evaluación y métricas de rendimiento

### 3️⃣ **03_Baseline.ipynb** - Modelo Baseline
- Implementación de modelo base
- Comparación de rendimiento
- Análisis de resultados

## 📊 Descripción del Dataset

El **Large Movie Review Dataset v1.0** (IMDB Reviews) es un benchmark estándar para clasificación de sentimientos que contiene:

- **50,000 reseñas etiquetadas**: 25,000 para entrenamiento y 25,000 para prueba
- **50,000 documentos sin etiquetar**: para aprendizaje no supervisado
- **Distribución balanceada**: 25k reseñas positivas y 25k negativas

### Criterios de Etiquetado

- **Reseña positiva**: puntuación ≥ 7 de 10
- **Reseña negativa**: puntuación ≤ 4 de 10
- Las reseñas con calificaciones neutrales (5-6) están excluidas del conjunto etiquetado

### Restricciones del Dataset

- Máximo 30 reseñas por película
- Los conjuntos de entrenamiento y prueba contienen películas disjuntas
- En el conjunto no supervisado hay un número igual de reseñas con puntuación > 5 y ≤ 5

## 🛠️ Tecnologías Utilizadas

- **Python** 3.x
- **Jupyter Notebook** para desarrollo interactivo
- **Pandas** para manipulación de datos
- **Scikit-learn** para modelos de ML
- **NLTK/Spacy** para procesamiento de lenguaje natural
- **Matplotlib/Seaborn** para visualizaciones

## 📚 Cómo Usar

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/valentinarias-dtsc/inteligencia_artificial_tp.git
   cd inteligencia_artificial_tp
   ```

2. **Instalar dependencias**
   ```bash
   pip install -r requirements.txt  # Si existe
   # o instalar manualmente:
   pip install pandas scikit-learn nltk jupyter matplotlib seaborn
   ```

3. **Ejecutar los notebooks**
   ```bash
   jupyter notebook
   ```

4. **Abrir en orden**: 01_EDA → 02_log_reg → 03_Baseline

## 📚 Referencias

Para más información sobre el dataset y formato LIBSVM:
- [LIBSVM Format](http://www.csie.ntu.edu.tw/~cjlin/libsvm/)
- Maas et al., 2011: "Learning Word Vectors for Sentiment Analysis" (ACL-HLT 2011)

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).

---

**Nota**: Este repositorio es parte de un trabajo práctico de Inteligencia Artificial utilizando el Large Movie Review Dataset como benchmark para análisis de sentimientos.
