# Funcion para etiquetar las bases de la Encuesta Permanente de Hogares.

Funcion para etiquetar las bases de la Encuesta Permanente de Hogares.

## Uso

``` r
organize_labels(df, type = "individual")
```

## Argumentos

- df:

  type de microdatos de la EPH

- type:

  (string) aclaracion sobre si la base a etiquetar es de tipo
  'individual' u 'hogar'

## Valor

Devuelve la base con sus variables etiquetadas de acuerdo con el disenio
de registro de la EPH (no renombra los valores o nombres de las
columnas, agrega etiquetas con esta información)

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r
df <- organize_labels(toybase_individual_2016_04, type = "individual")
```
