lorraine
================

``` r
<<<<<<< HEAD
asthma_data = read_csv(file = "./final_data/asthma_data.csv") %>%
=======
asthma_data = read_csv("./final_data/asthma_data.csv") %>%
<<<<<<< HEAD
  janitor::clean_names() 
=======
>>>>>>> b682072069c6ec899e62f5f61d0c58b20b031d7c
  janitor::clean_names()
>>>>>>> 2eb932c3b72864b47c4b58c63cececeb35743971
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
asthma_data2 = 
  asthma_data %>%
  mutate(year = year_description, 
         row = row_number())
```

``` r
fix_problems = 
  problems(asthma_data) %>%
<<<<<<< HEAD
  separate(actual, c("annual", "average", "year"), sep = " ") %>%
  select(row, year) %>%
  mutate(year = as.numeric(year))
```

``` r
asthma_merged =
  left_join(asthma_data2, fix_problems, by = "row")
=======
>>>>>>> b682072069c6ec899e62f5f61d0c58b20b031d7c
  separate(actual, c("annual", "average", "year"), sep = " ")
>>>>>>> 2eb932c3b72864b47c4b58c63cececeb35743971
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
