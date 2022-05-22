# Dificultad adaptativa



## Que es 

La dificultad tiene como objetivo hacer que el usuario entre en un estado de Flow, un estado de alta concentración que comúnmente se asocia a la diversión. El estado del Flow se puede entender entre el equilibrio entre el desafío que se le presenta al usuario con la habilidad que tiene el jugador. Si la dificultad es mucho mayor que a la habilidad del jugador este sentirá frustración mientras que si la habilidad es inferior este se aburrirá. El objetivo de todo diseñador es mantener al jugador en la zona de Flow, equilibrio entre habilidad y dificultad.

## Cuando

La teoría del flow se puede usar en juegos y en aplicaciones que añadan algún tipo de gamificación como duolingo o soloLearn. Hacer que los usuarios entren el estado de flow les hará mas eficientes al estar altamente concentrados.

## Porque

La teoria del flow se ha utilizado frecuentemente en videojuegos por generar atención en el usuarios y por mejorar el aprendizaje de las mecánicas y sistemas. 

EL mayor problema de la teoría del flow es que no todos los usuarios son iguales y vienen con las mismas habilidades previas. A causa de esto diseñar una sola progresión de dificultad puede llevar a algunos usuarios a encontrarse muy frustrado mientras que otros pueden encontrarse con una progresión muy lenta y aburrida.

En ambos casos esto puede llevar a el abandono del juego o aplicación.



<figure markdown>
   ![flow-theory](assets\flow-theory.png)
  <figcaption>Diagrama del flow</figcaption>
</figure>

## Como

### Dificultad adaptativa parametrizada:

El sistema parametrizado utiliza las estadísticas de las entidades para adaptar la dificultad del juego. El diseñador determinara unos valores base con los que se iniciará el juego, a medida que el juego progrese y se obtenga información del usuario se decidirá si las estadísticas de las entidades tienen que ser mejoradas o empeoradas.

Para hacer esto el diseñador deberá determinar cuatro intervalos de valores. El primer valor son las estadísticas base con las que empezara el juego y que se mantendrán hasta que se determine si está en Flow. El segundo es el escalado base, este intervalo de escalado es el de más pendiente y hará cambios más drásticos en las estadísticas para determinar un punto ideal para el jugador. El segundo es el soft-cap, este intervalo es una deceleración moderada del escalado de las estadísticas, permite que los valores no se eleven o disminuyan de forma descontrolada, pero manteniendo cierto escalado. Finalmente tenemos el hard-cap, el cual reduce drásticamente la pendiente hasta un valor máximo o mínimo. 

Mientras que el soft-cap es útil para hacer la transición del escalado base a el valor máximo/mínimo, el hard-cap es fundamental para evitar que haya valores desproporcionados que desequilibren demasiado a los jugadores

|           | Estadísticas base | Escalado base                                               | Soft-Cap                                                     | Hard-Cap                                                    |
| --------- | ----------------- | ----------------------------------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| Velocidad | 5 m/s             | 2.5-7 m/s (menos dificultad)  5-11.5 m/s (mayor dificultad) | 1.5-2.5 m/s (menos dificultad)  5-12.5 m/s (mayor dificultad) | 2.5-7 m/s (menos dificultad)  5-11.5 m/s (mayor dificultad) |

<figure markdown>
   ![crecimiento dificultad](assets\crecimiento dificultad.png)
  <figcaption>Visualización de como escalan las estadísticas</figcaption>
</figure>

Los caps se pueden interpretar con la cantidad de usuarios que deberían poder acceder a ciertos niveles de dificultad. La distribución debería ser parecida a la de una distribución normal, donde la gran mayoría de jugadores estarían dentro de las estadísticas base o del escalado base. Los jugadores con baja habilidad o alto rendimiento deberían ser los únicos en llegar al softcap, mientras que el hard-cap existe como medida de seguridad y prácticamente ningún jugador debería llegar.


<figure markdown>
   ![normal distribution](assets\normal distribution.png)
  <figcaption>Distribucion de los usuarios en funcion del escalado</figcaption>
</figure>

Este patron donde se modifican los valores proporciona una adaptabilidad moderada de la jugabilidad y puede servir tanto para potenciar al jugador como para reducir la dificultad de los enemigos. 

El objetivo aun así siempre será mejorar la experiencia del usuario, por lo que si se escala de forma muy agresiva una sola estadística será visible para el jugador, lo que puede romper la inmersión y molestar a algunos jugadores. Con el objetivo de disminuir esta sensación se recomienda el uso de varias estadísticas que se escalen de forma simultánea con una cola de prioridad. 

En esta cola se establecerán que estadísticas se tienen que disminuir o aumentar de forma prioritaria (normalmente las que suelen inducir a mayor dificultad) y se escalaran por orden. De esta manera siguiendo esta cola de prioridad donde el jugador está teniendo dificultades:

* Puntos de vida

* Daño

* Cadencia de fuego

* Velocidad

Primero el juego deberá reducir la vida del enemigo. Una vez se haya reducido la vida hasta cierto valor se reduce el siguiente. Cuando se hayan reducido todos los valores se proseguirá a reducir de nuevo el primer valor. El objetivo es que todas las estadísticas se reduzcan de forma uniforme y sean consistentes dentro de su nivel de dificultad.

Algunas aplicaciones fuera del videojuego que utilicen este control dinámico:

* Tiempo que se proporciona a estudiantes a resolver un ejercicio.

* Cantidad de ejercicios y dificultad que se da en un ejercicio.

## Ejemplos

Nevermind es un juego desarrollado para PC lanzado en 2015 que hace uso de un sensor de ritmo cardiaco para adaptar las situaciones al jugador final.

<figure markdown>
   ![nevermind](assets\nevermind.png)
  <figcaption>Nevermind</figcaption>
</figure>