lorraine
================

``` r
asthma_data = read_csv("./final_data/asthma_data.csv") %>%
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
