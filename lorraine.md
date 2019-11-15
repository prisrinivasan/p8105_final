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

``` r
fix_problems = 
  problems(asthma_data) %>%
  separate(actual, c("annual", "average", "year"), sep = " ")
```

``` r
asthma_data_tidy = 
  asthma_data %>%
  rename(year = year_description) %>%
  mutate(data_value = as.numeric(data_value))
```
