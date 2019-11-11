# Practica_1_Web_scraping
##  1. Contexto
El comportamiento humano es muy difícil de predecir. En el análisis de datos, en ocasiones, se pretende predecir a través de los datos, alguna acción que se sustenta plenamente, por el comportamiento humano. Es muy difícil, encontrar aquellas variables que correlacionan con el comportamiento humano, a veces, correlacionan los factores climáticos como la temperatura o la velocidad del viento, así como, también correlacionan otros datos como los económicos provenientes de índices bursátiles.

En este ejercicio, proponemos extraer datos sobre el sentimiento social de una población a partir de la influencia periodística.
¿Depende de cómo se escriba un artículo periodístico, puede influir al comportamiento humano?

Para responder a esta pregunta, ofrecemos la extracción de datos de un diario digital y su posterior cruce de datos con un diccionario de sentimientos.

De este modo, obtendremos una puntuación sobre qué grado emocional/sentimental tiene la influencia periodística en el día de hoy.
El diario digital elegido es el New York Times -> https://www.nytimes.com/section/todayspaper?redirect_uri=https%3A%2F%2Fwww.nytimes.com%2F

En este diario, encontramos un total de 55 noticias que resumen la actualidad del día de hoy 10/11/2019.

A través de la metodología del Web Scrapping, extraemos el contenido de los 55 titulares que resumen estas 55 noticias. Luego, procesaremos los datos obtenidos mediante una INNER JOIN con el diccionario de puntuación de palabras. Este diccionario, se ha obtenido de una web de referencia donde se expone una puntuación sentimental del -5 al 5 para cada una de las palabras, por ejemplo, "racista" esta puntuada con un -3. Finalmente, se realiza un sumatorio de todas las puntuaciones obtenidas, y ese resultado marcará la puntuación emocional/sentimental de influencia periodística.

##  2. Título para el dataset
Puntuación emocional/sentimental de influencia periodística

## 3. Descripción del dataset
El DataSet obtenido ofrece un total de 55 registros y un sola variable "html_text.titulares." esta  variable es el texto completo que compone cada una de las noticias del diario New York Times del día 10/11/2019.

## 4. Representación gráfica. 
*Se adjunta imagen nombrada "4_representacion_grafica"

## 5. Contenido
En el diario digital New York Times, en su publicación del día 10/11/2019 encontramos un total de 55 noticias. Estas noticias están todas encabezadas por un titular. Los titulares son la parte más crítica de la estructura de una noticia, un titular debe cumplir con la misión de informar sobre el contenido de la noticia y a la vez, mostrar un atractivo para que el lector se sienta seducido o intrigado en conocer más información y por tanto, genere la acción de clicar y leer el contenido de la noticia. Por lo tanto, el titular es la parte más valiosa de la noticia y como tal, los periodistas aportan mucha destreza en elegir bien que palabras marcarán ese titular. 

Por esta razón, empleamos las técnicas de Web Scrapping para extraer el contenido de todos los titulares del día. Este proceso de extracción lo realizamos mediante R Studio. El primer paso es marcar la url del diario y el siguiente paso es detectar el código html que hay detrás de los 55 titulares. Para saber que código es, utilizamos la herramienta "SelectorGadjet", la cual instalamos en nuestro navegador y es tan fácil de usar como abrir en el navegador con la url del NY Times, activar el "SelectorGadjet" instalado como extensión y finalmente, clicar encima de un titular. De este modo, se obtiene el resultado del código html que clasifica los titulares, en nuestro caso, ".e1f68otr0". Con ello, programamos la función de R por tal de extraer el contenido de todos los titulares. A continuación, procesamos los datos obtenidos realizando una limpieza de texto para que luego, estos datos puedan ser tratados.

Una vez se ha obtenido los 55 titulares, procesaremos los datos obtenidos mediante una INNER JOIN con el diccionario de puntuación de palabras (adjuntado con un dataset nombrado "diccionario_emocional". Este diccionario, se ha obtenido de la Universidad De Notre Dame https://sraf.nd.edu/data/ exponen una puntuación sentimental del -5 al 5 para cada una de las 2.477 palabras. Finalmente, se realiza un sumatorio de todas las puntuaciones obtenidas, y ese resultado marcará la puntuación emocional/sentimental de influencia periodística. 

## 6. Agradecimientos
Mostramos agradecimiento por los recursos facilitados públicamente: 

- Universidad de Notre Dame: Dicionario sentimental/emocional https://sraf.nd.edu/data/
- Diario New York Times: https://www.nytimes.com

## 7. Inspiración
Este ejercicio tiene un valor para aquellos analistas de datos que buscan aquellas variables que pueden ayudar a potenciar los resultados de éxito predictivos. En muchas ocasiones, necesitamos aplicar creatividad por tal de obtener variables que ayuden en la creación de modelos predictivos. Por ejemplo, cuando necesitamos predecir un accidente de tráfico, necesitamos un historial de todos los accidentes de tráfico que ha habido en una calle concreta de una ciudad, esta variable sería la que queremos predecir. Pero junto a ella, necesitamos compactarla con más variables que puedan correlacionarse. Siguiendo con este ejemplo, si cada registro es una fecha, necesitaríamos encontrar otras variables que correlacionaran mediante fechas con la variable de histórico de accidentes, una podría ser el volumen de tráfico, otra podría ser la temperatura, la velocidad del viento... Y por qué no, otra variable que podría introducirse es la puntuación emocional de influencia periodística, es decir, el resultado sobre cómo percibimos las noticias del día. Finalmente, si es que hay correlación, obtendríamos un resultado predictivo sobre si hoy, habrá o no habrá un accidente de tráfico.

## 8. Licencia

○ Released Under CC0: Public Domain License

## 9. Código
*Se adjunta el código en R sobre el ejercicio descrito

## 10. Dataset
*Se adjunta el dataset con los resultados obtenidos
