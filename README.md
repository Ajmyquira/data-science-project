# Validation of Twitter trends using topic modeling.

Lo que se busca con este trabajo es analizar las tendencias generadas por los #hashtags, y ponerlas en contraste con las tendencias generadas con el uso del modelado de tópicos. Para esto se usará como caso de estudio las tendencias relacionadas al presidente de la republica del Perú.

## Tweets Scrapping

Para esto se utilizó Twint con la siguiente configuración de parámetros.

<p align="center">
  <img src="https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/images/scrapping-parameters.png" alt="scrapping parameters" width="300px" height="200px" align="center">
</p>

## Data Manipulation

Esta parte consta de 3 partes:

1. Se completan los tweets de algunos días faltantes en el scrapping. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/1-tweets-completition.ipynb)
2. Se hace un procesamientos del texto de los tweets, los cuales serán la entrada para el modelado de tópicos. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/2-preprocessing.ipynb)
3. Se extraen los hashtags de los tweets para el análisis de tendencias final. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/3-hashtags-extration.ipynb)
4. Se hace el modelamiento de tópicos y la generación de tópicos, usados para el análisis de tendencias final. [notebook](https://github.com/Ajmyquira/tweets-topic-modelling/blob/master/4-top2vec.ipynb)

## Topic Modelling

Cada uno de los topicos tiene un conjunto de palabras que más lo representan, los cuales tienen un valor de probabilidad. Mientras más alto sea el valor de probabilidad, mayor sera la probabilidad de que en ese tópico se hable sobre esa palabra.

## Insights

De entre los tópicos utilizados, se busca los documentos que contengan cierta palabra como tópico.
De estos documentos se muestran la cantidad de documentos en función de sus fechas.

Al un documento pertenecer a un topic, no indica de manera más realista de que ese documento realmente está hablando de ese tema, y no solo tiene esa palabra escrita. Además que para considerar una palabra de un tópico para un documento, tiene que tener un cierto porcentaje de probabilidad

#### abimael

#### vacancia

#### congreso

#### gabinete

#### bolivia

The analysis of this project is published on my Medium. Check it out [here](https://medium.com/@antonyjuan.miranda/validando-las-tendencias-de-twitter-durante-la-era-castillo-con-topic-modeling-d2c0a4f5474a).

### References

[Search just stops scraping](https://github.com/twintproject/twint/issues/1363)
