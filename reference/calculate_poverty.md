# Calculo de Pobreza e Indigencia

Funcion para calcular la pobreza e indigencia siguiendo la metodologia
de linea.

## Uso

``` r
calculate_poverty(
  base,
  basket,
  print_summary = TRUE,
  window = "quarter",
  group_vars = c()
)
```

## Argumentos

- base:

  Base individual de uno o mas periodos

- basket:

  canasta basica alimentaria y total, con la estructura de la canasta de
  ejemplo (ver \`canastas_reg_example\`)

- print_summary:

  default = TRUE. Opcion para imprimir las tasas de pobreza e indigencia
  (proporcion de individuos)

- window:

  default = "quarter". Opcion para cambiar el lapso del calculo que se
  imprime en consola. "quarter" (para estimacion trimestral) o
  "semester" (estimacion semestral)

- group_vars:

  Opcion para agregar variables agrupadoras para el calculo que se
  imprime en consola.

## Valor

Devuelve la base agregando informacion respecto a la situacion de cada
hogar en terminos de sus ingresos: indigente, pobre o no pobre (a estos
fines, se agregan 5 columnas nuevas).

## Detalles

disclaimer: El script no es un producto oficial de INDEC.

## Ejemplos

``` r

bases <- dplyr::bind_rows(
  toybase_individual_2016_03,
  toybase_individual_2016_04
)

base_pobreza <- calculate_poverty(
  base = bases,
  basket = canastas_reg_example,
  print_summary = TRUE,
  group_vars = c(CH04, NIVEL_ED),
  window = "semestral"
)
#> # A tibble: 14 × 6
#> # Groups:   ANO4, SEMESTRE, CH04 [2]
#>     ANO4 SEMESTRE  CH04 NIVEL_ED Tasa_pobreza Tasa_indigencia
#>    <int>    <dbl> <dbl>    <int>        <dbl>           <dbl>
#>  1  2016        2     1        1       0.0700         0.00430
#>  2  2016        2     1        2       0.0149         0.00509
#>  3  2016        2     1        3       0.0348         0.00682
#>  4  2016        2     1        4       0.0158         0.0111 
#>  5  2016        2     1        5       0.0556         0.0399 
#>  6  2016        2     1        6       0              0      
#>  7  2016        2     1        7       0.0448         0.00442
#>  8  2016        2     2        1       0.0276         0.00708
#>  9  2016        2     2        2       0.0397         0.0315 
#> 10  2016        2     2        3       0.0427         0.0184 
#> 11  2016        2     2        4       0.0278         0.0194 
#> 12  2016        2     2        5       0.0349         0.0184 
#> 13  2016        2     2        6       0              0      
#> 14  2016        2     2        7       0.0125         0.0109 
```
