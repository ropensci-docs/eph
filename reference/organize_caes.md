# Clasificador de Actividades

Funcion para clasificar las actividades economicas segun el Clasificador
de actividades economicas para encuestas sociodemograficas. CAES
Mercosur 1.0 y CAES Mercosur. Basado en
https://www.indec.gob.ar/ftp/cuadros/menusuperior/clasificadores/notas_explicativas_caes_v2018.pdf

## Uso

``` r
organize_caes(base)
```

## Argumentos

- base:

  Base individual de uno o mas periodos

## Valor

Devuelve la base con 8 columnas nuevas (ver \`caes\`)

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

No olvides contemplar los cambios en la codificacion y categorias de las
distintas versiones del clasificador CAES para la elaboracion de series
de largo plazo.

## Ejemplos

``` r
bases <- dplyr::bind_rows(toybase_individual_2016_03, toybase_individual_2016_04)
bases_clasificadas <- organize_caes(base = bases)
#> Warning: Convirtiendo PP04B_COD a character
```
