

# Computación basada en la cognición





El punto de vista de Picard se considera cognitivo, ya que la forma en la que se detectan las emociones es de forma pasiva.

Todas las emociones tienen respuestas físicas o motoras en el cuerpo, por lo que una captura precisa de estas debería permitir inferir las emociones.

- El flujo de trabajo base de la computación afectiva desde punto de vista cognitivo es el siguiente:
  
    * Un usuario interactúa de forma normal con una interfaz.
    * Un sistema de detección pasivo capta información en a través de marcadores emocionales, audiovisuales o textuales.
    * Un sistema capaz de interpretar estos marcadores como OCC proporciona el estado emocional.
    * Un sistema de marcaje establece las emociones y la seguridad de que sea esta. 
    * Cada emoción, o conjunto de emociones tiene adjunto un comportamiento o modificación en base al diseño de la interfaz.
    * Se proporciona a la interfaz las modificaciones que debe hacer
    * El usuario experimenta estos cambios o adaptaciones.

``` mermaid
graph LR
  A[Usuario];
  B[Deteccion passiva];
  C[Interfaz]
  D[Sistema de interpretacion de emociones]
  E[Comportamiento en base a emociones]
  F[lista de emociones]
  
  B --> A
  A --> C
  B --> D
  D --> F
  F --> E
  E --> C
  
```





## Implicaciones de la computación orientada a la cognición



El workflow de la computación basada en la cognición tiene en su centro la capacidad de detectar e interpretar las emociones de los usuarios. Debido a que mayoritariamente se propone una detección de tipo pasiva, la eficacia de la tecnología dependerá de la precisión en la detección.

| Ventajas                                                     | Inconvenientes                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Idea para aplicaciones donde se requiere mucha inmersión.    | Algunos dispositivos pueden ser caros.                       |
| Aplicaciones medicas o de deporte donde ya se obtienen datos biométricos por defecto. | La compatibilidad es limitada.                               |
| Perfecto para espacios controlados como laboratorios o estudios de mercado. | Algunos sensores requieren de personal especializado.        |
| Aplicaciones donde el usuario no pueda ejercer una interacción activa como aplicaciones medicas, o conducción. | El propio uso de los sensores implica una invasión de la privacidad importante. |
| Permite mejorar la comunicación de personas con discapacidades. | El propio uso de los sensores implica una invasión de la privacidad importante. |
|                                                              | Algunos sensores solo se pueden usar en espacios controlados como laboratorios mientras que otros no se pueden usar de forma prolongada. |
|                                                              | A causa de la colocación de los sensores se puede llegar a reducir la movilidad del usuario. |

## Trabajo sobre la incerteza

La computacion cognitiva hace uso de sensores médicos por el cual es común ver que se consideran datos objetivos. 

La detección de las los distintos marcadores emocionales nunca implicara necesariamente una emoción. EL objetivo de la computacion cognitiva es dibujar patrones por lo que se puedan inferir emociones. Ahora bien, estas mediciones vendrán afectadas por distintas variables como el estado de animo del usuario, estado físico o psicológico.

Aunque se produzca la detección de ciertos marcadores y se tome la decisión de que el usuario esta experimentado un estado emocional, a no ser que este confirme su estado emocional, la interfaz solo podrá usar este dato como algo incierto. El usuario siempre tendrá la ultima palabra y por este motivo siempre podrá sobrescribir la emoción del usuario.

Además es fundamental adaptar las interfaces de forma sutil y de forma empática. Que se detecte una emoción puede generar la reacción opuesta en el usuario. Por ejemplo que un usuario se le detecte como triste y se hagan acciones que el usuario considera inadecuadas este genera ira y supondrá una enorme frustración con el sistema. El estado emocional de los usuarios es complejo y deberá tratarse siempre con extremo cuidado.



## Sistemas de asistencia

Los sistemas de asistencia son las aplicaciones mas interesantes desde un punto de vista de la computacion afectiva. El abaratamiento de los wearables y la mejora de la vida de la batería y precisión de los sensores ofrece una gran oportunidad para proporcionar a los usuarios de servicios que les mejoren la vida de forma pasiva.

Algunas de estas aplicaciones ya se hacen uso en dispositivos como el apple watch.  Detectar ataques de ansiedad y dar herramientas para contactar con un psicólogo, o ofrecer ejercicios de respiración para aliviar el ataque son algunas de las aplicaciones. Esta monitorización puede usarse para ayudar a personas con distintos trastornos psicológicos a través de acceso rápido a ayuda además de proporcionar mas información de la situación.

Detectar situaciones de emergencia como caídas, paradas cardiacas o demás son aplicaciones que son totalmente posibles con la tecnología actual. Mejorar la calidad de vida y seguridad de los usuarios es uno de los caminos de la computacion cognitiva.

## Recomendación de contenido y marqueting

Una constante detección de forma pasiva de las emociones de los usuarios puede permitir el análisis contante de las reacciones de los usuarios en frente a cierto contenido. Así mismo que un usuario se encuentre en ciertos estados emocionales puede suponer que se reaccione con mas facilidad a cierto estímulos.

Uno de los grandes usos para esto serian la recomendacion de contenido como ya se hace a traves de plataformas como Youtube o TikTok o bien los anuncios que se pueden encontrar en multitud de paginas web.

Aunque este tipo de recomendaciones se posicionan en base de la experiencia emocional del usuario y por tanto aumenta la probabilidad de que sean anuncios destacados las implicaciones éticas y de privacidad de los consumidores queda claramente violadas.

El uso de este tipo de recomendaciones siempre tendría que ir junto a avisos de los usuarios, deberían saber que se esta analizando su estado emocional y se debe ofrecer una alternativa a este tipo de recomendaciones.

## Aplicaciones de la computación cognitiva:

+ Estudios de mercado
+ Investigaciones científicas
+ Automoción (detección de cansancio o humor)
