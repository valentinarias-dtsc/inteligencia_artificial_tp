# Inteligencia Artificial - Trabajo Práctico

Este repositorio contiene un trabajo práctico de Inteligencia Artificial enfocado en análisis de sentimientos utilizando el **Large Movie Review Dataset v1.0**.

## 📁 Estructura del Repositorio

```
inteligencia_artificial_tp/
├── train/                          # Conjunto de datos de entrenamiento
│   ├── pos/                        # Reseñas positivas (25k archivos)
│   │   └── [id]_[rating].txt       # Archivos de texto con nombre: id_rating.txt
│   ├── neg/                        # Reseñas negativas (25k archivos)
│   │   └── [id]_[rating].txt       # Ejemplo: test/pos/200_8.txt
│   └── unsup/                      # Documentos sin etiquetar (50k archivos)
│       └── [id]_0.txt              # Sin información de rating
│
├── test/                           # Conjunto de datos de prueba
│   ├── pos/                        # Reseñas positivas
│   ├── neg/                        # Reseñas negativas
│   └── [archivos .feat]            # Características en formato LIBSVM
│
├── paper_files/                    # Archivos de referencia y vocabulario
│   ├── imdb.vocab                  # Vocabulario de tokens (índices de características)
│   ├── imdbEr.txt                  # Expected rating por token
│   ├── urls_pos.txt                # URLs de reseñas positivas
│   ├── urls_neg.txt                # URLs de reseñas negativas
│   └── urls_unsup.txt              # URLs de documentos sin etiquetar
│
└── README.md                       # Este archivo
```

## 📊 Descripción del Dataset

El **Large Movie Review Dataset v1.0** es un benchmark estándar para clasificación de sentimientos que contiene:

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

## 📄 Descripción de Archivos

### Archivos de Reseñas
Formato: `[id]_[rating].txt`
- `id`: Identificador único de la reseña
- `rating`: Puntuación en escala de 1-10

**Ejemplo**: `test/pos/200_8.txt` → reseña positiva de prueba con ID 200 y calificación 8/10

### Características LIBSVM (.feat)
Formato de vector disperso ASCII para datos etiquetados. Cada línea contiene:
- Índice de característica: cantidad (ej: `0:7` significa la palabra en índice 0 aparece 7 veces)
- Los índices se corresponden con tokens en `imdb.vocab`

### Archivos de Referencia
- **imdb.vocab**: Mapeo de índices a tokens del vocabulario
- **imdbEr.txt**: Puntuación esperada de polaridad por token
- **urls_[pos|neg|unsup].txt**: URLs de IMDb (línea N contiene URL de la reseña con ID N)

## 📚 Referencias

Para más información sobre el dataset y formato LIBSVM:
- [LIBSVM Format](http://www.csie.ntu.edu.tw/~cjlin/libsvm/)
- Maas et al., 2011: "Learning Word Vectors for Sentiment Analysis" (ACL-HLT 2011)

## 👤 Contacto

Para consultas sobre el dataset original:
- Andrew Maas: amaas@cs.stanford.edu

---

**Nota**: Este repositorio es parte de un trabajo práctico de Inteligencia Artificial utilizando el Large Movie Review Dataset como benchmark para análisis de sentimientos.
