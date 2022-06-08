# Bases de datos multimodales





Para poder detectar emociones de forma adecuada a través de la computación afectiva lo más importante es la información. Como se ha visto anteriormente, cada sensor o sistema es capaz de proporcionar ciertas medidas de los marcadores afectivos de un usuario. El objetivo final es tener información lo más completa posible, teniendo en cuenta que las emociones están afectadas por una gran multitud de factores como edad, género o cultura. Obtener el estado emocional a través de un solo canal de información proporciona información poco concreta.

La solución que se ha dado a esta situación las bases de datos multimodales. Bases de datos que contienen representaciones de reacciones afectivas a través de distintas metodologías. Estas bases datos ofrecen una mayor riqueza de los datos al contrastar emociones a través de distintos canales.

Los desarrolladores e investigadores tienen que tomar la decisión de hacer uso de las bases de datos que ya se han creado o crear las suyas propias. Cada investigación o producto tienen requerimientos propios que afectarán a que tipo de datos tendrán acceso o que sensores tendrán la capacidad de utilizar. En este punto, los desarrolladores necesitan tomar la decisión en función de que sensores tengan acceso, si las bases de datos disponibles ofrecen la diversidad demográfica que requieren o si tamaño de la muestra es suficiente [32], [35], [44].

Independientemente de si se tiene acceso a una base de datos que encaja o no con el proyecto o se requiere de producir una propia, hay ciertos factores que tener en cuenta.

## Disponibilidad

​                               

Fig. 23 evolución del uso de bases de datos multimodales. A: Audio, T: Text, V: Video[32]

Aunque la disponibilidad de las bases de datos multimodales está en crecimiento, aún se muestran escasos. Las bases de tos más populares son de tipo visual y sonoro. Otros tipos de bases de datos son mucho menos comunes. 

Parte de esta mayor disponibilidad viene de la accesibilidad a una cámara y plataformas de video como Facebook, Youtube o TikTok. La gran cantidad de datos hace que especialmente atractivos para muchos investigadores.

Unos de los factores más importantes es que sujetos son monitorizados durante la creación de las bases de datos. En sistemas multimodales relacionados, detección de mociones a través del habla afectará tanto el idioma como el origen y la lengua materna del usuario. Si los sistemas solo tienen acceso a una lengua, estos estarán limitados a esa lengua. El origen étnico puede suponer un factor relevante en la elección de las bases de datos, ya que una base de datos centrada en una población étnica puede generar sesgo de la información. Aunque la información de los sujetos es de gran importancia, la metainformación no suele contener más datos que la edad o el género, haciendo el análisis contextual prácticamente imposible.

En el caso de la construcción de una base de datos propia, los investigadores deberán enfrentarse a la paradoja del observador [8] . Por el cual los propios sujetos intentaran esconder sus emociones al ser observados. La publicación de los datos supondrá un acuerdo con los sujetos para ser accesible para otros investigadores. Mientras que datos de tipo más impersonal como ritmo cardiaco o actividad cerebral son suelen ser más fáciles de publicar, otras fuentes de datos que permitan la identificación del usuario harán más complicado obtener su consentimiento.

La publicación de los datos podría aumentar aún más la paradoja del observador ampliando la ratio de error.

Por otro lado, los instrumentos raramente estarán integrados en un mismo sistema, por lo que tendrán que ser sincronizados. El uso de marcadores de tiempo es la técnica más común de sincronización, aunque habrá que adaptar la escala de tiempo.

## Calidad de la muestra

Un segundo factor en la elección de la información es la calidad y cantidad de los datos. En casos en las que los investigadores requieran de hacer una base de datos propia habrá que tener en cuenta el volumen de datos requeridos y que, estos tendrán que ser analizado y etiquetado por personal cualificado y variado.

La calidad de los datos dependerá de las necesidades de la investigación. Algunos de los factores que afectaran a la calidad de estos datos será desde en que medio se han obtenido los datos y si se han tratado de forma adecuada eliminando ruido.

Una vez más también será un factor que valorar la diversidad étnica y de género de los etiquetadores de estas emociones pera obtener un alto estándar de calidad.


