From segmentation tutorial & RFM metrics calculation  

```
# Aggregate data by CustomerID into new dataframe datamart
datamart = df.groupby(['CustomerId').agg({
    'InvoiceDate': lambda x: (current_date - x.max()).days,
    'InvoiceNo': 'count',
    'TotalSum': 'sum'})

# Rename columns
datamart.rename(columns = {'InvoiceDate': 'Recency',
                           'InvoiceNo': 'Frequency',
                           'TotalSum': 'MonetaryValue'}, inplace=True)            
```
