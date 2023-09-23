# Eco Store
Sitio web para prácticar y aplicar las habilidades aprendida del curso de Fundamentos de SASS


## Notas del curso 

### Estructura de una hoja de estilos de SASS
Algunos statement contienen bloques y se definen entre un par de llave **{}** y son separados mediante punto y coma **;**

#### Top-level statement
Declaraciones que solo se pueden utilizar en la parte superior de la hoja de estilos.

- Imports
- Definición de un Mixin
- Definición de una función
- Módulos

#### Universal statement
Los podemos utilizar en cualquier parte de la hoja de estilos

- Variables, estructuras de control y las reglas @error, @warn y @debug
- Declaraciones CSS: Reglas de estilo, at-rules y mixins


### Variables
- Para declararlas usamos el signo $
- Tienen un valor único correspondiente a un elemento
- Son imperativas

#### Variables locales
- Están declaradas dentro de un bloque **{}**
- Cualquier selector anidado puede acceder a las variables locales declaradas dentro del selector

#### Variables globales
Por default, todas las variables declaradas fuera de un selector son globales.

#### Shadowing (concepto)
Las variables locales y globales pueden tener los mismo nombres, ya que se encuentran en diferente nivel del scope
Esto puede ayudar a que no se llegue a modificar por error el valor de las variables globales

### flags

#### !defaul flag
Se encarga de asignar un valor a la variable si y solo si esa variable no está definicina o su valor es null

#### !global flag
En caso de querer modificar el valor global de una variable dentro del scope de una variable local, se hace uso de la flag !global
