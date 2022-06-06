# Contenido adaptativo en base al estado emocional



## Que es

El objetivo del patrón es adecuar el contenido al estado emocional proporcionando una experiencia distinta cada vez que se experimenta al mismo tiempo que se puede conectar de manera más profunda con el usuario.

## Cuando usarlo

Se propone una solución basada en productos que hagan uso de timelines como el video, la música y hasta cierto punto algunos videojuegos.

## Porque

El contenido adaptativo permite una mayor inmersión con el usuarios al mismo tiene que obtiene una experiencia personalizada. Además de mejorar la experiencia a nivel personal aumenta la reversibilidad del contenido.

## Como

El estado emocional que interesa dentro de la experiencia es como el usuario reacciona al contenido, de esta manera siempre empezara con un contenido de tipo neutro, es decir que no está inclinado hacia ninguna emoción. A partir de cierto periodo de tempo, el diseñador deberá a través de una marca de tiempo deberá indicar un punto de detección emocional. Este punto no tiene que ser un corte en seco, sino que es un intervalo de tiempo que sirve para que el usuario o sistema de detección tenga tiempo para obtener los datos y tomar la decisión pertinente.


<figure markdown>
  ![music track](assets\music track.png)   
  <figcaption>Image caption</figcaption>
</figure>



Como se ha comentado el intervalo de decisión deberá ser amplio ya que esta decisión podrá ser tomada de dos formas:

*  Forma pasiva: el sistema de detección vendrá de algún tipo de sensor que proporcionará la aplicación con la información del estado emocional. Se deberá tener en cuenta el tiempo de detección para ver como de grande tiene que ser el intervalo proporcionado. En ocasiones el sistema no será capaz de proporcionar una respuesta lo suficiente rápida para la interacción o bien la emoción es neutra/no valida, por ello, los diseñadores deberán proporcionar una pista por defecto o bien dar una pista para cuando esto suceda.

*  Forma activa: el usuario introduce de forma voluntaria el camino que quiere seguir. A través de un proceso de selección de la pista o de utilizar una herramienta de cooperación con la aplicación. Las formas en las que se puede introducir son amplias y pueden ir desde una selección de opciones a experiencias más interactivas que permitan mayor conexión con el usuario. Sistemas más complejos tienen la capacidad de mejorar la experiencia a costa de mayor riesgo de fallar y de aumentar la dificultad de diseño.

El uso de un sistema de estas características puede permitir que el usuario se sienta mas conectado con el contenido consumido al mismo tiempo que se le ofrece una experiencia que se puede experimentar múltiples veces.

Mientras que en el ejemplo se muestran expresiones de miedo, tristeza o felicidad se pueden utilizar otras emociones primarias como secundarias. Otras emociones como aburrimiento, envidia o excitación pueden ser más adeudadas en función del tipo de contenido y de las emociones que se pretenda generar. El uso de sistemas flexibles que permitan de emociones fuera de las primarias es fundamental para la flexibilidad de la experiencia. El diseño de estas experiencias vendrá dado por los creadores de contenido y por tanto estará fuertemente influenciado por su contexto social y cultural por los usuarios podrían no compartir la visión del autor.

El tipo de cambios que se pueden ofrecer dos de dos tipos:

* Satélite: los sucesos satélites son pequeñas decisiones o cambios que ejerce el usuario en la trama a través de el estado emocional que genera cambios pequeños que no alteran la trama. Estos sucesos pueden ofrecer pequeños cambios en el dialogo o información adicional que hace que el usuario se sienta mas conectado con el contenido sin tener que hacer grandes cambios a nivel de producción.
* Significativos: estas adaptaciones son las mas complejas ya que pueden crear inconsistencias en el guion, son mas complejas de producir al tener un impacto mucho mayor en la trama. Los sucesos significativos son los que harán de una experiencia única pero también son los mas costosos.

Un balance entre sucesos satélite y significativo ofrecerán una mejor experiencia al mismo tiempo que no disparan los costes de producción de el contenido.

La creación de este tipo de experiencias tiene dos problemas principales, el espacio en memoria y el tiempo de creación de este contenido.

Si un creador de contenido tiene como objetivo crear un video de 10 minutos a 1080p 25fps este tendría un peso de 600mb en total una vez comprimido. Supongamos que el tiempo de producción de este video es de 3 horas cada 10 min de video producido, 18 min por cada minuto producido.

En el caso que este mismo creado de contenido quiere crear este mismo video, pero implementar este patrón añadiendo en cada corte dos emociones más una pista de emoción neutra. En el video hay 3 cortes de 2 minutos con 4 minutos comunes en todas las experiencias. El resultado es que el video ha pasado de 10 minutos a 22 minutos de duración total entre todas las pistas (4 minutos de video en común + (3 cortes*3pistas*2minutos cada pista) =22minutos). Con estos cambios el peso total del video ahora es de 1.32GB y el tiempo de producción es de 6 horas y 36 minutos. Todo esto sin tener en cuenta el tiempo que supone marcar los intervalos y el tiempo adicional de crear un video que utilice este patrón.

Mientras que este patrón permite un mayor grado de interacción entre el usuario y el contenido que consume se hace a costa de unos tiempos mucho mayores y de pistas que quizás nunca sean vistas por el usuario.

## Ejemplos

Bandersnatch es una película interactiva que ofrece cierta personalización con el usuario a través de las decisiones que este toma por algunos personajes de la historia. 

![bandersnatch](assets\bandersnatch.jpg)

La película está dividida en decisiones en su mayoría de tipo satélite, con algunas verdaderamente relevantes que ofrecen cambios significativos en la trama.

![bandersnatch diagram](assets\bandersnatch diagram.webp)

