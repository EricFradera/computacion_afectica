# Patrones de monitoraje



Los patrones de monitorajes son estrategias con las que captar las emociones en momentos concretos. Esta guía ofrece varios patrones y sistemas para mejorar la interacción entre usuarios y interfaces.



## TaskBar notification

Como se ha comentado la detección pasiva es muy invasiva para el usuario. En el caso de hacer uso de algún tipo de sensor del estilo del apple watch es adecuado notificar en que momentos se esta haciendo algún tipo de detección.

Siguiendo la estela de otros fabricantes como Google o Samsung, al hacer uso de algún tipo de sensor este se mostrara en la barra de tareas superior con un icono verde. Mientras este sensor se hace uso aparece en la barra superior junto a una pequeña animación. Cuando pasan unos dos segundos el icono animado se substituye por icono de menor tamaño verde para no molestar al usuario.

El usuario siempre esta al corriente de que aplicación esta obteniendo datos sobre el.

En el caso de recogida de datos indebida el usuario podrá decidir eliminar la aplicación.

El icono deberá mostrarse siempre en el dispositivo que se este usando para activar la funcionalidad. Es decir, si se activa el sensor de actividad cardiaca en el wearable se mostrara el icono en el wearable. En el caso que se active o lo active una aplicación desde un smartphone el icono se mostrara en el smartphone. El usuario **siempre** debe saber si esta siendo monitoreado por una aplicacion.

![ui_permissions](assets\ui_permissions.gif)