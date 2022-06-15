# EmotionML



En 2006 a través de W3C un grupo de investigación se propuso crear un lenguaje de etiquetado de emociones con el objetivo de marcar estados emocionales, el resultado de esta investigación fue el Emotion Markup Lenguague o EmotionML. Aunque EmotionML no es el único sistema para marcar emociones en interfaces, sí que se ha convertido en un lenguaje sencillo, que funciona sobre estructuras ya conocidas y que tiene suficiente complejidad para ser usado en muchos ámbitos.

El objetivo de EmotionML según sus creadores es el siguiente:

*“Allow a technological component to represent and process data, and to enable interoperability between different technological components processing the data.”*

Con este objetivo, EmotionML han construido un lenguaje basado en XML con variaciones propias para adaptar a las necesidades de la computación afectiva y estudios psicológicos. El lenguaje también soporta tanto sistemas unimodales como multimodales, proporcionando herramientas de sincronización dentro de los bloques XML.

Los principales casos de uso son:

* Anotación de datos.

* Reconocimiento de emociones

* Generación de emociones.

El sistema funciona de forma independiente a la técnica de detección emocional que se use. Es como una capa de abstracción por encima de la propia detección en la que la información se almacena ya procesada. La independencia de los sensores permite la interoperabilidad entre sistemas a través de la estandarización de la sintaxis. 

La ambigüedad de las emociones también está reflejada dentro del lenguaje, ofreciendo la capacidad de marcar varias emociones y con qué probabilidad se cree que es una o la otra. Como los propios creadores comentan: “*Any attempt to standardize the description of emotions using a finite set of fixed descriptors is doomed to failure”.* Por lo que solo se sugiere una estructura, las emociones que se recomienda no son cerradas y pueden ser ampliadas*.*

EmotionML nace fuertemente influenciado por las teorías emocionales más usadas en la computación afectiva. En el propio lenguaje se definen ciertas dimensiones como evaluación, activación o valores de juicio (action tendecies) términos propios de la teoría de la evaluación de Arnold-Lazarus. El uso de estas teorías permite cierta estandarización en el proceso de análisis emocional siguiendo todas las mismas bases. Algunos modelos como OCC pueden ser construidos a través de EmotonML.

 

## Estructura del documento

La raíz del documento es la marca <emotionml>. Funciona como el marcador del inicio del documento. Dentro de este documento se podrá establecer la emoción marcada con <category> con el nombre pertinente y finalmente con un valor “value” (en base 1) donde se especificará la intensidad de la emoción.

En ocasiones se considera que es pertinente establecer varias emociones en un mismo elemento, en este caso se encapsulan el set de emociones dentro del bloque <emotion category-set> 

```
<emotionml version="1.0" xmlns="http://www.w3.org/2009/10/emotionml">
<emotion category-set="http://www.w3.org/TR/emotion-voc/xml#big6">
    <category name="sadness" value="0.3"/>
    <category name="anger" value="0.8"/>
    <category name="fear" value="0.3"/>
</emotion>
</emotionml>
```

 

Otros descriptores de emociones:

* Dimensión: Establece en una escala continua las propiedades básicas de las emociones. Encaja con la teoría de Russell siendo los valores más comunes la valencia y excitación. Aunque estos valores son los más generales, EmotionML permite otros valores como potencia.

```
<emotion dimension-set>
    <dimension name="valance" value="0.2"/><!-- a pretty unfriendly person -->
</emotion>
```

* Appraisal: Permite establecer el objeto que desencadena una emoción.

```
<emotion appraisal-set>
    <appraisal name="suddenness" value="0.8"/>
    <appraisal name="intrinsic-pleasantness" value="0.2"/>
</emotion>
```

 

* Action-tendency: influencia de un sujeto a ciertos estados. Tendencias entre la evaluación y el desencadenante de esta. 

