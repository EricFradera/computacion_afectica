# Monitoraje pasivo

La obtención de datos de forma pasiva proporciona dato sin que el usuario tenga que intervenir en ningún momento de su experiencia con la aplicación. De forma dinámica el usuario se le proporciona el contenido y la información de la manera mas adecuada para el.

El monitoraje de tipo pasivo requiere de sensores que perciban las respuestas física del usuario al experimentar una emoción. Si se hacen uso de sensores siempre implicara un grado de incomodidad y de violación de su privacidad. Cada aplicación deberá valorar si el uso de estos sensores podría condicionar la usabilidad de la app.

## Excitación y valencia

La detección emocional proporciona 2 variables para expresar el estado emocional

* Valencia: expresa si una experiencia emocional es Positiva o negativa.
* Excitación: muestra el grado de interés por la tarea realizada.

Estas dos variables se colocan en el llamado circumplex model of affect diseñado por Russell el cual porporciona distintas emociones en funcion de la emocion que se este sintiendo.

![circumflex model of affect](assets\circumflex model of affect.png)

## Tipos de sensores

cada sensor puede detectar cierta información del usuario que será cartografiado en ese modelo. La mayoría de sensores serán capaz de detectar un valencia o excitación pero no ambos. Cada aplicación debe decidir que opciones son mas adecuadas. 



| Sensores                              | Estado emocional    | Aplicabilidad                                                |
| ------------------------------------- | ------------------- | ------------------------------------------------------------ |
| Ritmo cardiaco                        | Excitación          | Simple i sencillo. Común en muchos wearables.                |
| Presión sanguínea                     | Excitación          | barato y accesible en smartwatches. La señal contiene ruido que debe ser tratado. |
| Electrocardiograma                    | Excitación          | Requiere el uso de electrodos externos en la piel. El equipamiento es caro y requiere de personal especializado. |
| Variación de ritmo cardiaco           | Valencia            |                                                              |
| Electromiografía                      | Valencia            |                                                              |
| Electroencefalograma                  | Valencia/excitación |                                                              |
| Resonancia magnética                  | Valencia/excitación |                                                              |
| Variación de conductividad en la piel | Excitación          |                                                              |

![image-20220516130033219](C:\Users\Eric Fradera\AppData\Roaming\Typora\typora-user-images\image-20220516130033219.png)

## Comparación detección emocional

|                                                        | Intrusividad                                                 | Precisión                                                    | Durabilidad                | Tiempo de detección | Coste                                                        |
| ------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------- | ------------------- | ------------------------------------------------------------ |
| Autoinforme (análisis personal especializad)           | no es intrusivo en la experiencia pero si con el posterior análisis | Buena con el tratamiento correcto. Posibilidad de que los usuarios mientan en como se sienten | No aplica                  | A posteriori        | No implica detección con hardware, pero requiere de horas de personal experimentado |
| Ritmo cardiaco                                         | poco intrusivo con wearables, intrusivo con sensores convencionales | Buena                                                        | Se puede usar a diario     | tiempo real         | muy baratos                                                  |
| Respiracion                                            | Bastante intrusivo                                           | buena                                                        | no útil para el uso diario | tiempo real         | caro                                                         |
| EGG(electroencefalograma), fMRI( resonancia magnética) | Muy intrusivo. Limita movilidad.                             | buena pero sensible a muchos factores                        | frágil                     | tiempo real         | muy caro                                                     |
| Reconocimiento Facial                                  | No, pero requiere de buenas condiciones de luz i de estar en el frame. | buena, pero sencillo de engañar                              | Muy fuerte                 | tiempo real         | Costes de desarrollo o costes de contratación del servicio   |
| Deteccion de postura                                   | No, pero requiere de buenas condiciones de luz i de estar en el frame. | buena, pero sencillo de engañar                              | Muy fuerte                 | tiempo real         | Costes de desarrollo o costes de contratación del servicio   |
| Deteccion de texto                                     | Nada intrusivo                                               | mala                                                         | -                          | tiempo real         | coste de desarrollo                                          |

## Monitoraje en funcion de la distancia de la captura

| Distancia relativa al usuario |                           Sensores                           |
| :---------------------------- | :----------------------------------------------------------: |
| A distancia                   |    Expresiones faciales, Postura, gestos, comportamientos    |
| Cercano                       | Temperatura, Respiración, Dilatación de la pupila, conductividad de la piel, electroencefalograma, presión sanguínea |
| Interno                       |                 Hormonas, neurotransmisores                  |
