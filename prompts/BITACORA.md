# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts. Herramienta de IA usada: Claude

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 7 | 34|
| The students program in Java. | 6 | 29 |
| Desafortunadamente | 4 | 18 |

-Al escribir en un primer chat estos dos mensajes seguidos: 
"Estoy desarrollando una aplicacion llamada TiendaTec en Java Swing para gestionar los productos de una tienda. Solo responde: Entendido."
"¿Como se llama mi aplicacion y que tecnologia usa?"
 me respondio entendido y los nombres de la tienda respectivamente, Pero luego al abrir un nuevo chat le pregunte como se llama el nombre de la aplicacion, no supo que responder.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100%  | LibroYa |
| 0.5 | 65.3% | PrestaLibro  |
| 1 | 44.5% | LectorGo |
| 1.8 | 32.2% | PaginaLibre |

Al subir la temperatura los porcentajes se reparten y empiezan a salir nombres poco probables, como LectoGo o NubeDeTinta.
El simulador nunca inventa un nombre nuevo porque solo elige entre las opciones que ya tiene: la temperatura cambia qué tan arriesgado es al elegir, no lo que sabe.

## Ejercicio 4: Prompt vago vs estructurado 

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | si | si |
| Tiene exactamente 3 funcionalidades | no | no |
| Esta en 3 parrafos | no | si |
| Lo usaria en un informe real | si | si |
## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt | 
|----------|-------------|
| | Crea un programa en Java. |
| Rol | Actua como desarrollador Java. Crea un programa en Java. |
| Instruccion | Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. | 
| Ejemplo | Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda usando una clase Producto con los atributos codigo, nombre, precio y stock. | 
| Formato | Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda usando una clase Producto con los atributos codigo, nombre, precio y stock, Explica primero la estructura de la clase y luego presenta el codigo Java | 

#


-	**Primer prompt:** Me devolvio un programa simple de calculadora

-	**Segundo:** pregunto entre 3 opciones de programa para hacer, y creo un juego basico de ahorcado.

-	**Tercer prompt:** Ahora fue directo a el pedido que le hice de que sea un programa para gestionar productos de una tienda, y lo hizo a su criterio.

-	**Cuarto prompt:** Ahora hizo lo mismo que en el tercer prompt, solo que ahora uso la clase y atributos especificos que le pedi.

-	**Quinto prompt:** hizo lo mismo que en el prompt 4, pero esta vez explico detalladamente la estructura de la clase antes de presentar el codigo



- [Bitacora de prompts](prompts/BITACORA.md)