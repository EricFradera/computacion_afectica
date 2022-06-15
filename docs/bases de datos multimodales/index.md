# Bases de datos multimodales



Para poder detectar emociones de forma adecuada a través de la computación afectiva lo más importante es la información. Como se ha visto anteriormente, cada sensor es capaz de proporcionar ciertas medidas de los marcadores afectivos de un usuario. El objetivo final es tener información lo más completa posible, teniendo en cuenta que las emociones están afectadas por una gran multitud de factores como edad, género o cultura. Obtener el estado emocional a través de un solo canal de información proporciona información poco concreta.

La solución que se ha dado a esta situación son las bases de datos multimodales. Bases de datos que contienen representaciones de reacciones afectivas a través de distintos canales. Estas bases datos ofrecen una mayor riqueza de datos al contrastar emociones a través de distintos canales.

Los desarrolladores e investigadores deben tomar la decisión de hacer uso de bases de datos que ya se han creado o crear las suyas propias. Cada investigación o producto tienen requerimientos propios que afecta a qué tipo de datos se tiene acceso o de que sensores disponen. En este punto, los desarrolladores necesitan tomar la decisión en función de que sensores tienen, si las bases de datos disponibles ofrecen la diversidad demográfica que requieren o si tamaño de la muestra es suficiente.

Independientemente de si se tiene acceso a una base de datos que encaja o no con el proyecto o se requiere de producir una propia, hay ciertos factores que tener en cuenta.



## Disponibilidad



Aunque la disponibilidad de las bases de datos multimodales está en crecimiento, aún se muestran escasos. Las bases de tos más populares son de tipo visual y sonoro. Otros tipos de bases de datos son mucho menos comunes. 

Parte de esta mayor disponibilidad viene de la accesibilidad a una cámara y plataformas de video como Facebook, Youtube o TikTok. La gran cantidad de datos hace que especialmente atractivos para muchos investigadores.

Unos de los factores más importantes es que sujetos son monitorizados durante la creación de las bases de datos. En sistemas multimodales relacionados, detección de mociones a través del habla afectará tanto el idioma como el origen y la lengua materna del usuario. Si los sistemas solo tienen acceso a una lengua, estos estarán limitados a esa lengua. El origen étnico puede suponer un factor relevante en la elección de las bases de datos, ya que una base de datos centrada en una población étnica puede generar sesgo de la información. Aunque la información de los sujetos es de gran importancia, la metainformación no suele contener más datos que la edad o el género, haciendo el análisis contextual prácticamente imposible.

En el caso de la construcción de una base de datos propia, los investigadores deberán enfrentarse a la paradoja del observador [8] . Por el cual los propios sujetos intentaran esconder sus emociones al ser observados. La publicación de los datos supondrá un acuerdo con los sujetos para ser accesible para otros investigadores. Mientras que datos de tipo más impersonal como ritmo cardiaco o actividad cerebral son suelen ser más fáciles de publicar, otras fuentes de datos que permitan la identificación del usuario harán más complicado obtener su consentimiento.

La publicación de los datos podría aumentar aún más la paradoja del observador ampliando la ratio de error.

Por otro lado, los instrumentos raramente estarán integrados en un mismo sistema, por lo que tendrán que ser sincronizados. El uso de marcadores de tiempo es la técnica más común de sincronización, aunque habrá que adaptar la escala de tiempo.



## Calidad de la muestra



Un segundo factor en la elección de la información es la calidad y cantidad de los datos. En casos en los que los investigadores requieren de una base de datos propia hay que tener en cuenta el volumen de datos requerido y que estos tienen que ser marcados por personal cualificado y variado.

La calidad de los datos depende de las necesidades de la investigación. Algunos de los factores que afectan a la calidad de los datos es en qué medio se han obtenido y si se han tratado de forma adecuada eliminando. Por ejemplo, los sensores EDA normalmente deben ser tratados para eliminar el ruido de la captura.

Una vez más hay que valorar la diversidad étnica y de género de los etiquetadores de estas emociones para obtener un alto estándar de calidad.




## Bases de datos visual y sonora

Las bases de datos con contenido visual son las más comunes como resultado de la popularización de las redes sociales y la generación de contenido. Este tipo de bases de datos se suelen crear a través de dos vías.

1. Videos naturales: se seleccionan videos extraídos de plataformas de video como YouTube, Vimeo, Facebook y se marcan las emociones.

1. Grabaciones de actores: se proporciona a actores guías de que emoción tienen que representar en cada momento. Estas bases de datos sufren de acciones que no son propias de las emociones que están actuando. Los actores simulan las expresiones de las emociones que deben representar, pero normalmente no es genuina, por consiguiente, puede ser una representación poco reconocible.

Aunque existen gran multitud de bases de datos multimodales, cada una de estas siguen sistemas de marcaje distinto. Normalmente, se siguen sistemas lineales como el modelo de Russel (valencia y excitación) o bien las emociones básicas de Ekman (felicidad, ira, asco…). Aunque estos dos modelos son los más comunes, hay otros basados en la rueda de emociones de Plutchik o Fontaine que siguen un modelo de 4 dimensiones (valencia, potencia, excitación, predictibilidad). 

Los distintos datasets siguen los requerimientos de las teorías emocionales en las que se basan. Cada investigación sigue el modelo que encaja mejor con su caso de uso. Aunque se puede traducir entre modelos es preferible usar una base de datos basada en la misma teoría de las emociones.



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

 



 