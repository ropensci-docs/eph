# Registro de cambios

## eph 1.0.2

Versión CRAN: 2024-06-23

- better adjusted to CRAN’s policy ‘Packages which use Internet
  resources should fail gracefully with an informative message if the
  resource is not available or has changed (and not give a check warning
  nor error).’

## eph 1.0.1

Versión CRAN: 2024-06-19

- fixed organize_labels bug

## eph 1.0.0

Versión CRAN: 2023-09-15

- added new functions: get_total_urbano() and get_eahu() (as well as
  their auxiliar internal functions)
- improved documentation and site
- added contributing and codemeta.json files
- improved error messages using cli package
- reduced dependencies relying on base r and improved deprecated code
- re-structured functions using the early return philosophy
- styled code according to the tidyverse style guide
- modified get_microdata function to avoid parameter conflicts between
  trimester and wave
- fixed map_agglomerates bug
- added additional tests

## eph 0.6.1

Versión CRAN: 2023-07-17

- fixed bug in get_microdata() originated in a change in INDEC’s URL
  (old datasets are now directly downloaded from a stable github repo)

## eph 0.6.0

Versión CRAN: 2023-04-14

- removed ‘readr’ and ‘tidyverse’ from Imports. readr was reclassified
  as a Suggest (because it was only used in a vignette) and tidyverse
  was replaced by the tidyverse packages actually required.
- improved error messages in
  [`calculate_tabulates()`](https://docs.ropensci.org/eph/reference/calculate_tabulates.md)
  function.

## eph 0.5.1

Versión CRAN: 2022-08-29

- fixed warnings when downloading poverty lines

## eph 0.5.0

Versión CRAN: 2022-08-11

- improve
  [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md)
  internals
- remove `questionr` dependency
- add group_vars and window argument to calculate_poverty
- add function
  [`calculate_errors()`](https://docs.ropensci.org/eph/reference/calculate_errors.md)
- add affix_sign argument to
  [`calculate_tabulates()`](https://docs.ropensci.org/eph/reference/calculate_tabulates.md)

## eph 0.4.0

Versión CRAN: 2020-06-25

- add option destfile to
  [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md)
- add vignettes on poverty calculations
- add option to
  [`get_poverty_lines()`](https://docs.ropensci.org/eph/reference/get_poverty_lines.md)
  to download regional baskets

## eph 0.3.1

Versión CRAN: 2020-05-24

- rename organize_ocupations –\>
  [`organize_cno()`](https://docs.ropensci.org/eph/reference/organize_cno.md)
  for consistency
- add function
  [`organize_caes()`](https://docs.ropensci.org/eph/reference/organize_caes.md)
- fixed compatibility with dplyr 1.0

## eph 0.3.0

Versión CRAN: 2020-03-08

- improve `get_microdata_internal()` internals
- fixed compatibility with tibble 3.0.0
- add dataset on centroids of aglomerates of the survey
- add function
  [`map_agglomerates()`](https://docs.ropensci.org/eph/reference/map_agglomerates.md)
  for mapping indicators

## eph 0.2.0

Versión CRAN: 2019-11-26

- enhace
  [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md).
  Now downloads multiple datasets and allows to pre-select variables
- add skip_if_offline and some skip_on_cran for time-consuming tests
- add stop if there is no internet connection for
  [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md)
- add vignettes
- simplify output in
  [`organize_panels()`](https://docs.ropensci.org/eph/reference/organize_panels.md)
- add function organize_ocupations

## eph 0.1.1

Versión CRAN: 2019-09-07

- Added a `NEWS.md` file to track changes to the package.
- Bug fix in
  [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md)
- Added Authors@ information (orcid)
- add bugreport to DESCRIPTION
