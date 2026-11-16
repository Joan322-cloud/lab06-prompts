# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.
Herramienta de IA usada: Claude (claude.ai).

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

-Al escribir en un primer chat estos dos mensajes seguidos: 
"Estoy desarrollando una aplicacion llamada TiendaTec en Java Swing para gestionar los productos de una tienda. Solo responde: Entendido."
"¿Como se llama mi aplicacion y que tecnologia usa?"
 me respondio "Entendido" y luego que la aplicacion se llama TiendaTec y usa Java Swing. Pero al abrir un nuevo chat y hacer la misma pregunta, no supo que responder: leyo la memoria de mi cuenta, menciono otro proyecto mio y me pidio que le dijera de que aplicacion hablaba.

En el mismo chat el dato estaba dentro de su ventana de contexto. En el chat nuevo la ventana empezo vacia: la IA no olvido TiendaTec, simplemente nunca lo vio.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3% | PrestaLibro  |
| 1 | 44.5% | LibroYa, PrestaLibro, PrestaLibro, BiblioTec, BiblioTec |
| 1.8 | 32.2% | BiblioTec, LibroYa, LibroYa, LectoGo, PaginaLibre |
| 1.8 (otra vez) | 32.2% | LectoGo, LibroYa, BiblioTec, BiblioTec, BiblioTec |

Al subir la temperatura los porcentajes se reparten y empiezan a salir nombres poco probables, como LectoGo o NubeDeTinta.
El simulador nunca inventa un nombre nuevo porque solo elige entre las opciones que ya tiene: la temperatura cambia qué tan arriesgado es al elegir, no lo que sabe.

## Ejercicio 4: Prompt vago vs estructurado 

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | si | si |
| Menciona a los usuarios principales | si | si |
| Tiene exactamente 3 funcionalidades | no | si |
| Esta en 3 parrafos | no | si |
| Lo usaria en un informe real | si | si |

## Ejercicio 5: Anatomia de un prompt

Prompt final (nivel 5 + ejemplo):

```text
Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).
```

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java ... usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto | para gestionar los productos de una tienda |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. |

## Que cambio en cada nivel:


-	**Primer prompt:** Me devolvio un programa simple de calculadora

-	**Segundo:** pregunto entre 3 opciones de programa para hacer, y creo un juego basico de ahorcado.

-	**Tercer prompt:** Ahora fue directo a el pedido que le hice de que sea un programa para gestionar productos de una tienda, y lo hizo a su criterio.

-	**Cuarto prompt:** Ahora hizo lo mismo que en el tercer prompt, solo que ahora uso la clase y atributos especificos que le pedi.

-	**Quinto prompt:** hizo lo mismo que en el prompt 4, pero esta vez explico detalladamente la estructura de la clase antes de presentar el codigo
