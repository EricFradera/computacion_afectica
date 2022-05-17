# EDA

También conocido como "electrodermal activity", GSR "galvanic skin response". El sensor funciona calculando las variaciones de **conductividad en la superficie de la piel**. La licitación de algunas emociones activa el sistema simpático el cual activa las glándulas sudoríparas de la piel. El sensor utiliza estas variaciones de sudoración para observar l**as variaciones en arousal**.

Los sensores de actividad galvánica se deben colocar en lugares **sensibles a sudoración** como dedos. Actualmente se pude usar en las muñecas, el cual facilita su uso en gran medida. Para mejorar la detección se pude hacer uso de gel, el cual ayuda a detectar los variaciones en sudoración. Los datos obtenidos suelen ser muestras con con mucho ruido, por lo que se debe aplicar filtros que eliminen el ruido para tratar los datos.

![electrodermal-activity-eda-sensor_1_540x](assets\electrodermal-activity-eda-sensor_1_540x.jpeg)

## Sensores recomendados:

| Nombre del sensor             | Descripción                                                  | Precio | Link                                                         |
| ----------------------------- | ------------------------------------------------------------ | ------ | ------------------------------------------------------------ |
| BITALINO Electrodermal Sensor | Compatible con Arduino                                       |        | [BITALINO](https://www.pluxbiosignals.com/collections/sensors/products/electrodermal-activity-eda-sensor?variant=40886949118143) |
| BioSignalPlux EDA sensor      | Sensor orientado a la investigación medica. Proporciona datos tratados o sin tratar en función de las necesidades del investigador. Incluye integración con biosignalplux aquisition system. |        | [BioSignalPlux EDA sensor](https://www.pluxbiosignals.com/collections/biosignalsplux/products/electrodermal-activity-eda-sensor-1) |
| Biopac Student Lab            | Gold standart de los sensores EDA. Versión de estudiante     |        | [Biopac Student Lab](https://www.biopac.com/product/low-voltage-stimulator-bsl-mp35/#product-tabs) |
| EDAMove 3                     | Permite la integración fácil con bluethooth i incluye un acelerómetro. Ideal para aplicaciones que requieren de movilidad |        | [EDAMove 3](https://www.movisens.com/en/products/eda-and-activity-sensor-move-3/) |

## Recomendación:

En base al siguiente articulo: 

*D. Batista, H. Plácido da Silva, A. Fred, C. Moreira, M. Reis, y H. A. Ferreira, «Benchmarking of the BITalino biomedical toolkit against an established gold standard», Healthcare Technology Letters, vol. 6, n.º 2. Institution of Engineering and Technology (IET), pp. 32-36, mar. 21, 2019. doi: 10.1049/htl.2018.5037.*

+ Se recomienda el uso de **BITALINO** en proyectos de pequeña **bajo presupuesto** o proyectos para estudiante.

+ En caso de proyectos de **mayor envergadura BIOPAC** ofrece mejores resultados i un mayor soporte debido a estar orientado a la investigación.

