# Tabulado con ponderacion

Funcion para crear tabulados uni o bivariados con ponderacion, totales
parciales y porcentajes.

## Uso

``` r
calculate_tabulates(
  base,
  x,
  y = NULL,
  weights = NULL,
  affix_sign = FALSE,
  digits = 1,
  add.totals = "none",
  add.percentage = "none"
)
```

## Argumentos

- base:

  Dataframe

- x:

  string con el nombre de la variable a tabular

- y:

  otro string (opcional) con el nombre de una segunda variable, para una
  tabla de doble entrada. Tiene que ser de igual largo que x

- weights:

  string con el nombre de la variable con los pesos de pesos, tiene que
  ser de igual largo que x

- affix_sign:

  si es TRUE agrega el signo % al final

- digits:

  numero de digitos significativos

- add.totals:

  toma los valores c('none','row','col','both'), para agregar totales
  por fila, columna o ambos

- add.percentage:

  toma los valores c('none','row','col'), para agregar porcentajes por
  fila y columna

## Valor

Devuelve un tabulado uni o bivariado con ponderacion, totales parciales
y porcentajes.

## Ejemplos

``` r


### Tabla simple ###

calculate_tabulates(
  base = toybase_individual_2016_04,
  x = "REGION", y = "CH04",
  weights = "PONDERA"
)
#> # A tibble: 6 × 3
#>   `REGION/CH04`    `1`    `2`
#>   <fct>          <int>  <int>
#> 1 1             245400 236187
#> 2 40             41706  49796
#> 3 41             22680  19816
#> 4 42             23028  30712
#> 5 43            103892 119361
#> 6 44             19250  17926

### Totales por fila ###

calculate_tabulates(
  base = toybase_individual_2016_04,
  x = "REGION", y = "CH04",
  weights = "PONDERA", add.totals = "row"
)
#> # A tibble: 7 × 3
#>   `REGION/CH04`    `1`    `2`
#>   <chr>          <dbl>  <dbl>
#> 1 1             245400 236187
#> 2 40             41706  49796
#> 3 41             22680  19816
#> 4 42             23028  30712
#> 5 43            103892 119361
#> 6 44             19250  17926
#> 7 Total         455956 473798

### Totales por columna ###

calculate_tabulates(
  base = toybase_individual_2016_04,
  x = "REGION", y = "CH04",
  weights = "PONDERA", add.totals = "col"
)
#> # A tibble: 6 × 4
#>   `REGION/CH04`    `1`    `2`  Total
#>   <fct>          <int>  <int>  <dbl>
#> 1 1             245400 236187 481587
#> 2 40             41706  49796  91502
#> 3 41             22680  19816  42496
#> 4 42             23028  30712  53740
#> 5 43            103892 119361 223253
#> 6 44             19250  17926  37176

### Porcentajes por fila ###

calculate_tabulates(
  base = toybase_individual_2016_04,
  x = "REGION", y = "CH04",
  weights = "PONDERA", add.percentage = "row"
)
#> # A tibble: 6 × 3
#>   `REGION/CH04`   `1`   `2`
#>   <chr>         <dbl> <dbl>
#> 1 1              51    49  
#> 2 40             45.6  54.4
#> 3 41             53.4  46.6
#> 4 42             42.9  57.1
#> 5 43             46.5  53.5
#> 6 44             51.8  48.2
```
