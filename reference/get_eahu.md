# Descarga de Bases de la Encuesta anual de hogares urbanos

Funcion que descarga bases de la Encuesta anual de hogares urbanos del
INDEC entre 2010 y 2014

## Uso

``` r
get_eahu(year = 2010, type = "individual", vars = "all", destfile = NULL)
```

## Argumentos

- year:

  un integer o vector de integers entre 2010 y 2014

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

Devuelve la o las bases de la EAHU solicitadas

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r
if (FALSE) { # \dontrun{
base_individual <- get_eahu(
  year = 2010,
  type = "individual",
  vars = c("SUBDOMINIO", "PONDERA", "ESTADO", "CAT_OCUP")
)
} # }
```
