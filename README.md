# Validation of Twitter trends using topic modeling

Lo que se busca con este trabajo es analizar las tendencias generadas por los #hashtags, y ponerlas en contraste con las tendencias generadas con el uso del modelado de tópicos. Para esto se usará como caso de estudio las tendencias relacionadas al presidente de la republica del Perú.

## Tweets Scrapping

Para esto se utilizó Twint con la siguiente configuración de parámetros:

<p align="center">
  <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/scrapping-parameters.png" alt="scrapping parameters" width="300px" height="200px" align="center">
</p>

## Data Workflow

Esta parte consta de 4 partes:

1. Se completan los tweets de algunos días faltantes en el scrapping. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/1-tweets-completition.ipynb)
2. Se hace un procesamientos del texto de los tweets, los cuales serán la entrada para el modelado de tópicos. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/2-preprocessing.ipynb)
3. Se extraen los hashtags de los tweets para el análisis de tendencias final. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/3-hashtags-extration.ipynb)
4. Se hace el modelamiento de tópicos y la generación de tópicos, usados para el análisis de tendencias final. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/4-top2vec.ipynb)

## Insights

Como análisis final se verá la tendencia de una palabra atravez del tiempo. Esta tendencia se verá con la cantidad de tweets que tiene o hablan sobre esta palabra. Este análisis de tendencias se hará de dos formas

La primera es usando solo los hashtags, en donde, si el hashtags en en el tweet tiene la palabra, se considerará el tweets dentro de la tendencia.

La otra forma es usando los tópicos generados. Un tópico esta representado por un conjunto de palabras, las cuales tiene un porcentaje de probabilidad. Este porcentaje representa la probabilidad de que el tópico se trate sobre esa palabra.

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/topic.png" alt="topic"><br>
    Representación de tópico.
</p>

Sabiendo que cada tweet pertence a un tópico, para el análisis de la tendencia de la palabra se usará las palabras del tópico al cual el tweet pertence. Si la palabra pertence al tópico y cumple un cierto porcentaje de probabilidad, el tweet se considerará dentro de la tendencia. De esta forma se asegura que en el tweet se está hablando realmente de la palabra.

## Outcomes

Los siguientes son resultados obtenidos usando las siguientes palabras, en donde la grafica azul representa la tendencia usando tópicos, y la gráfica naranja es usando hashtags:

* abimael

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/abimael.png" alt="topic">
</p>
  
* vacancia

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/vacancia.png" alt="topic">
</p>

* congreso

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/congreso.png" alt="topic">
</p>

* gabinete

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/gabinete.png" alt="topic">
</p>

* bolivia

<p align="center">
    <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/bolivia.png" alt="topic">
</p>

The analysis of this project is published on my Medium. Check it out [here](https://medium.com/@antonyjuan.miranda/validando-las-tendencias-de-twitter-durante-la-era-castillo-con-topic-modeling-d2c0a4f5474a).
