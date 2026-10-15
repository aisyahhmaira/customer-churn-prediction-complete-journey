# How to Access The Complete Journey Dataset

This guide explains how to access the dataset used in the **Customer Churn Prediction using The Complete Journey Dataset** business analytics project.

**The Complete Journey** contains approximately one year of grocery shopping activity from **2,469 households**, including transactions, product information, demographics (where available), marketing campaigns, and coupon activity.

**Official references:**
- [The Complete Journey User Guide](https://bradleyboehmke.github.io/completejourney/articles/completejourney.html)
- [completejourney R package — GitHub repository](https://github.com/bradleyboehmke/completejourney)

## Method 1 — Install the R Package (Recommended)

### Step 1: Open R or RStudio

You will need an R environment to run the following commands.

### Step 2: Install and load the package

Run this in the R console:

```r
install.packages("completejourney")
library(completejourney)
```

You only need to install the package once on your computer; load it with `library(completejourney)` each time you begin a new R session.

### Step 3: See the available datasets

```r
data(package = "completejourney")
```

The package contains eight built-in datasets:

| Dataset | Description |
| --- | --- |
| `campaigns` | Marketing campaigns received by households |
| `campaign_descriptions` | Campaign types and active periods |
| `coupons` | Coupons associated with campaigns and products |
| `coupon_redemptions` | Coupons redeemed by households |
| `demographics` | Household characteristics, where available |
| `products` | Product information and categories |
| `promotions_sample` | Sample of promotional placements |
| `transactions_sample` | Sample of household transactions |

### Step 4: Preview a dataset

For example:

```r
head(transactions_sample)
head(products)
head(demographics)
```

The package includes **samples**, not the complete transaction and promotion tables. See Method 2 if you need those larger datasets.

## Method 2 — Download the Full Transaction and Promotion Data

According to the official user guide, the full transaction and promotion tables can be retrieved through functions provided by `completejourney`:

```r
library(completejourney)

# Full transaction data
transactions <- get_transactions()

# Full promotion data (large dataset)
promotions <- get_promotions()

# Check the number of rows and columns
dim(transactions)
dim(promotions)
```

The official documentation reports approximately:

| Full dataset | Rows | Columns |
| --- | ---: | ---: |
| `transactions` | 1,469,307 | 11 |
| `promotions` | 20,940,529 | 5 |

**Notes:**
- These functions retrieve the full data from the source GitHub repository and require an internet connection.
- The full `promotions` table is particularly large; allow sufficient memory and storage.
- If a download fails, check your connection and try again. An unsuccessful call may return `NULL`.

## Method 3 — Export the Dataset as CSV (For Excel, Python, etc.)

CSV export is an **optional step**, added here for people who want to use the dataset outside R. It is not a separate download method described by the official user guide.

### Option A: Export the sample transaction data

```r
library(completejourney)

dir.create("dataset", showWarnings = FALSE)

write.csv(
  transactions_sample,
  "dataset/transactions_sample.csv",
  row.names = FALSE
)
```

This creates a `dataset/transactions_sample.csv` file in your current working directory.

### Option B: Export all eight built-in datasets

```r
library(completejourney)

dir.create("dataset", showWarnings = FALSE)

names <- c(
  "campaigns",
  "campaign_descriptions",
  "coupons",
  "coupon_redemptions",
  "demographics",
  "products",
  "promotions_sample",
  "transactions_sample"
)

for (name in names) {
  write.csv(
    get(name),
    file.path("dataset", paste0(name, ".csv")),
    row.names = FALSE
  )
}
```

### Option C: Export full transactions (only if needed)

```r
library(completejourney)

dir.create("dataset", showWarnings = FALSE)
transactions <- get_transactions()

if (!is.null(transactions)) {
  write.csv(transactions, "dataset/transactions.csv", row.names = FALSE)
}
```

You can also export the full promotions data by calling `get_promotions()` and using `write.csv()`, but this may create a very large CSV file.

### Open a CSV in Python

After exporting, you can read the file with pandas:

```python
import pandas as pd

transactions = pd.read_csv("dataset/transactions_sample.csv")
print(transactions.head())
```

Or open smaller CSV files with Excel. Very large tables may exceed Excel's worksheet row limit, so use an appropriate data analysis tool for the full datasets.

## Method 4 — View the Source Files on GitHub

You can also inspect the available dataset files and the package source directly:

[Browse the official completejourney data folder](https://github.com/bradleyboehmke/completejourney/tree/master/data)

These are **R data files**, not necessarily ready-to-open CSV files. For a simple and reproducible workflow, Method 1 (R package) and Method 3 (CSV export) are easier to follow.

## Dataset Attribution

- **Dataset:** The Complete Journey
- **User guide:** https://bradleyboehmke.github.io/completejourney/articles/completejourney.html