```
<emotion action-tendency-set ">
    <action-tendency name="approach" value="0.7"/>   <!-- get close -->
    <action-tendency name="being-with" value="0.8"/> <!-- be happy -->
    <action-tendency name="attending" value="0.7"/>  <!-- pay attention -->
    <action-tendency name="dominating" value="0.7"/> <!-- be assertive -->
</emotion>
```

 

## Meta-Informacion

* Confidence: todos los descriptores pueden hacer uso de este tag para describir la fiabilidad de que esta emoción sea la que se ha detectado. Este valor es especialmente útil en situación de ambigüedad y es común establecer las distintas emociones que se detectan con su fiabilidad. La fiabilidad se define con un valor de probabilidad en base 1.

```
<emotion dimension-set="http://www.w3.org/TR/emotion-voc/xml#pad-dimensions">
    <dimension name="arousal" value="0.8" confidence="0.9"/>
<dimension name="pleasure" value="0.6" confidence="0.3"/>
</emotion>
```

 

* Expressed-through: marcador que permite establecer el canal por el que se ha detectado la emoción. EmotionML establece una lista de valores que puede ser ampliada por el usuario si se requiere de otros canales. Los canales que ponen son los siguientes: gaze, face, head, torso, gesture, leg, voice, text, locomotion, posture, physiology.

```
<emotion category-set> 
        expressed-through="voice">
    <category name="satisfied"/>
</emotion>
```

 

* Info: este bloque permite añadir estructuras de xml para proporcionar datos no contemplados por el lenguaje.

```
<emotionml xmlns>
    <info>
        <classifiers:classifier classifiers:name="GMM"/>
    </info>
    <emotion>
        <info><origin:localization value="bavarian"/></info>
        <category name="happiness"/>
    </emotion>
</emotionml>
```

 

## Referencias y tiempo

* Reference: permite hacer referencia a algún tipo de documentación externa como un video o audio.

```
<emotion ... >
    ...
    <reference uri="http://www.example.com/data/video/v1.avi?t=2,13" role="expressedBy"/>
    <reference uri="http://www.example.com/events/e12.xml" role="triggeredBy"/>
</emotion>
```

 

* Tiempo absoluto: el tiempo absoluto marca tanto el inicio (<start>) como el final (<end>) de un estado emocional o relacionado con una emoción. Para una mayor precisión el tiempo se expresa en milisegundos y se muestra de forma absoluta, siendo la fecha inicial el 1 de enero de 1970 a las 00:00:00 GMT. Distintos tipos de sensores o grabaciones harán uso de distintas escalas de tiempo o no se harán con tiempo absoluto, por lo que se requiere de la conversión de tiempo en cada caso.

```
<emotion category-set="http://www.w3.org/TR/emotion-voc/xml#big6"
         start="1268647332000" end="1268647334000">
```

 

* Tiempo relativo: el tiempo relativo hace referencia a cuánto tiempo ha pasado desde el inicio de la grabación hasta que se ha producido la emoción. Como el tiempo absoluto, la medida son milisegundos.

```
<emotion category-set="http://www.w3.org/TR/emotion-voc/xml#big6"
         time-ref-uri="#referenceAnger" offset-to-start="2000">
    <category name="surprise"/>
</emotion>
```

 

*  Duración: la duración indica el tiempo que ha pasado desde el punto de inicio hasta el final de la expresión de la emoción. En este caso la emoción ha sido sorpresa y la expresión de esta ha tenido una duración de 130 ms.

```
<emotion category-set="http://www.w3.org/TR/emotion-voc/xml#big6"
         start="1268647200000" duration="130">
    <category name="surprise"/>
</emotion>
```

## Definición de emociones

* Vocabulary: este bloque permite definir set de emociones, dimensiones, action-tendencies o elementos de emociones.

*  Item: cada item es un valor del set.

```
<vocabulary type="category" id="big6">
        <item name="anger"/>
        <item name="disgust"/>
        <item name="fear"/>
        <item name="happiness"/>
        <item name="sadness"/>
        <item name="surprise"/>
    </vocabulary>
```