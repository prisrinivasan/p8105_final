lorraine
================

``` r
<<<<<<< HEAD
asthma_data = read_csv(file = "./final_data/asthma_data.csv") %>%
=======
asthma_data = read_csv("./final_data/asthma_data.csv") %>%
>>>>>>> b682072069c6ec899e62f5f61d0c58b20b031d7c
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

<<<<<<< HEAD
This code chunk fixes the parsing failures.

``` r
fix_problems = problems(asthma_data) %>%
  filter(str_detect(actual, "^Annual")) %>%
=======
``` r
fix_problems = 
  problems(asthma_data) %>%
>>>>>>> b682072069c6ec899e62f5f61d0c58b20b031d7c
  separate(actual, c("annual", "average", "year"), sep = " ")
```

``` r
asthma_data_tidy = 
  asthma_data %>%
  rename(year = year_description) %>%
<<<<<<< HEAD
  mutate(data_value = as.numeric(data_value)) %>%
  select(-indicator_data_id, -indicator_id)
=======
  mutate(data_value = as.numeric(data_value))
>>>>>>> b682072069c6ec899e62f5f61d0c58b20b031d7c
```
