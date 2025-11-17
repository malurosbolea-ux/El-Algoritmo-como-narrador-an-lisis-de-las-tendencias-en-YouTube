# 📊 El algoritmo como narrador: análisis de YouTube Trending

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly)

**Análisis de 220,000+ videos trending para entender cómo el algoritmo de YouTube construye narrativas culturales**

</div>

---

## 🎯 Sobre el proyecto

Este proyecto analiza más de 220,000 videos trending de YouTube en 10 países para responder una pregunta clave: **¿Es el algoritmo de YouTube un narrador neutral o tiene preferencias claras?**

### Hallazgos principales

- 🎵 **Music y Entertainment representan el 45%** del contenido trending - evidencia empírica de sesgo algorítmico
- 😊 **El 65% de títulos virales son positivos** vs solo 10% negativos - el algoritmo prefiere narrativas optimistas  
- 🎓 **Education lidera en engagement** (~4.3%) pero solo es 2% del trending - calidad sobre cantidad
- 📈 **Correlación universal** entre vistas y likes en todas las escalas (10K a 100M vistas)
- 🌍 **Desigualdad geográfica** - mercados anglófonos dominan en viralidad

---

## 📈 Visualizaciones clave

### Correlación vistas vs likes: la dinámica universal

![Correlación vistas-likes](visualizations/grafico1_correlacion_vistas_likes.png)

**Conclusión:** Existe una correlación positiva consistente entre vistas y likes en todas las escalas, desde videos de nicho hasta fenómenos masivos. La escala logarítmica revela que este patrón es fractal.

---

### La hegemonía de la cultura pop

<div align="center">
<img src="visualizations/grafico2_distribucion_categorias.png" width="700">
</div>

**Conclusión:** Music y Entertainment no solo dominan en viralidad, sino también en frecuencia. El algoritmo tiene un sesgo claro hacia el entretenimiento de masas.

---

### Education: alto engagement, baja visibilidad

<div align="center">
<img src="visualizations/grafico3_engagement_categorias.png" width="700">
</div>

**Conclusión:** Education lidera en proporción likes/vistas, pero representa solo el 2% del contenido trending. Las audiencias están comprometidas, pero el algoritmo no prioriza esta categoría.

---

### Geografía de la viralidad

<div align="center">
<img src="visualizations/grafico4_vistas_por_pais.png" width="700">
</div>

**Conclusión:** Canadá y Alemania lideran en vistas promedio. Los mercados anglófonos y europeos tienen ventaja estructural en alcance viral.

---

### El sesgo emocional del algoritmo

<div align="center">
<img src="visualizations/grafico5_analisis_sentimiento.png" width="800">
</div>

**Conclusión:** El algoritmo favorece narrativas positivas en proporción 6.5:1 sobre negativas. YouTube prefiere contar historias optimistas.

---

### Comparación multidimensional

<div align="center">
<img src="visualizations/grafico6_metricas_comparadas.png" width="800">
</div>

**Conclusión:** Comedy lidera en las tres métricas clave, mientras que Entertainment y Music muestran consumo más pasivo pese a su dominio numérico.

---

## 🛠️ Stack tecnológico

### Análisis de datos
- **Python 3.x** - Lenguaje principal
- **Pandas** - Manipulación de datos (220K+ registros)
- **NumPy** - Computación numérica

### Machine Learning & NLP
- **Scikit-learn** - Modelado de temas (LDA)
- **Transformers** - Análisis de sentimiento (RoBERTa)
- **NLTK** - Preprocesamiento de texto
- **langdetect** - Detección automática de idioma

### Visualización
- **Plotly** - Gráficos interactivos
- **Matplotlib & Seaborn** - Visualizaciones estáticas

---

## 📊 Dataset

