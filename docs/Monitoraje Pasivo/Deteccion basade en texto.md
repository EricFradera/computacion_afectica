# Detección de emociones basada en texto



La comunicación vía texto carece marcadores emocionales como expresiones faciales o gestos. La intencionalidad de las conversaciones puede perderse con el uso de este canal. Mientras que los humanos suelen ser capaces de comprender las emociones involucradas con un texto, las máquinas carecen de la capacidad de entender el subtexto.

Actualmente, se están planteando dos formas de interpretar emociones en textos. Por un lado, tenemos un análisis semántico y, por otro lado, un análisis a través de machine learning.

## Análisis semántico



En el análisis basado en natural lenguaje (análisis semántico) hace uso de un diccionario en la cual se clasifican las distintas palabras en distintas emociones. Por ejemplo, el NRC lexicón clasifica aproximadamente quince mil palabras en función de emociones de: ira, anticipación, asco, tristeza, felicidad, sorpresa y confianza. En este caso el diccionario funciona de manera binaria asignando 0 o 1 a las palabras. Debido a la polisemia de las palabras, muchas son asociadas con varias emociones.

<figure markdown>
  ![nrc](assets\nrc.png)
  <figcaption>NRC lexicon</figcaption>
</figure>


El algoritmo de procesamiento del lenguaje elimina caracteres que no aportan significado como pronombres, preposiciones, artículos o palabras que no aporten información emocional Después de este preprocesamiento inicial se analizan frase por frase para determinar que emoción predomina. 



## Machine learning

Con los avances en la inteligencia artificial y a través del fácil acceso de las redes sociales, se han creado bases de datos con las que, algoritmos de inteligencia artificial han empezado a ser capaces de discernir emociones dentro de los textos. La mayoría de las bases de algoritmos han sido entrenados a través de tuits, comentarios de YouTube, o diálogos de películas que han sido marcados previamente por humanos. Estos datos han sido analizados a través de distintas técnicas de neural network, Deep learning o machine learning.

Algunos de los algoritmos más usados son:

Es común combinar las técnicas de análisis de lenguaje con los de machine learning para obtener mejores resultados. Se preprocesa la información con el NLP para eliminar entradas inconsistentes.

Los resultados que podemos observar en el siguiente estudio son los siguientes.

 

Fig. 22 Resultado de análisis de emociones vía texto con distintos algoritmos de inteligencia artificial[42]

En general se pude observar que las emociones de felicidad e ira son las más sencillas de detectar, mientras que tristeza y miedo son las que ofrecen menos precisión. 

## Apis reconocimiento via texto:

|                   |      |      |
| ----------------- | ---- | ---- |
| IBM tone analyzer |      |      |
| Respustate API    |      |      |
| Tone API          |      |      |



## Aplications

| Dominio | Aplicacion | Detalles | Referencia |
| ------- | ---------- | -------- | ---------- |
|         |            |          |            |
|         |            |          |            |
|         |            |          |            |
|         |            |          |            |
|         |            |          |            |
|         |            |          |            |

![2022-06-07 09_31_33-Sci-Hub _ Deep learning for affective computing_ Text-based emotion recognition ](assets\2022-06-07 09_31_33-Sci-Hub _ Deep learning for affective computing_ Text-based emotion recognition .png)
