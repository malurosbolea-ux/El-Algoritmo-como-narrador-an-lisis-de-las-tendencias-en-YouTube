# 📊 El algoritmo como narrador: análisis de YouTube Trending

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)

**Análisis de 220,000+ videos trending para entender cómo el algoritmo de YouTube construye narrativas culturales**


</div>

---

## 🎯 Sobre el proyecto

Este proyecto analiza más de 220,000 videos trending de YouTube en 10 países para responder: **¿Es el algoritmo de YouTube un narrador neutral o tiene preferencias claras?**

**Respuesta:** NO. El algoritmo tiene sesgos claros y medibles.

---

## 🔍 Hallazgos principales

🎵 **Hegemonía del entretenimiento**  
Music y Entertainment representan el **45% del contenido trending**

😊 **Sesgo hacia lo positivo**  
**65% de títulos virales son positivos** vs 10% negativos

🎓 **Education: calidad sin visibilidad**  
Lidera en engagement (4.3%) pero solo es 2% del trending

📈 **Correlación universal**  
Relación consistente vistas-likes en todas las escalas (10K a 100M)

🌍 **Desigualdad geográfica**  
Canadá y Alemania lideran en vistas promedio

---

## 📊 Visualizaciones del proyecto

Este análisis incluye **6 visualizaciones profesionales** (300 DPI, alta calidad):

1. **[Correlación vistas-likes](visualizations/grafico1_correlacion_vistas_likes.png)** - Escala logarítmica mostrando relación universal
2. **[Distribución de categorías](visualizations/grafico2_distribucion_categorias.png)** - Music y Entertainment dominan el 45%
3. **[Engagement por categoría](visualizations/grafico3_engagement_categorias.png)** - Education lidera con 4.3%
4. **[Vistas por país](visualizations/grafico4_vistas_por_pais.png)** - Análisis geográfico de viralidad
5. **[Análisis de sentimiento](visualizations/grafico5_analisis_sentimiento.png)** - 65% positivo, 25% neutral, 10% negativo
6. **[Comparación de métricas](visualizations/grafico6_metricas_comparadas.png)** - Vistas, likes y comentarios por categoría

> 📁 Todas las visualizaciones disponibles en [`visualizations/`](visualizations/)

---

## 🛠️ Stack tecnológico

**Análisis de datos y ML**
- Python 3.x, Pandas, NumPy
- Scikit-learn (Modelado de temas con LDA)
- Transformers (Análisis de sentimiento con RoBERTa)

**Procesamiento de lenguaje**
- NLTK para preprocesamiento
- langdetect para detección automática de idioma

**Visualización**
- Plotly (gráficos interactivos)
- Matplotlib & Seaborn (visualizaciones estáticas)

---

## 📊 Dataset

| Característica | Detalle |
|---------------|---------|
| **Origen** | [Kaggle YouTube Trending Dataset](https://www.kaggle.com/datasets/datasnaek/youtube-new) |
| **Tamaño** | 220,000+ videos (tras limpieza de 12,570 duplicados) |
| **Países** | 10 países: US, GB, CA, DE, FR, MX, KR, JP, IN, BR |
| **Variables** | views, likes, comments, category, title, tags, country |

> ⚠️ Los CSV originales (~400 MB) NO están en este repo. Ver [`data/README.md`](data/) para instrucciones de descarga.

---

## 🔬 Metodología

**1. Consolidación de datos**  
Unificación de CSVs de 10 países en un DataFrame global con trazabilidad geográfica

**2. Limpieza de datos**  
Eliminación de 12,570 duplicados | Gestión de nulos | Preservación de outliers (fenómenos virales)

**3. Preprocesamiento NLP**  
Detección de idioma + filtrado de stopwords multilingüe + tokenización

**4. Modelado de temas**  
LDA para identificar 10 sub-narrativas principales

**5. Análisis de sentimiento**  
RoBERTa sobre 1,000 títulos: 65% positivo | 25% neutral | 10% negativo

---

## 📁 Estructura del repositorio

```
youtube-trending-analysis/
├── README.md                          # Este archivo
├── notebooks/
│   └── analisis_youtube.ipynb         # Análisis completo
├── visualizations/
│   └── *.png                          # 6 gráficos (300 DPI)
├── docs/
│   └── El_algoritmo_como_narrador.pdf # Documento completo
└── data/
    └── README.md                       # Cómo descargar datos
```

---

## 🚀 Replicar este análisis

```bash
# 1. Clonar repositorio
git clone https://github.com/malurosbolea-ux/youtube-trending-analysis.git
cd youtube-trending-analysis

# 2. Instalar dependencias
pip install pandas numpy scikit-learn matplotlib seaborn plotly nltk transformers langdetect

# 3. Descargar datos
# Visita: https://www.kaggle.com/datasets/datasnaek/youtube-new
# Coloca los CSV en data/

# 4. Ejecutar análisis
jupyter notebook notebooks/analisis_youtube.ipynb
```

---

## 💡 Conclusión

El algoritmo de YouTube **NO es neutral**:

| Sesgo | Evidencia |
|-------|-----------|
| 🎭 Temático | Music + Entertainment = 45% del trending |
| 😊 Emocional | 65% positivo vs 10% negativo |
| 🏆 Jerárquico | Music/Entertainment > Gaming/Comedy > Education |
| 🌍 Geográfico | Mercados anglófonos dominan |

**Implicación:** El algoritmo construye una cultura global dominada por entretenimiento positivo, donde otros contenidos requieren mayor esfuerzo para ganar visibilidad.

---

## 📖 Documentación completa

Para leer el análisis completo con metodología detallada y discusión de resultados:

[El_algoritmo_como_narrador_YOUTUBE.pdf](https://github.com/user-attachments/files/23592962/El_algoritmo_como_narrador_YOUTUBE.pdf)

---

## 👩‍💻 Sobre mí

**María Luisa Ros Bolea**

Data Science & AI | Digital Communication  
Graduada en Comunicación Digital, CEU San Pablo  
Máster en Big Data e Inteligencia Artificial

Especializada en la intersección entre comunicación digital y ciencia de datos.  
Experiencia en Community Management, Content Creation y Growth Marketing.

**Stack técnico:** Python, Pandas, Scikit-learn, NLP, Machine Learning, Data Visualization  
**Idiomas:** Español (nativo), Inglés (C1), Francés (B1)

### 📫 Conecta conmigo

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maría-luisa-ros-bolea-400780160/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/malurosbolea-ux)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF6B6B?style=for-the-badge&logo=canva&logoColor=white)](https://marialuisarosboleaportfolio.my.canva.site/porfolio-profesional-mar-a-luisa-ros-bolea-actualizado)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:malurosbolea@gmail.com)

📍 Madrid, España  
📧 malurosbolea@gmail.com  
📱 +34 692 892 183

---

<div align="center">

**¿Te gusta este proyecto? ¡Dale una ⭐!**

*Noviembre 2025*

</div>