- **Origen:** [Kaggle YouTube Trending Dataset](https://www.kaggle.com/datasets/datasnaek/youtube-new)
- **Tamaño:** 220,000+ videos (tras limpieza)
- **Países:** US, GB, CA, DE, FR, MX, KR, JP, IN, BR
- **Período:** Videos trending durante varios meses
- **Variables:** views, likes, comments, category, title, tags, country

---

## 🔬 Metodología

### 1. Consolidación de datos
Unificación de archivos CSV de 10 países en un DataFrame global con trazabilidad geográfica.

### 2. Limpieza de datos
- Eliminación de 12,570 duplicados exactos
- Gestión de valores nulos (preservación de datos)
- **Preservación de outliers** (fenómenos virales)
- Visualización con escala logarítmica

### 3. Preprocesamiento NLP
- Detección automática de idioma (langdetect)
- Filtrado de stopwords multilingüe
- Tokenización y limpieza de texto

### 4. Modelado de temas
- Algoritmo: Latent Dirichlet Allocation (LDA)
- Identificación de 10 sub-narrativas principales
- Refinamiento metodológico para dataset multilingüe

### 5. Análisis de sentimiento
- Modelo: CardiffNLP twitter-roberta-base-sentiment
- Muestra: 1,000 títulos aleatorios
- Clasificación: Positivo (65%), Neutral (25%), Negativo (10%)

---

## 📁 Estructura del proyecto

```
youtube-trending-analysis/
│
├── README.md                          # Este archivo
├── notebooks/
│   └── analisis_youtube.ipynb         # Análisis completo en Jupyter
├── visualizations/
│   ├── grafico1_correlacion_vistas_likes.png
│   ├── grafico2_distribucion_categorias.png
│   ├── grafico3_engagement_categorias.png
│   ├── grafico4_vistas_por_pais.png
│   ├── grafico5_analisis_sentimiento.png
│   └── grafico6_metricas_comparadas.png
├── docs/
│   └── El_algoritmo_como_narrador.pdf  # Documento completo
└── data/
    └── README.md                       # Instrucciones para descargar datos
```

---

## 🚀 Cómo replicar este análisis

### 1. Clonar el repositorio
```bash
git clone https://github.com/TU_USUARIO/youtube-trending-analysis.git
cd youtube-trending-analysis
```

### 2. Instalar dependencias
```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly nltk transformers langdetect
```

### 3. Descargar los datos
Visita [Kaggle YouTube Trending Dataset](https://www.kaggle.com/datasets/datasnaek/youtube-new) y descarga los archivos CSV. Colócalos en la carpeta `data/`.

### 4. Ejecutar el análisis
Abre `notebooks/analisis_youtube.ipynb` en Jupyter y ejecuta las celdas secuencialmente.

---

## 💡 Conclusión principal

El algoritmo de YouTube **NO es neutral**. Actúa como un narrador con preferencias claras:

✅ Favorece entretenimiento sobre educación (45% vs 2%)  
✅ Prefiere narrativas positivas sobre negativas (65% vs 10%)  
✅ Mantiene jerarquías de categorías (Music/Entertainment > Gaming/Comedy > resto)  
✅ Da ventaja a mercados anglófonos y europeos  
✅ Permite pluralidad, pero con visibilidad desigual  

El "algoritmo como narrador" construye una **cultura global dominada por el entretenimiento positivo**, donde otras formas de contenido requieren mayor esfuerzo para ganar visibilidad.

---

## 📖 Documentación completa

Para leer el análisis completo con metodología detallada y discusión de resultados:

📄 **[Descargar documento completo (PDF)](docs/El_algoritmo_como_narrador.pdf)**

---

## 👩‍💻 Sobre mí

**María Luisa Ros Bolea **

Data Science & AI | Digital Communication  
Máster en Big Data e Inteligencia Artificial - CEU San Pablo

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maría-luisa-ros-bolea-400780160/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/malurosbolea-ux)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://marialuisarosboleaportfolio.my.canva.site/porfolio-profesional-mar-a-luisa-ros-bolea-actualizado)


---


<div align="center">

**Si este proyecto te resulta útil, ¡considera darle una ⭐!**

*Construido con 💜 y mucho Python*

</div>
