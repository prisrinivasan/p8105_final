Kelly
================

``` r
all_available_data=
  read_csv(file="./final_data/all_available_data.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   unique_id = col_double(),
    ##   indicator_id = col_double(),
    ##   name = col_character(),
    ##   measure = col_character(),
    ##   geo_type_name = col_character(),
    ##   geo_join_id = col_double(),
    ##   geo_place_name = col_character(),
    ##   time_period = col_character(),
    ##   start_date = col_date(format = ""),
    ##   data_value = col_double(),
    ##   message = col_character(),
    ##   confidence_interval = col_logical()
    ## )

    ## Warning: 42367 parsing failures.
    ##  row                 col           expected       actual                                  file
    ## 5332 confidence_interval 1/0/T/F/TRUE/FALSE (38.1, 45.8) './final_data/all_available_data.csv'
    ## 5334 confidence_interval 1/0/T/F/TRUE/FALSE (29.7, 35.1) './final_data/all_available_data.csv'
    ## 5336 confidence_interval 1/0/T/F/TRUE/FALSE (21.5, 27.5) './final_data/all_available_data.csv'
    ## 5338 confidence_interval 1/0/T/F/TRUE/FALSE (30.9, 37.1) './final_data/all_available_data.csv'
    ## 5340 confidence_interval 1/0/T/F/TRUE/FALSE (28.2, 38.4) './final_data/all_available_data.csv'
    ## .... ................... .................. ............ .....................................
    ## See problems(...) for more details.

``` r
Asthma_data=
  read_csv(file="./final_data/asthma_data.csv")
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
    ##  row              col expected              actual                           file
    ## 5167 year_description a double Annual Average 2009 './final_data/asthma_data.csv'
    ## 5168 year_description a double Annual Average 2009 './final_data/asthma_data.csv'
    ## 5169 year_description a double Annual Average 2009 './final_data/asthma_data.csv'
    ## 5170 year_description a double Annual Average 2009 './final_data/asthma_data.csv'
    ## 5171 year_description a double Annual Average 2009 './final_data/asthma_data.csv'
    ## .... ................ ........ ................... ..............................
    ## See problems(...) for more details.

``` r
mold_data=
  read_csv(file="./final_data/mold_home.csv")
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

### Kelly vision: X : borough name , Y: Hospitalization Asthma Rate, by different boroughs

``` r
overview_plot=
all_available_data %>% 
  filter(Name= "Public School Children ())
```

    ## Error: <text>:3:16: unexpected INCOMPLETE_STRING
    ## 2: all_available_data %>% 
    ## 3:   filter(Name= "Public School Children ())
    ##                   ^
