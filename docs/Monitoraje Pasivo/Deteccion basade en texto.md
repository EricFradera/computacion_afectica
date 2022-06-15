# Detección de emociones basada en texto



Las emociones son una parte fundamental en la comunicación. La comunicación vía texto carece de marcadores emocionales como expresiones faciales o gestos. La intencionalidad de las conversaciones puede perderse con el uso de este canal. Mientras que los humanos suelen ser capaces de comprender las emociones involucradas con un texto, las máquinas carecen de la capacidad de entender el subtexto [60], [61].

La transmisión de información vía texto carece de esta metainformación, por lo que todo el contenido que se quiere transmitir está en el propio texto.

Para transmitir emociones dentro de un texto se puede hacer a través de:

* Hacer explícita la emoción o intención que se quiere transmitir.

* Hacer uso de un vocabulario que haga implícita ciertas intenciones o emociones.

* Utilizar retórica o expresiones literarias para transmitir esta información.

El problema aparece en conversaciones en las que no son dos individuos humanos los que intentan interpretar un texto, sino una máquina que carece de conocimientos sobre el contexto o las emociones del transmisor.

Actualmente, se están planteando dos formas de interpretar emociones en textos. Por un lado, tenemos un análisis con lexicon y, por otro lado, un análisis a través de machine learning.

En el análisis basado en lexicón hace uso de un diccionario en el cual se clasifican las distintas palabras en distintas emociones. Por ejemplo, el NRC lexicón clasifica aproximadamente quince mil palabras en función de emociones de: ira, anticipación, asco, tristeza, felicidad, sorpresa y confianza. En este caso el diccionario funciona de manera binaria asignando 0 o 1 a las palabras. Debido a la polisemia de las palabras, muchas son asociadas con varias emociones.

​                               

![2022-06-15 19_14_17-memoria final - Copy.docx - Word](assets\2022-06-15 19_14_17-memoria final - Copy.docx - Word.png)

El algoritmo de procesamiento del lenguaje elimina caracteres que no aportan significado como pronombres, preposiciones, artículos y demás palabras que no aporten directamente significado. Después de este preprocesamiento inicial se analizan frase por frase para determinar la emoción que más peso tenga. Hay muchas implementaciones e interpretaciones, algunos algoritmos trabajan en función de valencia y excitación, mientras que otros muestran las emociones de forma más granular.

Con los avances en la inteligencia artificial y a través del fácil acceso de las redes sociales, se han creado bases de datos con las que algoritmos de inteligencia artificial han empezado a ser capaces de discernir emociones dentro de los textos. La mayoría de las bases de algoritmos han sido entrenados a través de tuits, comentarios de YouTube, o diálogos de películas que han sido marcados previamente por humanos. Estos datos han sido analizados a través de distintas técnicas de neural network, deep learning o machine learning.

Es común combinar las técnicas de análisis de lenguaje con los de machine learning para obtener mejores resultados. Se preprocesa la información con el NLP para eliminar entradas inconsistentes.

Los resultados que podemos observar en el siguiente estudio son los siguientes.

 

![2022-06-15 19_13_57-memoria final - Copy.docx - Word](assets\2022-06-15 19_13_57-memoria final - Copy.docx - Word.png)

En general se pude observar que las emociones de felicidad e ira son las más sencillas de detectar, mientras que tristeza y miedo son las que ofrecen menos precisión. 

 

#### 1.1.1.1.    Datasets de reconocimiento por texto

| Nombre       | descripción                                                  | Enlace                             |
| ------------ | ------------------------------------------------------------ | ---------------------------------- |
| SemEval      | Consiste en titulares en  inglés y arabe clasificadas en base a las 6 emocione s básicas de ekman | https://semeval.github.io          |
| EmotionLines | Dataset obtenido de  sitcoms y marcados en base a las emocione básicas de ekman | https://arxiv.org/abs/1802.08379   |
| Daily dialog | Frases obtenidas y  marcadas de conversaciones diarias entre usuarios. | https://aclanthology.org/I17-1099/ |