## Bases de datos visual y sonora

Las bases de datos con contenido visual son las más comunes debido a la popularización de las redes sociales y la generación de contenido por los usuarios. Este tipo de bases de datos se suelen crear a través de dos vías.

\1.   Videos naturales: se selecciona videos extraídos de plataformas de video como YouTube, Vimeo, Facebook y se marcan las emociones.

\2.   Grabaciones de actores: se proporciona a actores un guion con claras guías de que emoción tienen que simular en cada momento. Estas bases de datos sufren de acciones que no son propias de las emociones que están actuando. Los actores simulan las acciones, no sienten la emoción, por lo que la información suele ser poco precisa.

Aunque existen gran multitud de bases de datos multimodales, cada una de estas siguen sistemas de marcaje distinto. Normalmente, se siguen sistemas lineares como el modelo de Russel (Valencia y Excitación) o bien las emociones básicas de Ekman (felicidad, ira, asco…). Aunque estos dos modelos son los más comunes, hay otros basados en la rueda de emociones de Plutchik o Fontaine que siguen un modelo de 4 dimensiones (Valencia, potencia, excitación, predictibilidad). 

Los distintos datasets siguen los requerimientos de las teorías emocionales en las que se basan. Mientras que algunas teorías se pueden llegar a traducir de una a la otra, o investigadores deben hacer una investigación previa de marcaje es óptimo para elegir la base de datos.

Algunos ejemplos de bases de datos multimodales:

| Nombre           | Año publicación | Autor       |                                                              |
| ---------------- | --------------- | ----------- | ------------------------------------------------------------ |
| Youtube Dataset  | 2011            | Morency     | Tri-modal sentiment análisis (visual, sonoro  y textual). 47 videos (divididos entre 20 videos con mujeres y 27 con  hombres), edades entre 14 y 60 años. El marcaje se ha basado en sentimientos  positivos, negativos y neutros (Valencia). |
| MOUD dataset     | 2013            | Perez-Rosas | Videos grabados en castellano. 80 videos, 65  mujeres, 15 hombres. Edades entre 20 y 60 años. Estos videos han sido  seccionados en fragmentos de aproximadamente 5 segundos. Estos fragmentos han  sido marcados a través de la Valencia (positivo, negativo o neutro) |
| ICT-MMO database |                 |             |                                                              |
| SEMAINE project  |                 |             |                                                              |
| eNTERFACE        |                 |             | 40 sujetos son grabados y clasificados en  base a las emociones básicas de Ekman |
|                  |                 |             |                                                              |

 

## Bases de datos unimodales

Las bases de datos unimodales son la base de las multimodales, y aunque generalmente menos precisas, en algunos escenarios solo se puede obtener una única fuente.

## Bases de datos con contenido captura Psicológica

Aunque mucho menos comunes, existen bases de datos que junta grabaciones audiovisuales contienen información de otro tipo de sensores como EDA o EGG.

Algunos datasets destacables son los siguientes:

| Nombre      | Año publicación | Autor                   |                                                              |
| ----------- | --------------- | ----------------------- | ------------------------------------------------------------ |
| QMUL-UT EEG | 2009            | Koelstra,Muehl y Patras | 17 participantes son visualizan videos que  generan distintos tipos de emociones mientras que son grabados con distintos  sensores. Sensores: EDA, EOG (electrooculography), ritmo cardiaco,  respiración y temperatura. |
| DEAP        |                 | Koelstra                | 32 participantes son grabados reaccionando a  videos mientras son monitorizados con otros sensores. EEG y clasificación de  las emociones de los propios participantes. |
| RECOLA      | 2013            | Ringeval                | 46 sujetos son grabados durante una  conferencia. El data set proporciona información en video, ECG, EDA, audio.  & anotadores marcaron las emociones en base a valencia y excitación. |
| MAHNOB-HCI  | 2012            | Soleymani               | grabación de 30 participantes desde 6 puntos  distintos. Además, el sujeto es monitorizado con: ECG, EEG, EDA, respiración  y temperatura. |

 



 