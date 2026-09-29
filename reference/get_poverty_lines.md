# Descarga de canasta basica alimentaria y canasta basica total

Funcion que descarga la CBA y CBT a partir de abril 2016

## Uso

``` r
get_poverty_lines(regional = FALSE)
```

## Argumentos

- regional:

  booleano, default = FALSE. Si es TRUE, descarga los datos de canastas
  regionales que se utilizan para el calculo de pobreza. Si es FALSE,
  descarga la serie de GBA provista por indec en
  https://www.indec.gob.ar/indec/web/Nivel4-Tema-4-43-149

## Valor

Devuelve una tabla con la CBA y CBT a partir de abril 2016

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r

canasta <- get_poverty_lines(regional = TRUE)
canasta
#> # A tibble: 234 × 5
#> # Groups:   region [6]
#>    region periodo   CBA   CBT codigo
#>    <chr>  <chr>   <dbl> <dbl>  <dbl>
#>  1 Cuyo   2015.4  1225. 2951.     42
#>  2 Cuyo   2016.1  1315. 3219.     42
#>  3 Cuyo   2016.2  1401. 3637.     42
#>  4 Cuyo   2016.3  1509. 3872.     42
#>  5 Cuyo   2016.4  1570. 4030.     42
#>  6 Cuyo   2017.1  1635. 4219.     42
#>  7 Cuyo   2017.2  1731. 4513.     42
#>  8 Cuyo   2017.3  1802. 4690.     42
#>  9 Cuyo   2017.4  1894. 4975.     42
#> 10 Cuyo   2018.1  2013. 5374.     42
#> # ℹ 224 more rows
```
