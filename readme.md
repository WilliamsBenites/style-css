## CSS
1. Una hoja de estilos en cascada
## VINCULACION HTML - CSS
1. usando Hoja de estilos externos usando etiqueta "link"
```html
    <link rel="stylesheet" href="./styles.css"/>
    ```
2. Usando etiqueta style
```html
<style>
    h1{
        color: red;
    }
</style>
```
3. De manera inline en elemento con el atributo "style"
```html
    <h1 style="color: red">css</h1>
```

## DESCRIPCION

    h1{
    color: peru;
    }
h=Selector
color=Propiedad
peru=valor

# CSS
 
- Es un lenguaje para dar estilos a la web (1996)
 
## SINTAXIS
 
- Como se puede establecer codigo CSS
 
```css
h1 {
  color: red;
}
```
 
- h1 : Selector
- color : Propiedad
- red : Valor
 
## CONCEPTOS IMPORTANTES CSS
 
- 4 Conceptos importantes de CSS
 
### SELECTORES
 
- Indica a que elemento o elementos, se aplicara estilos
 
```css
/* SELECTOR DE ETIQUETA */
h1 {
  color: red;
}
 
/* SELECTOR DE DESCENDENCIA */
nav ul li a {
  color: red;
}
```
 
### HERENCIA
 
- Elementos ancestros heredan algunas propiedades a sus descendientes.
 
```html
<p>Hola mundo <a href="#">Esto es un enlace</a></p>
```
 
```css
p {
  color: peru;
}
 
a {
  color: inherit;
}
```
 
### CASCADA
 
- Significa que los estilos que llegan en ultimo lugar , sobreescriben a los de antes.
- La especificidad vence a la cascada
 
```css
h1 {
  color: red;
}
 
h1 {
  color: blue;
}
```
 
### ESPECIFICIDAD
 
- Es un valor numerico que adquieren los selectores y se aplica cuando hay conflictos
 
```html
<!-- Selector de Etiqueta (1) -->
 
<!-- Selector de Clase (10) -->
 
<!-- Selector de ID (100) -->
 
<!-- INLINE (1000) -->
 
<!-- IMPORTANT (infinito) -->
```
 # ESTILOS DE TEXTO

h1 {
  color: red;
}
# ESTILOS DE TEXTO
 
## PROPIEDADES
 
- color
- font-size (em,rem,px)
- font-family (google fonts - fontface)
- font-weight (peso de tipografia)
- estilo entre navegadores (normalize.css)
- text-transform: uppercase | lowercase | capitalize
- text-align : left | center | right
- text-decoration : none | underline
 
# SELECTORES
 
- Selector de Etiqueta(1)
- Selector de Clase(10)
- Selector de ID(100)
- Selector Universal (uso box model)

## SELECTORES SIMPLES

1. Selector de Etiquetas
- Se aplica al elemento html especifico

2. Selector de Clase

- Es un atributo HTML que se indica con "class"
- Es lo mas utilizado en CSS para aplicar estilos

```html
<h1 class="mesnsaje">selector de clase</h1>
```
```css
.message {
  color: blue;
}
```
## SELECTORES COMPUESTOS
# SELECTORES
 
- La manera de agarrar elemento o elementos del HTML para aplicar estilos
 
## SELECTORES SIMPLES
 
1. Selector de Etiqueta
 
- Se aplica a elementos HTML especificos
- Se le conoce como estilos base(general)
 
```css
h1 {
  color: red;
}
 
span {
  display: block;
}
```
 
2. Selector de Clase
 
- Es un atributo HTML que se indica con "class"
- Es lo mas utilizado en CSS para aplicar estilos (recomendado)
- Para el nombramiento de clases se utiliza nomenclatura( arquitectura )
 
```html
<h1 class="message">Selector de Clase</h1>
```
 
```css
.message {
  color: blue;
}
```
 
3. Selector de ID
 
- Es un atributo HTML que se indica con "id"
- No se recomienda utilizarlo para CSS
- No puede existir dos elementos html con el mismo "id"
 
```html
<main id="mainContent">Contenido principal</main>
```
 
```css
#mainContent {
  display: block;
}
```
 
4. Selector Universal
 
- No se recomienda utilizar mucho
- Tiene un caso especifico
 
```css
* {
  color: red;
}
```
 
## SELECTORES COMPUESTOS
 
1. Selector de Descendencia (Descendente)
 
- Se aplica a un elemento que esta incluido en otro
- No necesita ser hijo directo, puede estar niveles mas abajo
 
```html
<div class="padre">
  <p>Hijo 1</p>
  <p>Hijo 2</p>
  <p>Hijo 3</p>
</div>
```
 
2. Selector Hijo Directo
 
- Selecciona al elemento o elementos que estan dentro y seguido de otro elemento
 
```html
<div class="padre">
  <p>Hijo 1</p>
  <p>Hijo 2</p>
  <p>Hijo 3</p>
</div>
```
 
```css
.padre > .hijo {
  color: red;
}
```
 
3. Selector Anidado
 
- Juntar selectores mediante comas
- Se aplica a todos los selectores
 
# BOX MODEL
 
 
- Algoritmo que usa el navegador para dibujar elementos
- Estos elementos tienen propiedades
- Todos los elementos en la web son rectangulares
- Propiedades importantes ( width - height )( ancho - alto )
- Elementos bloque ( width - height )
- Elementos inline ( width relativo - no tiene height)
- Propiedad display
- El box model se aplica solo a elementos de bloque
 
```html
<div>Soy un elemento</div>
```
 
## PARTES
 
1. Content Box (AZUL)
2. Padding Box (VERDE)
3. Border Box (AMARILLO)
 
4. Margin Box (NARANJA)

# POSICIONAMIENTO
 
- Con posicionamiento vamos a poder poner un elemento en cualquier lado que deseemos
- Position va romper el flujo basico del DOM
- Para que un elemento este posicionado (initial | relative | absolute | fixed | sticky)
- Cuando un elemento esta posicionado , aprende nuevas propiedades
<!--
  top
  right
  bottom
  left
  z-index
-->
 
## RELATIVE
 
- Un element posicionado de manera relative, mantiene sus dimensiones
- La relacion de relative es para dar contexto a un posicionamiento absolute
 
## ABSOLUTE
 
- Un element posicionado de manera absolute,no mantiene sus dimensiones (salvo que las tenga definidas)
- Su contexto es su ancestro posicionado mas cercano
 
## FIXED
 
- Pierde su espacio en el flujo
 
 