final\_project
================

``` r
pests_home = read_csv(file = "./final_data/mold_home.csv") %>%
  janitor::clean_names()
```

    ## Parsed with column specification:
    ## cols(
    ##   indicator_data_id = col_double(),
    ##   indicator_id = col_double(),
    ##   name = col_character(),
    ##   Measure = col_character(),
    ##   geo_type_name = col_character(),
    ##   geo_entity_id = col_double(),
    ##   year_description = col_double(),
    ##   data_value = col_character(),
    ##   message = col_character()
    ## )

    ## Warning: 378 parsing failures.
    ##  row              col               expected actual                         file
    ## 1975 year_description no trailing characters  -2013 './final_data/mold_home.csv'
    ## 1976 year_description no trailing characters  -2013 './final_data/mold_home.csv'
    ## 1977 year_description no trailing characters  -2013 './final_data/mold_home.csv'
    ## 1978 year_description no trailing characters  -2013 './final_data/mold_home.csv'
    ## 1979 year_description no trailing characters  -2013 './final_data/mold_home.csv'
    ## .... ................ ...................... ...... ............................
    ## See problems(...) for more details.

``` r
air_conc = read_csv(file = "./final_data/air_conc.csv") %>%
  janitor::clean_names()
```

    ## Parsed with column specification:
    ## cols(
    ##   indicator_data_id = col_double(),
    ##   indicator_id = col_double(),
    ##   name = col_character(),
    ##   Measure = col_character(),
    ##   geo_type_name = col_character(),
    ##   geo_entity_id = col_double(),
    ##   year_description = col_character(),
    ##   data_value = col_double(),
    ##   message = col_character()
    ## )

``` r
mice_home = read_csv(file = "./final_data/mice_home.csv") %>%
  janitor::clean_names()
```

    ## Parsed with column specification:
    ## cols(
    ##   indicator_data_id = col_double(),
    ##   indicator_id = col_double(),
    ##   name = col_character(),
    ##   Measure = col_character(),
    ##   geo_type_name = col_character(),
    ##   geo_entity_id = col_double(),
    ##   year_description = col_double(),
    ##   data_value = col_character(),
    ##   message = col_character()
    ## )

    ## Warning: 3486 parsing failures.
    ##  row              col expected              actual                         file
    ## 5167 year_description a double Annual Average 2009 './final_data/mice_home.csv'
    ## 5168 year_description a double Annual Average 2009 './final_data/mice_home.csv'
    ## 5169 year_description a double Annual Average 2009 './final_data/mice_home.csv'
    ## 5170 year_description a double Annual Average 2009 './final_data/mice_home.csv'
    ## 5171 year_description a double Annual Average 2009 './final_data/mice_home.csv'
    ## .... ................ ........ ................... ............................
    ## See problems(...) for more details.
