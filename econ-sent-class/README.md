# Clasificar de Sentimiento Económico

En este repositorio se muestra cómo desarrollar un **clasificador de sentimiento económico**, un algoritmo que clasifica textos con contenido económico según su polaridad: pesimista, neutral u optimista.

## Enlaces a resumenes y explicaciones

Puede encontrar un resumen del trabajo en mi **sitio web**:

https://www.percepcioneseconomicas.cl/indices/indice-de-sentimiento-corporativo-parte-1/

https://www.percepcioneseconomicas.cl/indices/indice-de-sentimiento-corporativo-parte-2/

***

Un **resumen en PDF**, más extenso y detallado, se puede encontrar en:

https://github.com/percepcioneseconomicas/publicaciones/blob/main/isc/Indice%20de%20Sentimiento%20Corporativo-comprimido.pdf

***

Las notebooks también se pueden encontrar explicadas en mi canal de **YouTube** (pendiente): 

https://www.youtube.com/channel/UCC35tdrH4dDRFhDEvPYl2bQ

<a href="https://www.youtube.com/channel/UCC35tdrH4dDRFhDEvPYl2bQ" target="_blank"> YouTube </a>



## Introducción 

Este trabajo se inspira en el **índice de incertidumbre político-económica de Baker, Bloom y Davis (2016)**. El algoritmo calcula la frecuencia con que se encuentran grupos de palabras asociadas a la incertidumbre en noticias publicadas en los 10 mayores periódicos de EEUU. Los artículos deben contener los tríos de palabras: “economic” o “economy”, “uncertain” o “uncertainty”, y uno o más entre “congress”, “deficit”, “Federal Reserve”, “legislation”, “regulation” o “White House”. El índice es capaz de predecir—a nivel de firmas—la volatilidad de los precios de las acciones, la inversión y el empleo en sectores económicos sensibles; y a nivel macro, la inversión agregada, actividad económica, y el empleo.

En Chile se han realizado trabajos similares. Por ejemplo, el índice de incertidumbre económica de Clapes UC, propuesto por Cerda, Silva y Valente (2018), investigadores de Clapes UC; o los estudios de Becerra y Sagner (2020), quienes elaboraron un índice de incertidumbre económica en base a actividad de Twitter; y el de del Pilar, Peralta y Ávila (2020), quienes realizaron un análisis del sentimiento del Informe de Percepciones de Negocios del Banco Central de Chile.

La principal contribución de este trabajo es que, a diferencia de los otros estudios que interpretan la información implícita en los textos en base a un conjunto arbitrario de palabras, en este estudio la clasificación del sentimiento se realiza mediante algoritmos de Machine Learning, que seleccionan automáticamente las palabras que mejor reflejan los sentimientos optimistas. De esta manera, se busca que la clasificación del sentimiento económico encontrado en los textos sea lo más imparcial y completa posible, basada en patrones y combinaciones de palabras que se encuentran frecuentemente en los textos, y que pueden ser identificadas de forma eficiente y sistemática por los algoritmos. 

El algoritmo se utilizó para identificar el sentimiento económico implícito en las cartas a los accionistas de las empresas del IPSA, y en base a esta clasificación se elaboró el **índice de sentimiento corporativo (ISC)**.

El desarrollo del clasificador se encuentra separado en una serie de notebooks que se describen a continuación:

