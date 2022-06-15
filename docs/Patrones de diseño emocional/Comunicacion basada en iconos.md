# Comunicación basada en iconos

## Que es

Añadir información visual al texto para mejorar la interacción textual entre usuarios.

## Cuando usarlo

Este patrón es especialmente útil en comunicación entre usuarios en las que se carece de información contextual y emocional.

Se puede implementar en cualquier aplicación en la que haya comunicación entre personas como redes sociales, chats, blogs ...

## Porque

Los humanos durante la comunicación verbal transmiten mucha información metatextual. Utilizando las mismas palabras se puede transmitir información distinta solo por utilizar entonaciones distintas, expresiones faciales o postura corporal.

Esta información que se encuentra fuera del texto se pierde en interacciones sociales digitales, lo que obliga al usuario a explicarse cómo se siente continuamente o bien dejar significado por el camino.

Añadir elementos visuales como fuentes, emojis o colores permite a los usuarios crear un léxico con el que transmitir sus emociones entre iguales. En grupos sociales ya se hacen uso de expresiones, emojis con objetivos emocionales por lo que esto crea una estandarización con la que mejorar la comunicación textual.

## Como

La primera tarea es crear un lenguaje propio de la aplicación a través de elementos visuales. Esta iconografía debe asignar a cada emoción que se quiera transmitir uno o varios de los siguientes elementos:

* Color
* Iconos
* Tipografías

Con esta información adicional el usuario puede asociar cada frase o cada palabra con una emoción, mejorando la expresividad. Se aconseja el uso de al menos uno, aunque es mejor una combinación de los tres. Una combinación de las tres mejoras la accesibilidad de la información. El uso de colores supone un problema para usuarios con dificultades visuales, mientras que usuarios con dislexia podrían mostrar dificultades ante el uso de ciertas fuentes. Una combinación de colores, tipografías e iconos ofrece la mayor expresividad y accesibilidad.

Las emociones están afectadas por contextos culturales, sociales e incluso generacionales. Mientras que un emoji puede tener un significado en ciertos contextos en otros pueden tener significados incluso ofensivos. Con el objetivo de tener una experiencia placentera para el usuario, durante el proceso de configuración el usuario tiene que indicar con que símbolos quiere representar que emociones y crear un perfil propio. Con este proceso se puede crear un sistema adaptado al usuario.

A causa de la variedad de posibilidades que la modificación de colores supone se tiene considerar el uso de tonalidades distintas para poder ofrecer al usuario una ratio de contraste de al menos 4:5:1 entre el fondo y el texto. En la figura 25 se puede ver cómo se podrían adaptar los colores para respetar el contraste.

<figure markdown>
  ![color_pattern](assets/color_pattern.png)  
  <figcaption>Ejemplo de perfil de colores que pueden estar asociados a un conjunto de emociones. El uso de tonalidades más oscuras y más claras mejora la visibilidad manteniendo las tonalidades base</figcaption>
</figure>



Podemos observar como el uso de uno o varios sistemas de modificacion de estilo cambian la intencionalidad de el texto:


<figure markdown>
   ![text example](assets\text example.png)
   <figcaption>Ejemplo de cómo se podría mostrar el texto con emociones asociadas</figcaption>
</figure>


En un inicio tanto el emisor cómo el receptor ha creado un perfil para las preferencias de usuario. En este caso mientras que el color se mantiene igual entre los dos usuarios el símbolo y tipografía varía. Cuando el usuario escribe el texto establece el mismo la emoción y los sistemas de representación que quiere añadir. La aplicación puede ofrecer un sistema de detección de emociones vía texto para automatizar el proceso. 

El sistema de detección permite hacer el proceso más rápido a través de sugerencias, que siempre serán seleccionadas por el usuario. El sistema puede intentar agilizar el proceso, pero siempre tiene que trabajar con el usuario. Una vez se hayan seleccionado las emociones al gusto del usuario la aplicación genera un script de marcación con EmotionML o similares donde se indiquen las emociones de cada frase. Con este archivo de marcación y las preferencias del usuario se aplican los símbolos, fuentes y colores asociados con las emociones. Una vez se le presente el texto al usuario con los marcadores emocionales asociados se le dará también la opción de modificar el texto y emociones antes de enviar.

El sistema del receptor funciona de forma similar al del emisor. La aplicación del emisor recibirá el mensaje junto a un sistema de marcación. Con el sistema de marcaje se aplica en base a las preferencias del receptor los símbolos pertinentes.

En esta aplicación el emisor tiene la capacidad de enviar texto con información emocional al receptor sin que los contextos de los usuarios afecten a su percepción.


<figure markdown>
  ![chat example](assets\chat example.png)
  <figcaption>Ejemplo de chat usando el patrón de símbolos</figcaption>
</figure>


El sistema de detección automática de emociones se puede implementar con sistemas distintos. Por un lado, se puede usar la detección de emociones a través de texto con un lexicón como IBM tone anylzer. Otra opción es emplear las expresiones faciales del usuario, aunque esto implica el uso de la cámara y puede no mostrar expresiones faciales a causa de que no tiene por qué estar experimentando esta emoción, sino que solo la quiere transmitir. El uso de sensores más complejos como EDA, EGG y demás tiene los mismos obstáculos que la detección facial, además de ser sensores menos accesibles.


