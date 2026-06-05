# Explcacion del significado de variables en el dataset

## Canciones
Las canciones son la principal fuente de estudio de este analisis, sus atributos son los siguientes:

| Atributo | Significado | Calculo |
| :---: | :--- | :--- |  
| **track_uri** | Es el identificador unico que tiene cada cancion en spotify, es su ID ||
|**name**|Es el nombre de las canciones||
|**artists_names**|Es una LISTA de los nombres de los artistas involucrados en la creacion o interpretacion de la cancion||
|**popularity**|Es la popularidad actual de la cancion.  | Es un numero obtenido mediante el calculo del numero reciente de reproducciones sobre el total historico de reproducciones|
|**album_type**|Es el tipo de lanzamiento de la cancion (album, single, etc)||
|**is_playable**|Debido a que spotify puede prohibir la reproduccion de algunas canciones, es una variable booleana la cual nos dice si la cancion aun se puede reproducir|
|**release_date**| Es la fecha de lanzamiento de la cancion||
|**artists_uris**|Es una LISTA que contiene el identificador unico de cada artista||
|**playlists_uris**| Es una LISTA que contiene el identificador unico de algunas playlists en las que se encuentra la cancion||
|**danceability**| Es un valor normalizado (de 0 a 1) el cual rebresenta que tan bailable es una cancion.| Mediante un algoritmo el cual compara el tempo (BPM), estabilidad ritmitca, fuerza del compas, regularidad|
|**energy**|Es un valor nromalizado (0 a 1), representa la intensidad o la energia que tiene una cancion |La energía en Spotify se calcula analizando la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**key**|Es una valor categorico el cual nos dice en que tonalidad se encuentra una cancion | Se analiza la señal de audio de una canción y midiendo su volumen, velocidad, ritmo y ruido para asignarle un valor de intensidad|
|**loudness**|Es la sonoridad percibida de una canción, medida en decibelios (dB), que determina qué tan fuerte o suave suena el audio para el oído humano en comparación con otras pistas. | Promediando el volumen de toda la canción bajo el estándar internacional LUFS, el cual aplica filtros de frecuencia que imitan la sensibilidad del oído humano para analizar la potencia acústica real.|
|**mode**|Es el modo de la tonalidad, mayor o menor. | Se calcula mediante algoritmos de inteligencia artificial que analizan las relaciones de frecuencia y los acordes predominantes de la pista para asignar un valor binario: 1 para el modo mayor y 0 para el modo menor.|
|**speechiness**|Es la métrica que mide la presencia de palabras habladas en una pista, diferenciando entre contenido puramente hablado y música cantada. ||
|**Acousticness**|Es la medida de confianza que determina la probabilidad de que una canción haya sido creada exclusivamente con instrumentos acústicos, sin amplificación ni efectos electrónicos. | Se calcula mediante algoritmos de aprendizaje automático que analizan el timbre, la pureza de las frecuencias y la ausencia de distorsión digital en la pista, asignando una puntuación de 1.0 para alta probabilidad acústica y 0.0 para música puramente electrónica o muy procesada.|
|**Instrumentalness**|Es la métrica que predice la probabilidad de que una canción no contenga voces humanas|Se calcula mediante algoritmos de inteligencia artificial que analizan la pista en busca de fonemas, palabras o canto estructurado, asignando una puntuación donde los valores superiores a 0.5 indican música instrumental y las canciones con letras convencionales se acercan a 0.0.|
|**Liveness**|Es una métrica que detecta la presencia de una audiencia o público en la grabación, determinando si la canción se grabó en vivo o en un estudio.|Se calcula mediante algoritmos de inteligencia artificial que buscan sonidos ambientales específicos como aplausos, ovaciones, ecos de grandes recintos o ruido de fondo, asignando un valor superior a 0.8 si es una pista en directo y menor a 0.5 si es una sesión de estudio.|
|**Valence**|Es la métrica que describe la positividad musical que transmite una canción, midiendo si el estado de ánimo de la pista es alegre o triste|Se calcula mediante algoritmos de inteligencia artificial que analizan el color tonal, el ritmo y la estructura armónica, asignando un valor entre 0.0 (canciones tristes, deprimidas o enojadas) y 1.0 (canciones felices, alegres o eufóricas).|
|**Tempo**|BPM||
|**duration_ms**|Duracion de la cancion en milisegundos.||
|**time_signature**|Describe cuantas notas hay por compas.||
|**Artist_popularities**|Es una métrica interna y relativa, expresada en una escala de 0 a 100, que mide la relevancia y el nivel de tracción actual de un músico en la plataforma en comparación con todos los demás|Se calcula de forma matemática y automática a partir de la popularidad acumulada de todas las canciones del artista, utilizando un algoritmo que pondera fuertemente el volumen de reproducciones recientes (de los últimos 28 a 30 días) y el nivel de interacción del usuario, como guardados en la biblioteca o adiciones a playlists|
|**Artist_genres**|Son las etiquetas o clasificaciones musicales asociadas directamente al perfil de un músico, las cuales sirven para agruparlo dentro de estilos, subgéneros y microcomunidades musicales específicas.|Se calcula mediante algoritmos de inteligencia artificial que analizan los metadatos de las distribuidoras, el comportamiento de los usuarios (siempre que los oyentes agrupen al artista con otros similares en sus playlists) y el análisis del sonido de sus canciones mediante el procesamiento de señales digitales.|
|**Artist_followers**|Cantidad de seguidores que tiene cada artista que participa en la cancion.||

## Artista

|Atributo|Significado|Calculo|
| :---: | :--- | :--- | 
|**artist_uri**|Es el identificador unico que tiene cada artista en spotify, es su ID||
|**artist_popularitu**|Es una métrica interna y relativa, expresada en una escala de 0 a 100, que mide la relevancia y el nivel de tracción actual de un músico en la plataforma en comparación con todos los demás|Se calcula de forma matemática y automática a partir de la popularidad acumulada de todas las canciones del artista, utilizando un algoritmo que pondera fuertemente el volumen de reproducciones recientes (de los últimos 28 a 30 días) y el nivel de interacción del usuario, como guardados en la biblioteca o adiciones a playlists|
|**Artist_genres**|Son las etiquetas o clasificaciones musicales asociadas directamente al perfil de un músico, las cuales sirven para agruparlo dentro de estilos, subgéneros y microcomunidades musicales específicas.|Se calcula mediante algoritmos de inteligencia artificial que analizan los metadatos de las distribuidoras, el comportamiento de los usuarios (siempre que los oyentes agrupen al artista con otros similares en sus playlists) y el análisis del sonido de sus canciones mediante el procesamiento de señales digitales.|
|**Artist_followers**|Cantidad de seguidores que tiene cada artista que participa en la cancion.||

## Playlist

|Atributo|Significado|
| :---: | :--- |
|**uri**|Es el identificador unico que tiene cada playlist en spotify, es su ID|
|**name**|Nombre de la playlist|
|**description**|Descripcion de la playlist|
|**query**||
|**author**|Autor de la playlist|
|**n_tracks**|Numero de canciones en la playlist, solo se toman en cuenta las primeras 100 canciones|
|**playlist_followers**|Numero de seguidores que tiene cada playlist|
