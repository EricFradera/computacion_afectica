

# Computación basada en la cognición





El punto de vista de Picard se considera cognitivo, ya que la forma en la que se detectan las emociones es de forma pasiva.

Todas las emociones tienen respuestas físicas o motoras en el cuerpo, por lo que una captura precisa de estas debería permitir inferir las emociones.

- El flujo de trabajo base de la computación afectiva desde punto de vista cognitivo es el siguiente:
  
    * Un usuario interactúa de forma normal con una interfaz.
    * Un sistema de detección pasivo capta información en a través de marcadores emocionales, audiovisuales o textuales.
    * Un sistema capaz de interpretar estos marcadores como OCC proporción la información.
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



## Detección en base a la distancia



| Distancia relativa al usuario |                           Sensores                           |
| :---------------------------- | :----------------------------------------------------------: |
| A distancia                   |    Expresiones faciales, Postura, gestos, comportamientos    |
| Cercano                       | Temperatura, Respiración, Dilatación de la pupila, conductividad de la piel, electroencefalograma, presión sanguínea |
| Interno                       |                 Hormonas, neurotransmisores                  |

