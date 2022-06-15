# Contenido adaptativo en base al estado emocional



## Que es

El objetivo del patrón es adecuar el contenido al estado emocional del usuario. Proporciona una experiencia distinta cada vez que se experimenta al mismo tiempo que se puede conectar de manera más profunda con el contenido

## Cuando usarlo

Para productos que hagan uso de timelines como el video, la música y videojuegos.

## Porque

El contenido adaptativo permite una mayor inmersión con el usuario al mismo tiene que obtener una experiencia personalizada. Además de mejorar la experiencia a nivel personal aumenta la reversibilidad del contenido.

## Como

El contenido siempre empieza en un estado neutro. Empezar en estado neutro permite dar personalidad al contenido en los primeros compases, así como esperar la reacción del usuario. En el punto que el creador decida el contenido se divide en distintos caminos en función del estado emocional con el objetivo de crear una experiencia personalizada para cada usuario. Estas divisiones no son inmediatas, sino que son una transición que permiten al usuario expresar cómo se sienten o al sistema de detección pasiva capturar el estado emocional del usuario.


<figure markdown>
  ![music track](assets\music track.png)   
  <figcaption>Image caption</figcaption>
</figure>


Como se ha comentado el intervalo de decisión debe ser amplio ya que esta decisión puede ser tomada de dos formas:

* Forma pasiva: el sistema de detección obtiene a través de un sensor el estado emocional. Se debe tener en cuenta el tiempo de detección para ver como de duradero tiene que ser el intervalo proporcionado. En ocasiones el sistema no es capaz de proporcionar una respuesta a suficiente velocidad para la interacción o bien la emoción es neutra o no válida, por ello, los diseñadores deben proporcionar una pista por defecto.

* Forma activa: el usuario introduce de forma voluntaria el camino que quiere seguir. A través de un proceso de selección de la pista. Las formas en las que se puede introducir son amplias y pueden ir desde una selección de opciones a experiencias más interactivas que permitan mayor conexión con el usuario. Sistemas más complejos tienen la capacidad de mejorar la experiencia a costa de mayor riesgo de fallar y de aumentar la dificultad de diseño.

El uso de un sistema de estas características puede permitir que el usuario se sienta más conectado con el contenido consumido al mismo tiempo que se le ofrece una experiencia que se puede experimentar múltiples veces.

Mientras que en el ejemplo se muestran expresiones de miedo, tristeza o felicidad se pueden utilizar otras emociones primarias como secundarias. Otras emociones como aburrimiento, envidia o excitación pueden ser más adecuadas en función del tipo de contenido y de las emociones que se pretenda generar. El diseño de estas experiencias viene dado por los creadores de contenido y por tanto está influenciado por su contexto sociocultural, que hará que algunos usuarios no conecten su contenido.

El tipo de cambios que se pueden ofrecer dos de dos tipos:

* Satélite: los sucesos satélites son pequeñas decisiones o cambios que ejerce el usuario en la trama a través del estado emocional. Estos sucesos pueden ofrecer pequeños cambios en el diálogo o información adicional que hace que el usuario se sienta más conectado con el contenido sin tener que hacer grandes cambios a nivel de producción.

* Significativos: estas adaptaciones son más complejas ya que pueden crear inconsistencias en el guión a cambio de hacer cambios significativos en la trama. Los sucesos significativos son los que harán de una experiencia única pero también son los más costosos de producir.

Un balance entre sucesos satélite y significativos ofrece una mejor experiencia al mismo tiempo que no se disparan los costes de producción del contenido.

La creación de este tipo de experiencias tiene dos problemas principales, el espacio en memoria y el tiempo de creación de este contenido.

Si un creador de contenido tiene como objetivo crear un video de 10 minutos a 1080p 25fps este tiene un peso aproximado de 600mb una vez comprimido. Si el tiempo de producción de este video es de tres horas cada diez minutos de video, dieciocho minutos por cada minuto producido.

Al implementar este patrón se añaden en cada corte dos emociones más una pista de emoción neutra. En el video hay tres cortes de dos minutos con cuatro minutos comunes en todas las experiencias. El resultado es que el video ha pasado de diez minutos a 22 minutos de duración total entre todas las pistas (cuatro minutos de video en común + (tres cortes*tres pistas* dos minutos cada pista) =22minutos). Con estos cambios el peso total del video ahora es de 1.32GB y el tiempo de producción es de seis horas y 36 minutos. Todo esto sin tener en cuenta el tiempo que supone marcar los intervalos y el tiempo adicional de crear un video que utilice este patrón.

Mientras que este patrón permite un mayor grado de interacción entre el usuario y el contenido que consume se hace a costa de unos tiempos mucho mayores y de pistas que quizás nunca sean vistas por el usuario.

## Ejemplos

Bandersnatch es una película interactiva que ofrece cierta personalización con el usuario a través de las decisiones que este toma por algunos personajes de la historia. 

![bandersnatch](assets\bandersnatch.jpg)

La película está dividida en decisiones en su mayoría de tipo satélite, con algunas verdaderamente relevantes que ofrecen cambios significativos en la trama.

![bandersnatch diagram](assets\bandersnatch diagram.webp)

