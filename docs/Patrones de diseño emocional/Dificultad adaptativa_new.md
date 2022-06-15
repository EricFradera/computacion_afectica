# Dificultad adaptativa



## Que es 

La dificultad tiene como objetivo hacer que el usuario entre en un estado de Flow, un estado de alta concentración que comúnmente se asocia a la diversión. El estado del Flow se puede entender como el equilibrio entre el desafío que se le presenta al usuario con la habilidad que tiene el jugador. Si la dificultad es mucho mayor a la habilidad del jugador este se frustra mientras que si la habilidad es inferior se aburre. El objetivo de todo diseñador es mantener al jugador en la zona de Flow, equilibrio entre habilidad y dificultad.

## Cuando

La teoría del flow se puede usar en juegos y en aplicaciones que añaden algún tipo de gamificación como duolingo o soloLearn. Hacer que los usuarios entren en estado de flow les hará más eficientes al estar altamente concentrados.

## Porque

La teoría del flow se ha utilizado frecuentemente en videojuegos por generar atención en el usuario y por mejorar el aprendizaje de las mecánicas y sistemas. 

El mayor problema de la teoría del flow es que no todos los usuarios son iguales y vienen con las mismas habilidades previas. A causa de esto diseñar una sola progresión de dificultad puede llevar a algunos usuarios a encontrarse muy frustrado mientras que otros pueden encontrarse con una progresión muy lenta y aburrida.En ambos casos esto puede llevar a el abandono del juego o aplicación



<figure markdown>
   ![flow-theory](assets\flow-theory.png)
  <figcaption>Diagrama del flow</figcaption>
</figure>

## Como

### Dificultad adaptativa parametrizada:

El sistema parametrizado utiliza las estadísticas de las entidades para adaptar la dificultad del juego. El diseñador determina unos valores base con los que se inicia el juego, a medida que el juego progresa y se obtiene información del usuario se modifican las estadísticas de las entidades que tienen que ser mejoradas o empeoradas.

El diseñador debe determinar cuatro intervalos de valores. El primer valor son las estadísticas base con las que empezar el juego y que se mantienen hasta que se determina si el jugador está en Flow. El segundo es el escalado base, este intervalo de escalado es el de mayor pendiente y hace cambios más drásticos en las estadísticas para determinar un punto ideal para el jugador. El segundo es el soft-cap, este intervalo es una reducción moderada del escalado de las estadísticas, permite que los valores no se eleven o disminuyan de forma descontrolada, pero aun con cierto escalado. Finalmente tenemos el hard-cap, este reduce drásticamente la pendiente hasta un valor máximo o mínimo. 

Mientras que el soft-cap es útil para hacer la transición del escalado base al valor máximo/mínimo, el hard-cap es fundamental para evitar que haya valores desproporcionados que desequilibran demasiado el juego.

|           | Estadísticas base | Escalado base                                               | Soft-Cap                                                     | Hard-Cap                                                    |
| --------- | ----------------- | ----------------------------------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| Velocidad | 5 m/s             | 2.5-7 m/s (menos dificultad)  5-11.5 m/s (mayor dificultad) | 1.5-2.5 m/s (menos dificultad)  5-12.5 m/s (mayor dificultad) | 2.5-7 m/s (menos dificultad)  5-11.5 m/s (mayor dificultad) |

<figure markdown>
   ![crecimiento dificultad](assets\crecimiento dificultad.png)
  <figcaption>Visualización de como escalan las estadísticas</figcaption>
</figure>

Los caps se pueden interpretar con la cantidad de usuarios que pueden acceder a ciertos niveles de dificultad. La distribución debe ser parecida a la de una distribución normal, donde la gran mayoría de jugadores están dentro de las estadísticas base o del escalado base. Los jugadores con baja habilidad o alto rendimiento deberían ser los únicos en llegar al softcap, mientras que el hard-cap existe como medida de seguridad y prácticamente ningún jugador debe llegar. 


<figure markdown>
   ![normal distribution](assets\normal distribution.png)
  <figcaption>Distribucion de los usuarios en funcion del escalado</figcaption>
</figure>
En este patrón se modifican los valores de las estadísticas proporcionado una adaptabilidad moderada de la jugabilidad y puede servir tanto para potenciar al jugador como para reducir la dificultad de los enemigos. 

El objetivo aun así siempre es mejorar la experiencia del usuario, si se escala de forma muy agresiva una sola estadística se hace visible para el jugador, lo que puede romper la inmersión y molestar a algunos jugadores. Con el objetivo de disminuir esta sensación se recomienda el uso de varias estadísticas que se escalan de forma simultánea con una cola de prioridad. 

En esta cola se establecen qué estadísticas se disminuyen o aumentan de forma prioritaria (normalmente por el orden que inducen mayor dificultad) y se escalaron por orden. 

Por ejemplo, un enemigo de un nivel podría tener las siguientes estadísticas:

* Puntos de vida

* Daño

* Cadencia de fuego

* Velocidad

Primero el juego debe reducir la vida del enemigo. Una vez se haya reducido la vida hasta cierto valor se reduce el siguiente. Cuando se hayan reducido todos los valores se vuelve a reducir de nuevo el primer valor. El objetivo es que todas las estadísticas se reduzcan de forma uniforme y sean consistentes dentro de su nivel de dificultad

Algunas aplicaciones fuera del videojuego que utilicen este control dinámico:

* Tiempo que se proporciona a estudiantes a resolver un ejercicio.

* Cantidad de ejercicios y dificultad que se da en un ejercicio.

## Ejemplos

Nevermind es un juego desarrollado para PC lanzado en 2015 que hace uso de un sensor de ritmo cardiaco para adaptar las situaciones al jugador final.

<figure markdown>
   ![nevermind](assets\nevermind.png)
  <figcaption>Nevermind</figcaption>
</figure>