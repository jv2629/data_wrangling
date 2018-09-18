Data\_Wrangling
================
Jaclyn Verity
9/18/18

Import FAS csv files
--------------------

Import my first csv

``` r
litters_data = read_csv(file = "./data/FAS_litters.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   Group = col_character(),
    ##   `Litter Number` = col_character(),
    ##   `GD0 weight` = col_double(),
    ##   `GD18 weight` = col_double(),
    ##   `GD of Birth` = col_integer(),
    ##   `Pups born alive` = col_integer(),
    ##   `Pups dead @ birth` = col_integer(),
    ##   `Pups survive` = col_integer()
    ## )

``` r
litters_data = janitor::clean_names(litters_data)
names(litters_data)
```

    ## [1] "group"           "litter_number"   "gd0_weight"      "gd18_weight"    
    ## [5] "gd_of_birth"     "pups_born_alive" "pups_dead_birth" "pups_survive"

Import FAS pups csv files
-------------------------

Import Learning Assessment

``` r
pups_data = read_csv(file = "./data/FAS_pups.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   `Litter Number` = col_character(),
    ##   Sex = col_integer(),
    ##   `PD ears` = col_integer(),
    ##   `PD eyes` = col_integer(),
    ##   `PD pivot` = col_integer(),
    ##   `PD walk` = col_integer()
    ## )
