# Practica_1_Web_scraping
##  1. Contexto
El comportamiento humano es muy dificil de predecir. En el análisis de datos, en ocasiones, se pretende predecir a través de los datos, alguna acción que se sustenta plenamente, por el comportamiento humano. Es muy dificil, encontrar aquellas variables que correlacionan con el comportamiento humano, a veces, correlacionan los factores climáticos como la temperatura o la velocidad del viento, así como, tabién correlacionan otros datos como los económicos provenientes de índices bursátiles. 

En este ejercicio, proponemos extraer datos sobre el sentimiento social de una población a partir de la influencia periodística. 

¿Depende de cómo se escriba un artículo periodístico, puede influir al comportamiento humano?

Para responder a esta pregunta, ofrecemos la extracción de datos de un diario digital y su posterior cruce de datos con un diccionario de sentimientos. 

De este modo, obtendremos una puntuación sobre qué grado emocional/sentimental tiene la influencia periodística en el día de hoy.

El diario digital elegido es el New York Times -> https://www.nytimes.com/section/todayspaper?redirect_uri=https%3A%2F%2Fwww.nytimes.com%2F

En este diario, encontramos un total de 55 noticias que resumen la actualidad del día de hoy 10/11/2019.

A través de la metodología del Web Scrapping, extraermos el contenido de los 55 titulares que resumen estas 55 noticias. Luego, procesaremos los datos obtenidos mediante una INNER JOIN con el diccionario de puntuación de palabras. Este diccionario, se ha obtenido de una web de referencia donde se expone una puntuación sentimental del -5 al 5 para cada una de las palabras, por ejemplo, "racista" esta puntuada con un -3. Finalmente, se realiza un sumatorio de todas las puntuaciones obtenidas, y ese resultado marcará la puntuación emocional/sentimental de influencia periodística. 

##  2. Título para el dataset
Puntuación emocional/sentimental de influencia periodística

## 3. Descripción del dataset
El DataSet obtenido ofrece un toal de 55 registros y un sola variable "html_text.titulares." esta  variable es el texto completo que compone cada una de las noticias del diario New York Times del día 10/11/2019.

## 4. Representación gráfica. 


## 5. Contenido
Explicar los campos que incluye el dataset, el periodo de tiempo de los datos y cómo se ha recogido.

## 6. Agradecimientos
Presentar al propietario del conjunto de datos. Es necesario incluir citas de investigación o análisis anteriores (si los hay).

## 7. Inspiración
Explique por qué es interesante este conjunto de datos y qué preguntas se pretenden responder.

## 8. Licencia
Seleccione una de estas licencias para su dataset y explique el motivo de su selección:
○ Released Under CC0: Public Domain License
○ Released Under CC BY-NC-SA 4.0 License
○ Released Under CC BY-SA 4.0 License
○ Database released under Open Database License, individual contents
under Database Contents License
○ Other (specified above)
○ Unknown License

## 9. Código
Adjuntar el código con el que se ha generado el dataset, preferiblemente en Python o, alternativamente, en R.

## 10. Dataset
Presentar el dataset en formato CSV
