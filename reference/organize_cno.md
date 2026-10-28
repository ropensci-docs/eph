# Clasificador de Ocupaciones

Funcion para clasificar las ocupaciones segun las 4 dimensiones del
Clasificador Nacional de Ocupaciones (CNO 2001)

## Uso

``` r
organize_cno(base)
```

## Argumentos

- base:

  Base individual de uno o mas periodos

## Valor

Devuelve la base con 4 columnas nuevas (que indican la informacion
correspondiente al Clasificador Nacional de Ocupaciones)

## Detalles

Importante: Verificar que el clasificador CNO 2001 sea compatible con la
base que estes utilizando.

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r


bases <- dplyr::bind_rows(toybase_individual_2016_03, toybase_individual_2016_04)
bases_clasificadas <- organize_cno(base = bases)
```
