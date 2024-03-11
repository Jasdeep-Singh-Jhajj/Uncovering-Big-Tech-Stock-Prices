# Data


## `big_tech_stock_prices.csv`

| variable       | class     | description                                                                                                                                                                                                                       |
|---------|---------|-----------------------------------------------------|
| `stock_symbol` | character | stock_symbol                                                                                                                                                                                                                      |
| `date`         | double    | date                                                                                                                                                                                                                              |
| `open`         | double    | The price at market open.                                                                                                                                                                                                         |
| `high`         | double    | The highest price for that day.                                                                                                                                                                                                   |
| `low`          | double    | The lowest price for that day.                                                                                                                                                                                                    |
| `close`        | double    | The price at market close, adjusted for splits.                                                                                                                                                                                   |
| `adj_close`    | double    | The closing price after adjustments for all applicable splits and dividend distributions. Data is adjusted using appropriate split and dividend multipliers, adhering to Center for Research in Security Prices (CRSP) standards. |
| `volume`       | double    | The number of shares traded on that day.                                                                                                                                                                                          |

## `big_tech_companies.csv`

| variable     | class     | description               |
|--------------|-----------|---------------------------|
| stock_symbol | character | stock_symbol              |
| company      | character | Full name of the company. |



# Codebook for the Dataset
```{r}
if (!require(pacman))
  install.packages(pacman)


pacman::p_load(readr,
               here)
               
# Getting all the underlying data in the dataset

big_tech_stock_prices <- read_csv(here("data","big_tech_stock_prices.csv"))
big_tech_companies <- read_csv(here("data","big_tech_companies.csv"))


```

