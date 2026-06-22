![Data Science](https://img.shields.io/badge/Data%20Science-Project-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Classification-orange)
![Spotify](https://img.shields.io/badge/Dataset-Spotify-green)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-brightgreen)
![Gradio](https://img.shields.io/badge/UI-Gradio-red)
# Predicción de Popularidad musical en Spotify mediante un análisis de su información y Machine Learning

## Descripción general
Este proyecto analiza datos obtenidos de la plataforma Spotify, analiza sus comportamientos y entiende patrones en ellos con el fin de poder aplicar un algoritmo de Machine Learning el cual pueda predecir si una canción podrá alcanzar el éxito mediático o no, basado únicamente en el entendimiento de sus características musicales, información de sus compositores y métricas adicionales de Spotify


## Tabla de contenidos
1. [Resultados destacados](#resultados-destacados)
2. [Objetivos](#objetivos)
3. [Tecnologías utilizadas](#tecnologías-utilizadas)
4. [Instalación y configuración](#instalación-y-configuración)
5. [Arquitectura](#arquitectura)
6. [Dataset](#dataset)
7. [Metodología](#metodolog%C3%ADa)
8. [Primeros resultados](#primeros-resultados)
9. [Resultados finales y conclusiones](#resultados-finales-y-conclusiones)
10. [Implementación de interfaz del modelo](#implementaci%C3%B3n-de-interfaz-del-modelo)
11. [Estructura del repositorio](#estructura-del-repositorio)
12. [Autores](#autores)


## Resultados destacados

- Dataset integrado con más de 200,000 canciones.
- Accuracy final: ~80%.
- MCC final: ~0.55.
- Variables más importantes:
  - Popularidad promedio de artistas.
  - Seguidores promedio.
  - Seguidores de playlists.
- Aplicación interactiva desarrollada con Gradio.

## Objetivos
1. Analizar las relaciones existentes entre las características técnicas de las canciones.

2. Identificar patrones y tendencias musicales presentes en las canciones y artistas del conjunto de datos. 

3. Determinar qué características musicales influyen en la popularidad de una canción.

4. Analizar la relación entre los artistas y el desempeño de sus canciones.

5. Construir modelos predictivos para estimar la popularidad o éxito potencial de una canción a partir de sus características musicales.

### Preguntas a resolver

#### Popularidad
* ¿La popularidad de una canción está relacionada con su nivel de danceability?
* ¿Las canciones más energéticas tienden a ser más populares?
* ¿Existe una combinación de características que favorezca una mayor popularidad?
* ¿La duración de una canción influye en su popularidad?
* ¿La popularidad depende más del artista o de las características musicales?
* ¿Qué factores musicales influyen más en la popularidad de una canción?
* ¿Existen perfiles musicales característicos de los artistas más exitosos?

#### Características musicales
* ¿Existen grupos naturales de canciones con características similares?
* ¿Qué características presentan las correlaciones más fuertes?
* ¿Las canciones con alta danceability también suelen tener alta energy?
* ¿Existe relación entre valence (positividad emocional) y popularidad?
* ¿Qué variables explican mejor la variabilidad musical del conjunto de datos?
* ¿Es posible identificar géneros o estilos únicamente a partir de características acústicas?

#### Artistas
* ¿Los artistas mantienen un estilo musical consistente entre sus canciones?
* ¿Existen artistas que se distingan claramente por ciertas características musicales?
* ¿Qué artistas presentan mayor diversidad musical?
* ¿Los artistas populares producen canciones con características similares?

#### Predicciones
* ¿Es posible predecir la popularidad de una canción usando únicamente sus características musicales?
* ¿Qué variables tienen mayor importancia en el modelo predictivo?
* ¿Qué algoritmo ofrece mejor desempeño para estimar la popularidad?
* ¿Se puede clasificar una canción como "éxito" o "no éxito" utilizando aprendizaje automático?
* ¿Puede un modelo de Machine Learning predecir el éxito comercial de una canción antes de su lanzamiento?

## Tecnologías utilizadas

El desarrollo del proyecto se realizó utilizando herramientas orientadas al análisis de datos, aprendizaje automático y desarrollo de aplicaciones interactivas.

| Tecnología       | Uso dentro del proyecto                                                               |
| ---------------- | ------------------------------------------------------------------------------------- |
| Python 3.12| Lenguaje principal para análisis, modelado y desarrollo de la aplicación.|
| Pandas | Limpieza, transformación y manipulación de datos.|
| NumPy | Operaciones matemáticas y procesamiento numérico.|
| Matplotlib | Visualización de datos y generación de gráficos exploratorios.|
| Seaborn | Análisis estadístico visual y exploración de relaciones entre variables.|
| Scikit-Learn | Implementación de algoritmos de Machine Learning y evaluación de modelos.|
| XGBoost | Desarrollo de modelos basados en Gradient Boosting.|
| UMAP| Reducción de dimensionalidad y visualización de agrupamientos presentes en los datos.|
| Gradio | Construcción de la interfaz gráfica para realizar predicciones.|
| Joblib | Serialización y almacenamiento de modelos entrenados.|
| Jupyter Notebook | Desarrollo de análisis exploratorios y experimentación.|
| Mermaid | Elaboración de diagramas de arquitectura y flujo de trabajo.|
| Git y GitHub | Control de versiones y gestión del repositorio.|
|||


## Instalación y configuración

### Requisitos previos

Antes de ejecutar el proyecto es necesario contar con:

* Python 3.12 o superior.
* Git instalado.
* Acceso a una terminal o consola de comandos.

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd Data_Analisis_Spotify
```

### 2. Crear un entorno virtual 

```bash
python -m venv .venv
```

Activar el entorno virtual:

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

### 3. Instalar dependencias

Instalar todas las bibliotecas necesarias mediante:

```bash
pip install -r requirements.txt
```

### 4. Preparar los datasets

Dentro de la carpeta `Dataset/` se encuentran los archivos comprimidos utilizados por el proyecto.

Es necesario descomprimir los siguientes archivos:

* [artists.csv.zip](Data_Analisis_Spotify\Dataset\artists.csv.zip)
* [final_playlists.csv.zip](Data_Analisis_Spotify\Dataset\final_playlists.rar)
* [final_tracks.csv.zip](Data_Analisis_Spotify\Dataset\final_tracks.csv.zip)
* [main_dataset.csv.zip](Data_Analisis_Spotify\Dataset\main_dataset.csv.zip)

Una vez extraídos, los archivos `.csv` deben permanecer dentro de la carpeta `Dataset/`.

### 5. Ejecutar los análisis

Los notebooks utilizados para el análisis exploratorio y el entrenamiento de modelos se encuentran en la carpeta:

```text
Analisis/
```

Cada notebook puede ejecutarse de forma independiente mediante Jupyter Notebook o Visual Studio Code.

### 6. Ejecutar la aplicación de predicción

Acceder a la carpeta de la aplicación:

```bash
cd aplicacion_de_prediccion
```

Ejecutar:

```bash
python app.py
```

Al iniciarse correctamente, Gradio generará una dirección local similar a:

```text
http://127.0.0.1:7860
```

Abrir dicha dirección en un navegador web para utilizar la interfaz gráfica de predicción.

### 7. Uso de la aplicación

1. Introducir la información de la canción.
2. Registrar los artistas asociados.
3. Registrar las playlists relacionadas.
4. Presionar el botón **Predecir**.
5. Consultar el resultado generado por el modelo.

Para realizar una nueva predicción, utilizar el botón **Limpiar todos los datos**.



## Arquitectura

```mermaid
flowchart LR

A[Kaggle datasets] --> B[Merge datasets]
B --> C[EDA]
C --> D[Feature engineering]
D --> E[Entrenamiento de modelos]
E --> F[Modelo final]
F --> G[Interfaz Gradio]
```

## Dataset
El conjunto de datos utilizado en este proyecto fue construido a partir de múltiples fuentes públicas disponibles en Kaggle que contienen información extraída originalmente de Spotify. Debido a cambios recientes en las políticas de acceso de la plataforma, no fue posible realizar una recolección directa y masiva mediante la API oficial, por lo que se optó por integrar diversos datasets previamente recopilados por la comunidad.

Los datos fueron consolidados mediante un proceso de integración basado en los identificadores únicos (URI) de canciones, artistas y playlists. Como resultado, se obtuvo un conjunto de datos enriquecido que combina características musicales, métricas de popularidad, información de artistas y datos relacionados con playlists.

Esta integración permitió construir una visión más completa del ecosistema musical y proporcionó la base necesaria para el análisis exploratorio y el desarrollo de modelos predictivos orientados a estimar el éxito potencial de una canción.


### Canciones
Las canciones son la principal fuente de estudio de este análisis, sus atributos son los siguientes:

| Atributo | Significado | Cálculo |
| :---: | :--- | :--- |  
|**track_uri** | Es el identificador único que tiene cada canción en Spotify, es su ID ||
|**name**|Es el nombre de las canciones||
|**artists_names**|Es una LISTA de los nombres de los artistas involucrados en la creación o interpretación de la canción||
|**popularity**|Es la popularidad actual de la canción.  | Es un número obtenido mediante el cálculo del número reciente de reproducciones sobre el total histórico de reproducciones|
|**album_type**|Es el tipo de lanzamiento de la canción (álbum, single, etc)||
|**is_playable**|Debido a que Spotify puede prohibir la reproducción de algunas canciones, es una variable booleana la cual nos dice si la canción aún se puede reproducir|
|**release_date**| Es la fecha de lanzamiento de la canción||
|**artists_uris**|Es una LISTA que contiene el identificador único de cada artista||
|**playlists_uris**| Es una LISTA que contiene el identificador único de algunas playlists en las que se encuentra la canción||
|**danceability**| Es un valor normalizado (de 0 a 1) el cual representa qué tan bailable es una canción.| Mediante un algoritmo el cual compara el tempo (BPM), estabilidad rítmica, fuerza del compás, regularidad|
|**energy**|Es un valor normalizado (0 a 1), representa la intensidad o la energía que tiene una canción |La energía en Spotify se calcula analizando la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**key**|Es un valor categórico el cual nos dice en qué tonalidad se encuentra una canción | Se analiza la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**loudness**|Es la sonoridad percibida de una canción, medida en decibelios (dB), que determina qué tan fuerte o suave suena el audio para el oído humano en comparación con otras pistas. | Promediando el volumen de toda la canción bajo el estándar internacional LUFS, el cual aplica filtros de frecuencia que imitan la sensibilidad del oído humano para analizar la potencia acústica real.|
|**mode**|Es el modo de la tonalidad, mayor o menor. | Se calcula mediante algoritmos de inteligencia artificial que analizan las relaciones de frecuencia y los acordes predominantes de la pista para asignar un valor binario: 1 para el modo mayor y 0 para el modo menor.|
|**speechiness**|Es la métrica que mide la presencia de palabras habladas en una pista, diferenciando entre contenido puramente hablado y música cantada. ||
|**Acousticness**|Es la medida de confianza que determina la probabilidad de que una canción haya sido creada exclusivamente con instrumentos acústicos, sin amplificación ni efectos electrónicos. | Se calcula mediante algoritmos de aprendizaje automático que analizan el timbre, la pureza de las frecuencias y la ausencia de distorsión digital en la pista, asignando una puntuación de 1.0 para alta probabilidad acústica y 0.0 para música puramente electrónica o muy procesada.|
|**Instrumentalness**|Es la métrica que predice la probabilidad de que una canción no contenga voces humanas|Se calcula mediante algoritmos de inteligencia artificial que analizan la pista en busca de fonemas, palabras o canto estructurado, asignando una puntuación donde los valores superiores a 0.5 indican música instrumental y las canciones con letras convencionales se acercan a 0.0.|
|**Liveness**|Es una métrica que detecta la presencia de una audiencia o público en la grabación, determinando si la canción se grabó en vivo o en un estudio.|Se calcula mediante algoritmos de inteligencia artificial que buscan sonidos ambientales específicos como aplausos, ovaciones, ecos de grandes recintos o ruido de fondo, asignando un valor superior a 0.8 si es una pista en directo y menor a 0.5 si es una sesión de estudio.|
|**Valence**|Es la métrica que describe la positividad musical que transmite una canción, midiendo si el estado de ánimo de la pista es alegre o triste|Se calcula mediante algoritmos de inteligencia artificial que analizan el color tonal, el ritmo y la estructura armónica, asignando un valor entre 0.0 (canciones tristes, deprimidas o enojadas) y 1.0 (canciones felices, alegres o eufóricas).|
|**Tempo**|BPM||
|**duration_ms**|Duración de la canción en milisegundos.||
|**time_signature**|Describe cuántas notas hay por compás.||
|**Artist_popularities**|Es una métrica interna y relativa, expresada en una escala de 0 a 100, que mide la relevancia y el nivel de tracción actual de un músico en la plataforma en comparación con todos los demás|Se calcula de forma matemática y automática a partir de la popularidad acumulada de todas las canciones del artista, utilizando un algoritmo que pondera fuertemente el volumen de reproducciones recientes (de los últimos 28 a 30 días) y el nivel de interacción del usuario, como guardados en la biblioteca o adiciones a playlists|
|**Artist_genres**|Son las etiquetas o clasificaciones musicales asociadas directamente al perfil de un músico, las cuales sirven para agruparlo dentro de estilos, subgéneros y microcomunidades musicales específicas.|Se calcula mediante algoritmos de inteligencia artificial que analizan los metadatos de las distribuidoras, el comportamiento de los usuarios (siempre que los oyentes agrupen al artista con otros similares en sus playlists) y el análisis del sonido de sus canciones mediante el procesamiento de señales digitales.|
|**Artist_followers**|Cantidad de seguidores que tiene cada artista que participa en la canción.||

### Artista

|Atributo|Significado|Cálculo|
| :---: | :--- | :--- | 
|**artist_uri**|Es el identificador único que tiene cada artista en Spotify, es su ID||
|**artist_popularity**|Es una métrica interna y relativa, expresada en una escala de 0 a 100, que mide la relevancia y el nivel de tracción actual de un músico en la plataforma en comparación con todos los demás|Se calcula de forma matemática y automática a partir de la popularidad acumulada de todas las canciones del artista, utilizando un algoritmo que pondera fuertemente el volumen de reproducciones recientes (de los últimos 28 a 30 días) y el nivel de interacción del usuario, como guardados en la biblioteca o adiciones a playlists|
|**Artist_genres**|Son las etiquetas o clasificaciones musicales asociadas directamente al perfil de un músico, las cuales sirven para agruparlo dentro de estilos, subgéneros y microcomunidades musicales específicas.|Se calcula mediante algoritmos de inteligencia artificial que analizan los metadatos de las distribuidoras, el comportamiento de los usuarios (siempre que los oyentes agrupen al artista con otros similares en sus playlists) y el análisis del sonido de sus canciones mediante el procesamiento de señales digitales.|
|**Artist_followers**|Cantidad de seguidores que tiene cada artista que participa en la canción.||

### Playlist

|Atributo|Significado|
| :---: | :--- |
|**uri**|Es el identificador único que tiene cada playlist en Spotify, es su ID|
|**name**|Nombre de la playlist|
|**description**|Descripción de la playlist|
|**query**||
|**author**|Autor de la playlist|
|**n_tracks**|Número de canciones en la playlist, solo se toman en cuenta las primeras 100 canciones|
|**playlist_followers**|Número de seguidores que tiene cada playlist|

El merge de los datasets se realizó mediante la utilización de los *uris*, ya que como son identificadores únicos, se pueden encontrar los registros con ellos


## Metodología

La metodología seguida durante el desarrollo del proyecto se dividió en cuatro etapas principales: análisis exploratorio, ingeniería de características, modelado predictivo e implementación de la aplicación.

### 1. Análisis Exploratorio de Datos (EDA)

La primera etapa consistió en comprender la estructura del conjunto de datos, identificar patrones relevantes y detectar posibles problemas de calidad de información. Para facilitar el análisis, el estudio se dividió en tres áreas principales:

* Análisis de artistas.
* Análisis de características musicales.
* Análisis de popularidad de canciones, artistas y playlists.

Durante esta fase se realizaron análisis estadísticos, visualizaciones y estudios de correlación con el objetivo de identificar variables potencialmente relevantes para la predicción del éxito musical.

### 2. Ingeniería de Características

Una vez comprendido el comportamiento de los datos, se aplicaron diversas transformaciones destinadas a mejorar la capacidad predictiva de los modelos.

Entre las principales transformaciones realizadas se encuentran:

* Discretización de variables probabilísticas.
* Codificación de variables categóricas.
* Estandarización de variables numéricas.
* Construcción de nuevas características derivadas de artistas y playlists.
* Eliminación de observaciones poco representativas para reducir ruido en el conjunto de datos.

Estas transformaciones permitieron obtener un conjunto de variables más adecuado para los algoritmos de aprendizaje automático.

### 3. Desarrollo y Evaluación de Modelos

Posteriormente se entrenaron diversos modelos de clasificación con el objetivo de determinar si una canción podía ser catalogada como éxito o fracaso.

Los algoritmos evaluados fueron:

* Regresión Logística.
* Random Forest.
* XGBoost.

Cada modelo fue sometido a diferentes procesos de ajuste de hiperparámetros y evaluado mediante Accuracy y Matthews Correlation Coefficient (MCC), prestando especial atención a esta última métrica debido al desbalance existente entre clases.

### 4. Implementación de la Aplicación

Finalmente el modelo seleccionado fue integrado dentro de una aplicación interactiva desarrollada utilizando Programación Orientada a Objetos y la biblioteca Gradio.

Esta implementación permite capturar información relacionada con canciones, artistas y playlists para generar predicciones en tiempo real mediante una interfaz gráfica intuitiva.


## Primeros resultados

Para los tres modelos predictivos evaluados se realizaron múltiples experimentos mediante el ajuste de hiperparámetros. Tras diversas pruebas, se seleccionaron las configuraciones que ofrecieron el mejor desempeño dentro de los escenarios analizados.

La evaluación de los modelos se llevó a cabo mediante dos métricas principales: Accuracy Score y Matthews Correlation Coefficient (MCC). El Accuracy mide la proporción de predicciones correctas realizadas por el modelo, tomando valores entre 0 y 1. Por su parte, el MCC considera los cuatro posibles resultados de una matriz de confusión (verdaderos positivos, verdaderos negativos, falsos positivos y falsos negativos), generando valores entre -1 y 1, donde -1 representa una clasificación completamente incorrecta, 0 indica un comportamiento equivalente al azar y 1 corresponde a una clasificación perfecta.

Aunque el Accuracy proporciona una medida general del porcentaje de aciertos, se consideró especialmente relevante el MCC debido al desbalance presente en las clases del conjunto de datos. De esta forma, es posible determinar si el modelo realmente aprendió patrones útiles o si simplemente favorece la clase mayoritaria, obteniendo un Accuracy aparentemente elevado sin una capacidad predictiva real.

* Regresión Logística

    * La regresión logística obtuvo un Accuracy de 0.57, lo que indica que aproximadamente el 57 % de las muestras del conjunto de prueba fueron clasificadas correctamente. Sin embargo, esto también implica que una proporción considerable de observaciones fue clasificada de forma incorrecta. Su valor de MCC fue cercano a 0.19, lo que sugiere que el modelo logró capturar ciertos patrones en los datos, aunque su capacidad predictiva sigue siendo limitada.

* Random Forest

    * El modelo Random Forest presentó un desempeño superior al de la regresión logística, alcanzando un Accuracy de 0.68. Esto significa que más de dos terceras partes de las muestras fueron clasificadas correctamente. No obstante, su MCC fue de aproximadamente 0.20, valor que indica una mejora modesta respecto al modelo anterior y evidencia que aún existen dificultades para distinguir adecuadamente entre las clases.

    * El análisis de importancia de variables mostró que loudness, duration_ms y energy fueron las características con mayor influencia en las predicciones. Este resultado sugiere que dichas variables contienen información relevante para diferenciar entre canciones exitosas y no exitosas dentro del conjunto de datos analizado.

* XGBoost

    * El modelo XGBoost obtuvo resultados prácticamente idénticos a los de Random Forest, tanto en Accuracy como en MCC. Aunque ambos algoritmos se basan en árboles de decisión, difieren en la forma en que construyen y combinan sus modelos, por lo que resulta interesante que hayan alcanzado desempeños tan similares.

    * En cuanto a la importancia de variables, XGBoost identificó a album_type como la característica más relevante. A partir de este hallazgo, se analizó la proporción de clasificaciones correctas para cada categoría de esta variable. Se observó que la categoría compilation presentó la mayor tasa de aciertos, con aproximadamente un 75 % de canciones clasificadas correctamente.

    * Este resultado podría indicar una relación entre la aparición de una canción en un álbum de tipo compilación y su nivel de éxito. Una posible explicación es que las canciones incluidas en compilaciones suelen haber alcanzado previamente cierta popularidad o reconocimiento comercial, lo que las convierte en candidatas para ser relanzadas dentro de este tipo de producciones.

Por lo tanto, se puede concluir que las características musicales poseen cierta capacidad para predecir el éxito de una canción; sin embargo, dicha capacidad es limitada y moderada. Los resultados obtenidos sugieren que estas variables, por sí solas, no son suficientes para explicar completamente el éxito comercial de una pieza musical.

Esta situación puede atribuirse a diversos factores externos que no fueron considerados en el conjunto de datos. Entre ellos destacan la influencia de las redes sociales, las campañas de marketing, la popularidad previa de los artistas, las recomendaciones de las plataformas de streaming y los fenómenos virales que se generan en medios digitales.

En la actualidad, plataformas como TikTok, Instagram Reels y YouTube Shorts tienen la capacidad de impulsar significativamente la popularidad de una canción en periodos muy cortos de tiempo. Como consecuencia, algunas canciones pueden alcanzar niveles elevados de éxito comercial debido a su difusión viral, independientemente de que sus características musicales sean similares a las de otras canciones con menor impacto. Esto sugiere que el éxito musical es un fenómeno complejo que depende tanto de factores musicales como de elementos sociales, culturales y tecnológicos.

Después de darnos cuenta que no se puede predecir el éxito de una canción meramente por los atributos musicales de la misma, se optará por tomar en cuenta datos ajenos a la pieza, como información de sus respectivos autores o playlists en las que se encuentran

Esta vez, se tomará información de playlists en las que se encuentra una canción e información de su respectivo artista

## Resultados finales y conclusiones

Con este nuevo conjunto de características, fue posible predecir el éxito o fracaso de una canción con un mayor grado de confianza. Los modelos alcanzaron un Accuracy cercano al 80 % y un MCC de 0.55. Considerando que el conjunto de datos presenta un desbalance entre clases, estos resultados indican que los modelos lograron aprender patrones relevantes y no se limitaron a predecir la clase predominante.

A diferencia del análisis anterior, en esta ocasión se utilizaron principalmente características externas a las canciones, obteniendo un desempeño significativamente superior. Asimismo, tanto Random Forest como XGBoost mostraron resultados similares en cuanto a la importancia de las variables, lo que aporta consistencia a los hallazgos obtenidos.

Las variables con mayor influencia en las predicciones fueron la popularidad promedio de los artistas y el número promedio de seguidores de los mismos. Este resultado es coherente con la dinámica de la industria musical, ya que los artistas que cuentan con una base sólida de seguidores suelen tener una mayor visibilidad y alcance, lo que incrementa la probabilidad de que sus lanzamientos alcancen niveles elevados de popularidad.

De manera similar, se observó que la presencia de artistas poco conocidos junto a artistas consolidados puede incrementar considerablemente la probabilidad de éxito de una canción. Esto sugiere que la exposición proporcionada por artistas con una audiencia establecida puede tener un impacto significativo en la difusión y recepción de nuevos lanzamientos.

Por otra parte, el número promedio de canciones dentro de una playlist y la cantidad de seguidores de esta también mostraron una influencia importante en el modelo. Este hallazgo indica que la visibilidad proporcionada por playlists populares puede contribuir significativamente al éxito de una canción. En consecuencia, incluso artistas con poca presencia en la industria pueden beneficiarse de aparecer en listas de reproducción con una gran audiencia.

Adicionalmente, este modelo no solo puede interpretarse como un predictor del éxito musical, sino también como una aproximación a la capacidad de una canción para alcanzar una alta difusión en plataformas digitales. Sin embargo, establecer una relación directa con fenómenos virales en servicios como TikTok, Instagram Reels o YouTube Shorts requeriría incorporar variables adicionales relacionadas con la actividad y el alcance de dichas plataformas.

Los resultados obtenidos permiten concluir que las características externas asociadas a los artistas y a los mecanismos de difusión tienen una capacidad predictiva considerablemente superior a la de las características musicales analizadas previamente. En particular, la popularidad de los artistas, su base de seguidores y la exposición obtenida a través de playlists desempeñan un papel fundamental en la predicción del éxito de una canción. Por ello, puede afirmarse que los factores externos constituyen indicadores relevantes para estimar la probabilidad de éxito comercial de una producción musical.


## Implementación de interfaz del modelo

Con el objetivo de facilitar la interacción con el modelo predictivo, se desarrolló una aplicación web utilizando la biblioteca Gradio. Esta herramienta permite consumir el modelo entrenado mediante una interfaz gráfica intuitiva, eliminando la necesidad de ejecutar código o interactuar directamente con los notebooks de análisis.

La aplicación implementa una arquitectura basada en Programación Orientada a Objetos, donde las entidades principales del dominio (Canción, Artista y Playlist) son representadas mediante clases independientes. Posteriormente, un servicio especializado transforma la información ingresada por el usuario en el conjunto de características requerido por el modelo de Machine Learning.

Una vez procesados los datos, el modelo genera una predicción indicando si la canción posee características asociadas al éxito o al fracaso dentro del contexto analizado.

```mermaid
flowchart LR

A[Usuario] --> B[Interfaz Gradio]
B --> C[Objetos Cancion Artista Playlist]
C --> D[Feature Engineering]
D --> E[Modelo XGBoost]
E --> F[Prediccion]
```


![Interfaz de la aplicación](resources/app_img.png)


#### Ejemplos de entrada)

| # | Canción | Detalles Canción | Artistas (Popularidad, Géneros, Seguidores) | Playlist (Nombre, Canciones, Seguidores) | Salida |
| :-: | :--- | :--- | :--- | :--- | :-: |
| **1** | **Flowers** | • **Reproducible:** Sí<br>• **Tipo:** Single<br>• **Lanzamiento:** 2023-12-01 | • **Artista 1:** Pop. 92 \| pop \| 20250106 seg. | • **Nombre:** 100 Canciones más felices<br>• **Canciones:** 100<br>• **Seguidores:** 24586 | **Éxito** |
| **2** | **PRC** | • **Reproducible:** Sí<br>• **Tipo:** Single<br>• **Lanzamiento:** 2024-06-20 | • **Artista 1:** Pop. 91 \| sad sierreno \| 1548818 seg.<br>• **Artista 2:** Pop. 87 \| corrido, corridos tumbados, mexa \| 6173797 seg. | • **Nombre:** Corridos 2022-2023<br>• **Canciones:** 174<br>• **Seguidores:** 19974 | **Éxito** |
| **3** | **Death Blues** | • **Reproducible:** Sí<br>• **Tipo:** Álbum<br>• **Lanzamiento:** 2010-03-26 | • **Artista 1:** Pop. 29 \| dark cabaret, gothic \| 15,968 seg. | • **Nombre:** gothic songs<br>• **Canciones:** 13<br>• **Seguidores:** 223 | **Fracaso** |

## Estructura del repositorio

```text
Data_Analisis_Spotify/
│
├── Analisis/
│   ├── artista.ipynb
│   ├── Caracteristicas_musicales.ipynb
│   ├── popularidad.ipynb
│   └── predicciones.ipynb
│
├── aplicacion_de_pred/
│   ├── modelos/
│   │   ├── __init__.py
│   │   ├── artista.py
│   │   ├── cancion.py
│   │   └── playlist.py
│   │
│   ├── servicios/
│   │   ├── __init__.py
│   │   ├── creador_de_features.py
│   │   ├── predictor.py
│   │   └── predictor.joblib
│   │
│   ├── ui/
│   │   ├── __init__.py
│   │   └── interfaz.py
│   │
│   └── app.py
│
├── Dataset/
│   ├── artists.csv
│   ├── final_playlists.csv
│   ├── final_tracks.csv
│   └── main_dataset.csv
│
├── resources/
│   ├── app_img.png
│   ├── diagrama_UML.md
│   ├── Explicacion_de_variables.md
│   └── objetivos.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

### Descripción de directorios

| Carpeta | Descripción |
|----------|------------|
| `Analisis/` | Notebooks utilizados para análisis exploratorio, ingeniería de características y evaluación de modelos. |
| `aplicacion_de_prediccion/modelos/` | Clases de dominio que representan artistas, canciones y playlists. |
| `aplicacion_de_prediccion/servicios/` | Lógica de negocio para creación de características y generación de predicciones. |
| `aplicacion_de_prediccion/ui/` | Componentes de la interfaz gráfica desarrollada con Gradio. |
| `Dataset/` | Conjunto de datos obtenidos y procesados de Kaggle. |
| `resources/` | Recursos de documentación, diagramas UML, imágenes y material de apoyo. |


## Autores

* Alarcón Ruiz Sergio Fernando
* Ramírez Cortes Axel Osiris

Estudiantes de Licenciatura en Ciencia de Datos
ESCOM - Instituto Politécnico Nacional
