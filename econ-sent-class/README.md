# Clasificador de Sentimiento Económico

En este repositorio se muestra cómo desarrollar un **clasificador de sentimiento económico**, un algoritmo que clasifica textos con contenido económico según su polaridad: pesimista, neutral u optimista.

## Enlaces a resumenes

Puede encontrar un resumen del trabajo en mi **sitio web**:

https://www.percepcioneseconomicas.cl/indices/indice-de-sentimiento-corporativo-parte-1/

https://www.percepcioneseconomicas.cl/indices/indice-de-sentimiento-corporativo-parte-2/

***

Un **resumen en PDF**, más extenso y detallado, se puede encontrar en:

https://github.com/percepcioneseconomicas/publicaciones/blob/main/isc/Indice%20de%20Sentimiento%20Corporativo-comprimido.pdf

***

Las notebooks también se pueden encontrar explicadas en mi canal de **YouTube**: 

https://youtube.com/playlist?list=PLQHBntu5_EeKbhBLbJzAJNNIyVuNVHdOt


## Introducción 

Este trabajo se inspira en el **índice de incertidumbre político-económica de Baker, Bloom y Davis (2016)**. El algoritmo calcula la frecuencia con que se encuentran grupos de palabras asociadas a la incertidumbre en noticias publicadas en los 10 mayores periódicos de EEUU. Los artículos deben contener los tríos de palabras: “economic” o “economy”, “uncertain” o “uncertainty”, y uno o más entre “congress”, “deficit”, “Federal Reserve”, “legislation”, “regulation” o “White House”. El índice es capaz de predecir—a nivel de firmas—la volatilidad de los precios de las acciones, la inversión y el empleo en sectores económicos sensibles; y a nivel macro, la inversión agregada, actividad económica, y el empleo.

En Chile se han realizado trabajos similares. Por ejemplo, el **índice de incertidumbre económica de Clapes UC**, propuesto por Cerda, Silva y Valente (2018); o los estudios de Becerra y Sagner (2020), quienes elaboraron un índice de incertidumbre económica en base a publicaciones de Twitter; y el de del Pilar, Peralta y Ávila (2020), quienes realizaron un análisis del sentimiento del *Informe de Percepciones de Negocios* del Banco Central de Chile.

La principal **contribución de este trabajo** es que, a diferencia de los otros estudios, que clasifican la polaridad (sentimiento) de los textos en base a un conjunto arbitrario de palabras, en este estudio la clasificación del sentimiento se realiza mediante algoritmos de Machine Learning, que seleccionan automáticamente las palabras que mejor reflejan los sentimientos. De esta manera, se busca que la clasificación del sentimiento económico encontrado en los textos sea lo más imparcial y completa posible, basada en patrones y combinaciones de palabras que se encuentran frecuentemente, y que pueden ser identificadas de forma eficiente y sistemática por los algoritmos. 

El algoritmo se utilizó para identificar el sentimiento económico implícito en las cartas a los accionistas de las empresas del IPSA, y en base a esta clasificación se elaboró el **índice de sentimiento corporativo (ISC)**.

El desarrollo del clasificador se encuentra separado en una serie de notebooks que se describen a continuación:


## Análisis exploratorio

https://github.com/percepcioneseconomicas/publicaciones/blob/main/econ-sent-class/0_analisis_exploratorio.ipynb

En esta sección se analiza descriptivamente la base de datos de **cartas a los accionistas**. Luego se prepara para su análisis posterior, dándole una estructura adecuada.


## Modelo

En esta sección se desarrolla el **modelo** clasificador de sentimiento económico:
https://github.com/percepcioneseconomicas/publicaciones/blob/main/econ-sent-class/1_modelo.ipynb

Los **datos** de sentimiento económico, usados para entrenar al modelo, se pueden encontrar en:
https://github.com/percepcioneseconomicas/publicaciones/tree/main/sentiment_data


## Clasificación

En esta sección se muestra cómo usar el modelo para **clasificar las cartas a los accionistas** según su sentimiento económico:
https://github.com/percepcioneseconomicas/publicaciones/blob/main/econ-sent-class/2_clasificacion.ipynb 

## Indice de Sentimiento Corporativo

En esta sección se construye el **índice de sentimiento corporativo** y se analiza descriptivamente.
https://github.com/percepcioneseconomicas/publicaciones/blob/main/econ-sent-class/3_indice_sentimiento_corporativo.ipynb 


## Referencias

Baker, S., Bloom, N & Davis, J. (2016). Measuring Economic Policy Uncertainty, The Quarterly Journal of Economics, Volume 131, Issue 4, November 2016, Pages 1593–1636, https://doi.org/10.1093/qje/qjw024

Becerra, Juan Sebastián & Sagner, Andrés (2020). Twitter-Based Economic Policy Uncertainty Index for Chile. Working Papers N° 883 https://www.bcentral.cl/en/web/banco-central/content/-/detalle/documento-de-trabajo-n-883

Cerda, Rodrigo; Silva, Álvaro & Valente, José Tomás (2018). Impact of economic uncertainty in a small open economy: the case of Chile, Applied Economics, Taylor & Francis Journals, vol. 50(26), pages 2894-2908, June. https://doi.org/10.1080/00036846.2017.1412076

del Pilar Cruz, María; Peralta, Hugo & Ávila, Bruno (2020). Análisis de Sentimiento Basado en el Informe de Percepciones de Negocios del Banco Central de Chile, Working Papers Central Bank of Chile 862, Central Bank of Chile. https://www.bcentral.cl/en/web/banco-central/content/-/detalle/analisis-de-sentimiento-basado-en-el-informe-de-percepciones-de-negocios-del-banco-central-de-chile
