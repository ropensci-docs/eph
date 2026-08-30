# Descarga de Bases de EPH total urbano

Funcion que descarga bases de la Encuesta Permanente de Hogares total
urbano del INDEC a partir de 2016

## Uso

``` r
get_total_urbano(
  year = 2016,
  type = "individual",
  vars = "all",
  destfile = NULL
)
```

## Argumentos

- year:

  un integer o vector de integers a partir de 2016

- type:

  tipo de base a descargar: 'individual' ; 'hogar'

- vars:

  opcional: un vector de characters. variables a seleccionar. Default =
  'all' trae todas las variables

- destfile:

  opcional: un string con la direccion de un archivo .RDS. Si se ingresa
  un path a un archivo que no existe, se descarga el archivo y se graba
  en esa direccion. Si existe un archivo en ese path, se lee el archivo.

## Valor

Devuelve la o las bases de la EPH total urbano solicitadas

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r
if (FALSE) { # \dontrun{
base_individual <- get_total_urbano(
  year = 2016,
  type = "hogar",
  vars = c("PONDERA", "IV1", "IV2")
)
} # }
```
