# Estructura de la app



La aplicación esta desarrollada utilizando Flutter ver 2.10.  Flutter es un framework construido encima de dart que permite un alto grado de customización visual a través de la construcción de componentes (widgets). 

Los datos han sido gradados en FireBase a causa de la buena integración que tiene flutter con Firebase. Firebase es una base de datos no relacional que ha permitido modificar el tratado de datos hasta el final del desarrollo. Esto ha permitido muy buena flexibilidad durante el desarrollo. 

## Estructura de la aplicación:

Esta es la estructura simplificada de la app. Para mas detalles acceder al repositorio.

``` mermaid
classDiagram
  UserController <|--|> FirebaseController
  UserExpressionThemeController <|--|> FirebaseController
  expressionPageController <|-- UserExpressionThemeController
  AnalyticsController <|--|> FirebaseController
  LogIn <|-- UserController
  Chat <|-- UserController
  ExpressionPage <|-- expressionPageController
  Analytics <|-- AnalyticsController
  FirebaseController <|--|> cloud
  
  class HowItWorks{
  
  }

  class UserController{

  }
  class UserExpressionThemeController{

  }
  class FirebaseController {
  
  }
  class AnalyticsController{
  
  }
  class Log In{
 
  }
```
## Diagrama de sequencia caracteristicas



### Crear perfil de Usuario

``` mermaid
sequenceDiagram
  loop ModifyData
  	Expression Page->>ExpressionPageController: setData(int emotion)
  end
  Expression Page->>ExpressionPageController: saveData(int emotion)
  ExpressionPageController->>ExpressionThemeController: buildTheme(int emotion)
  ExpressionThemeController->> AppTheme: obx(AppTheme)
  AppTheme ->>  Expression Page: Theme.of(context).getColor()
 
```

### Cambiar estado de animo

``` mermaid
sequenceDiagram
  ProfilePage->>UserController: changeMood(int emotion)
  UserController ->> FireBaseController: updadeMood()
  ProfilePage ->> ExpressionThemeController: changeTheme(int mood)

  ExpressionThemeController->> AppTheme: obx(AppTheme)
  AppTheme ->>  ProfilePage: Theme.of(context).getColor()
 
```

### Analytics

``` mermaid
sequenceDiagram

  AnalyticsPage->>AnalyticsController: getStatistic(int emotion)
  AnalyticsController->>FireBaseController: getData(int emotion)
  FireBaseController -->AnalyticsController:return data;
  AnalyticsController --> AnalyticsPage:return Statistic()
 
 
```

## Estructura de datos en FireBase

### Estructura usuario

En el caso de usuario solo necsitamos guardar el email, el mood,el url del perfil y un pseudonimo

![users](assets\users.png)

### UserThemes

En user themes se guarda cada emocion de forma separada.

En cada emocion se guardan los siguientes datos:

![userThemes](assets\userThemes.png)

### Estructura mensaje

![messages](assets\messages.png)
