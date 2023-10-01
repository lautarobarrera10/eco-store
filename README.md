# Eco Store
Sitio web para prácticar y aplicar las habilidades aprendida del curso de Fundamentos de SASS


## Notas del curso 

### ¿Qué es un preprocesador?
Un preprocesador es una herramienta que nos permite escribir pseudocódigo recibiendo como parámetro de entrada los estilos que posteriormente serán convertidos a CSS nativo. Podemos decir que funcionan de manera similar a los traductores pues al indicarle una sintaxis devuelve los valores en una sintaxis nueva.
**Un preprocesador es un lenguaje que permite trabajar con estilos CSS haciendo uso de una sintaxis propia.**


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

### At rules CSS
Es una declaración que cumple con diferentes funciones, se inicializa con el símbolo @ y cuenta con sintaxis propia
Las at-rules dentro de SASS ayudan a mantener la compatibilidad con próximas versiones de CSS

- @use
- @import
- @function
- @forward
- @extend
- @at-root
- @error, @warn, @debug (de compilación)
- @include
- @for, @if, @each, @while

  #### ¿Para qué sirven las at-rules?
  Para modularizar nuestros estilos.
  **x** Son reglas de Sass que cumplen con diferentes funciones y cuenta con su sintaxis propia.

  ### Herencia
  #### ¿Qué es la herencia?
  La herencia es un mecanismo mediante el cual un selector puede recibir estilos CSS que vienen de variables utilizadas previamente.

  **x** Para hacer uso de la herencia en Sass es necesario utilizar la regla @extend.

