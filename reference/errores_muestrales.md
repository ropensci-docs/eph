# Tabla con los errores muestrales para estimaciones de poblacion

Base con los errores muestrales para estimaciones de poblacion en los
aglomerados urbanos para la EPH continua desde 2003 segundo trimestre
segun documentacion de INDEC:
https://www.indec.gob.ar/ftp/cuadros/menusuperior/eph/EPH_errores_muestreo_3t2014.pdf
https://www.indec.gob.ar/ftp/cuadros/menusuperior/eph/EPH_errores_muestreo.pdf

## Uso

``` r
errores_muestrales
```

## Formato

Un data frame con 1687 filas y 5 variables:

- `codigo`:

  character —String con codigo numerico de los 31 aglomerados, "Gran
  Buenos Aires" (solo para 2003.03 a 2014.02), o con "Total" para el
  conjunto de los 31 aglomerados—

- `aglomerado`:

  character —String con el nombre del aglomerado—

- `periodo`:

  character —String indicando el periodo de EPH que corresponde,
  "2014.03" para datos de EPH a partir del tercer trimestre 2014, o
  "2003.03_2014.02" para datos anteriores—

- `x`:

  double —Estimacion de poblacion para la cual se desea conocer el error
  muestral—

- `ds`:

  double —Desvio Estandar correspondiente a la estimacion de poblacion
  en el aglomerado—

- `cv`:

  double —Coeficiente de Variacion correspondiente a la estimacion de
  poblacion en el aglomerado—
