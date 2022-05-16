# Computación Cooperativa



En 2007 Kirsten Boehner et al publico un articulo que plantea una prospectiva distinta al punto de vista cognitivo. Este punto de vista viene a redefinir la computacion afectiva y como se estaba desarrollando hasta ese momento.

Para comprender los motivos por los que se planteo esta teoría casi antitética es importante destacar las criticas a la computacion afectiva cognitiva.

* Se considera que se ha intentado crear unas normas lógicas para el estudio de emociones intrínsecamente ilógicas. Los sistemas de información cerrados no son capaces de mostrar el rango de las emociones.
* Las diferencias culturales marcan tanto la percepción de las emociones como la reacción a estas. La generalización de estas lleva a sesgos de información importantes.
* Un usuario observado nunca mostrara su verdaderas intenciones a causa de la paradoja del observador.
* La detección de emociones es variable por gran cantidad de aspectos como cultura, estado fisco, mental...
* El usuario requiere una monitorización constante.



Estos puntos hicieron que la propia conceptualizacion de la computacion afectiva y como se desarrollava pasara a ser erronea y por tanto debia de ser rediseñada de arriba abajo.



## Co-experiencia



La solucion al problema de la computacion cognitiva pasaba por un proceso de comparticion de las emociones de los usuarios. Los usuarios dejaban de ser analizados por sensores apra detectar sus emociones, sino que los propiso usuarios formavan parte de la experiencia emocional.

Dentro de esta prespectiva el usaurio tiene una posicion central en su experiencia. El usuario trabaja de forma activa con el software para mejorar su experiencia.

``` mermaid
graph LR
  A[Usuario] --> B[UI];
  C[Asistencia emocional]
 D[Detección pasiva]
 D-->A
 D-->C
 C[Canvios en la UI]--> B

```
!!! note annotate "Computación Cognitiva"

    Bajo esta linea de diseño el usuario nunca es participe de su experiencia emocional. El sujeto siempre es pasivo a su experiencia con la UI. Si la UI falla en la deteccion nunca sera asistido, mientras que los falsos positivos pueden generar fustración al recibir reacciones inadequadas.




``` mermaid
graph LR
  A[Usuario] -->|Me siento frustrado| B[UI];
  C[Asistencia emocional]
  B-->C
  C-->|Si requiere ayuda puede acceder a los FAQs|A
  
  
```
!!! note annotate "Computación Cooperativa"

    En la experiencia el usuario siempre es participe de sus propias necesidades y se requiere de input activo.
    
    
