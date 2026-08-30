# Pool de Datos en Panel - Base Individudal EPH continua

Permite armar un pool de datos en panel de la EPH continua a partir de
especificar una serie consecutiva de bases, variables y el largo de la
ventana -window- de observacion

## Uso

``` r
organize_panels(bases, variables, window = "anual")
```

## Argumentos

- bases:

  Lista de bases de microdatos a utilizar para armar el pool de datos

- variables:

  Vector con nombres de las variables de interes

- window:

  Especificar distancia temporal entre las observaciones. anual o
  trimestral

## Valor

Devuelve el pool de datos de panel

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r

lista_bases <- list(toybase_individual_2016_03, toybase_individual_2016_04)
pool_trimestral <- organize_panels(
  bases = lista_bases,
  variables = c("P21", "ESTADO"),
  window = "trimestral"
)
```
