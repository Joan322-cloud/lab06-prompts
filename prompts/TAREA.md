# Tarea: Mi prompt profesional

Hare un prompt donde como prueba para poner en practica los distintos tipos de prompt vistos en la bitacora del laboratorio, hare que cree un juego estilo five nights at freddys, desde un prompt basico hasta uno complejo con cosas especificas que quiero y no quiero.

Herramienta de IA usada: Claude. Cada version la envie en un chat nuevo.

## Funcionalidad elegida

**Que cree un juego estilo five nights at freddys**

## Version 1: prompt basico

```text
crea un juego estilo five nights at freddys
```

- Creo un juego estilo five night at freddys usando una idea propia llamado noches en la pizzeria pelusa.

- Uso como motor html simple, sonidos generados que suenan como 8 bits, la unica indicacion que tomo fue que fuera estilo five night at freddys.

- En general esto genero un juego simple, hecho en html web, y con varias cosas faltantes.

## Version 2

```text
Actua como un desarrollador de videojuegos de terror, crea un juego estilo five night at freddys basado y ambientado en el palacio de gobierno del peru y sus politicos como animatronicos.
```

- En este prompt use que tenga un rol e instruccion especifica de como era mi idea del juego.

- Esta vez especifique en que quiero que este ambientado el juego, y que actue como un desarrollador de juegos de terror.

- Aun creo el juego en html.

- Aun esta el juego en 2d.

- Uso aun sonidos hechos propios en 8 bits que suenan mal, y uso nombres inventados.

## Version 3: prompt final

```text
Actua como un desarrollador de videojuegos de terror, crea un juego estilo five night at freddys basado y ambientado en el palacio de gobierno del peru y sus politicos como animatronicos, debe ser en 3d, como aplicacion jugable .exe, si es necesario que instales una interfaz de desarrollo puedes hacerlo y no puedes usar sonidos generados por ti, si no buscar de algun banco de sonidos o modificar sonidos para que suene mas organico y terrorrifico. Los animatronicos serian:
-queico: presidenta china, solo roba
-Pehdroh kastiyo: Ex presidente, solo quiere saber si el pollo esta vivo o muerto
-Biscarry: ex presidente que busca disolver el congreso
-Jalan Garzia: ex presidente que solo dice que lo demuestren pues.
```

- En este prompt use el ejemplo y el formato que queria, especificandole que sea el juego en 3d, que use una interfaz de desarrollo y los personajes exactos que queria.

- Le indique como restriccion que no use sonidos generados por el mismo, debido a que suenan mal.

- Ahora creo un ejecutable en lugar de un html.

- Ahora uso los animatronicos exactos que le indique, y su funcion exacta.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como un desarrollador de videojuegos de terror |
| Instruccion | crea un juego estilo five night at freddys |
| Contexto | basado y ambientado en el palacio de gobierno del peru y sus politicos como animatronicos |
| Ejemplos | La lista de los animatronicos con lo que hace cada uno (queico, Pehdroh kastiyo, Biscarry y Jalan Garzia) |
| Formato | debe ser en 3d, como aplicacion jugable .exe |
| Restriccion | no puedes usar sonidos generados por ti, si no buscar de algun banco de sonidos o modificar sonidos |

## Evaluacion del resultado

| Criterio | Version 1 | Version 2 | Version 3 |
|---|---|---|---|
| Esta ambientado en el palacio de gobierno | No | Si | Si |
| Usa los animatronicos que yo pedi | No | No | Si |
| El juego es en 3d | No | No | Si |
| Es un ejecutable .exe y no un html | No | No | Si |
| No usa sonidos generados por la IA | No | No | Si |

## Errores que evite

- **Ser demasiado general:** en la version 1 solo pedi "crea un juego estilo five nights at freddys" y la IA invento todo: la pizzeria, los personajes y los sonidos. Lo evite dandole un rol y diciendole donde queria que este ambientado el juego.

- **No indicar el formato:** en la version 2 no dije como queria el juego y por eso lo siguio haciendo en html y en 2d. Lo evite en la version 3 pidiendole que sea en 3d y como un ejecutable .exe.
