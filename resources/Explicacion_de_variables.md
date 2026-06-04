# Explcacion del significado de variables en el dataset

## Canciones
Las canciones son la principal fuente de estudio de este analisis, sus atributos son los siguientes:

| Atributo | Significado | Calculo |
| :---: | :--- | | :--- |
| **track_uri** | Es el identificador unico que tiene cada cancion en spotify, es su ID ||
|**name**|Es el nombre de las canciones||
|**artists_names**|Es una LISTA de los nombres de los artistas involucrados en la creacion o interpretacion de la cancion||
|**popularity**|Es la popularidad actual de la cancion.  | Es un numero obtenido mediante el calculo del numero reciente de reproducciones sobre el total historico de reproducciones|
|**album_type**|Es el tipo de lanzamiento de la cancion (album, single, etc)||
|**is_playable**|Debido a que spotify puede prohibir la reproduccion de algunas canciones, es una variable booleana la cual nos dice si la cancion aun se puede reproducir|
|**release_date**| Es la fecha de lanzamiento de la cancion||
|**artists_uris**|Es una LISTA que contiene el identificador unico de cada artista||
|**playlists_uris**| Es una LISTA que contiene el identificador unico de algunas playlists en las que se encuentra la cancion||
|**danceability**| Es un valor normalizado (de 0 a 1) el cual rebresenta que tan bailable es una cancion. <br> **Calculo:** mediante un algoritmo el cual compara el tempo (BPM), estabilidad ritmitca, fuerza del compas, regularidad|
|**energy**|Es un valor nromalizado (0 a 1), representa la intensidad o la energia que tiene una cancion <br> **Calculo:** La energía en Spotify se calcula analizando la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**key**|Es una valor categorico el cual nos dice en que tonalidad se encuentra una cancion <br> **Calculo:** Se analiza la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**loudness**|Es la sonoridad percibida de una canción, medida en decibelios (dB), que determina qué tan fuerte o suave suena el audio para el oído humano en comparación con otras pistas. <br> **Calculo:**  promediando el volumen de toda la canción bajo el estándar internacional LUFS, el cual aplica filtros de frecuencia que imitan la sensibilidad del oído humano para analizar la potencia acústica real.|
|**mode**|Es el modo de la tonalidad, mayor o menor. <br> **Calculo:** Se calcula mediante algoritmos de inteligencia artificial que analizan las relaciones de frecuencia y los acordes predominantes de la pista para asignar un valor binario: 1 para el modo mayor y 0 para el modo menor.|
|**speechiness**|Es la métrica que mide la presencia de palabras habladas en una pista, diferenciando entre contenido puramente hablado y música cantada. <br> **Calculo:**|
|**Acousticness**|Es la medida de confianza que determina la probabilidad de que una canción haya sido creada exclusivamente con instrumentos acústicos, sin amplificación ni efectos electrónicos <br> **calculo:** Se calcula mediante algoritmos de aprendizaje automático que analizan el timbre, la pureza de las frecuencias y la ausencia de distorsión digital en la pista, asignando una puntuación de 1.0 para alta probabilidad acústica y 0.0 para música puramente electrónica o muy procesada.|
|||
|||
|||