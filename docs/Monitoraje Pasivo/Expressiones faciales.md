# Expresiones faciales

La detección de expresiones faciales es actualmente el sistema más popular debido al fácil acceso a cámaras. A través de la popularización de los teléfonos inteligente y la mejora de tratamiento de imágenes y sensores fotográficos ha hecho que la detección facial se convierta en una vía de reconocimiento muy atractiva.

Las expresiones faciales no son reflejos fiables de la emoción, sí que el fácil acceso permite la creación de productos dirigida a consumidores que ya poseen este hardware. Además del fácil acceso, el crecimiento de las redes sociales ha permitido bases de datos que han mejorado la detección facial.

## Factores a tener en cuenta en la captura

Hay diversos factores importantes a tener en cuenta en esta técnica. Las cámaras normales dependerán de las condiciones lumínicas de la captura. La captura bajo situaciones de baja o excesiva iluminación genera complicaciones en la captación de imágenes. No todas las cámaras utilizan el mismo sensor, por lo que algunas cámaras serán capaces de captar más luz a causa de su apertura focal. Algunos de los factores determinantes del hardware que pueden afectar a la captura son:

* Resolución
* Apertura focal
* Capacidad de procesamiento
* Sistema operativo
* Tiempo de apertura

La captura de imágenes a altos fotogramas o altas resoluciones es un proceso intensivo en la CPU, por lo que algunos dispositivos podrían mostrar dificultades al capturar (y reconocer si se hace en tiempo real). En el caso de dispositivos móviles se debe tener en cuenta tanto la batería como el sobrecalentamiento. La batería puede sufrir si se hacen grabaciones prolongadas, lo cual reduce el tiempo de vida del dispositivo. El sobrecalentamiento prolongado generada tres problemas. El primero es la reducción de velocidad de reloj de la CPU, el cual provocara la caída de fotogramas de la grabación, empeorando la calidad. El segundo es la sensación de malestar en usuarios si deben sujetar el teléfono inteligente a según que temperaturas (los smartphones pueden llegar hasta los 60º C) y finalmente el calentamiento puede dañar a la batería y acortar su vida.

## Detección facial

El primer paso de la detección de las expresiones faciales pasa por la detección de la propia cara y hacer ajustes para localizar puntos de interés como los ojos o los labios. Hay múltiples técnicas que cumple el mismo objetivo:

* Active Apperearance Model AAM
* Optical Flow model ASM
* Active Shape Model ASM
* 3d Morphable Model 3DMM
* Muscle-Based Model MBM
* 3D Wireframe model 3DM
* Elastic net model
* Geometry based model
* 3d contrained local model
* Generalized Adaptative View-baed Model

Los dos sistemas más usados actualmente son AAM y CLM[40]. Mientras que AAM obtiene mejor precisión, este tiene que ser entrenado persona a persona, mientras que CLM es una generalización del AAM que reduce su precisión, pero permite la generalización[35]

El sistema de CLM funciona de forma similar a AAM por el cual se crea un maya bidimensional que se adapta a la cara del usuario. En el caso de CLM este se genera entrenando a un modelo con caras marcadas previamente con las emociones. La textura del modelo se produce normalizando las distintas caras en cada rasgo por parches.

### APIS de reconocimiento

| Nombre       | Descripcion | Link |
| ------------ | ----------- | ---- |
| Emotient     |             |      |
| Imotions     |             |      |
| EmoVU        |             |      |
| nViso        |             |      |
| Kairos       |             |      |
| Face reader  |             |      |
| Sightcorp    |             |      |
| SkyBiometric |             |      |

