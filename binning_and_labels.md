To specify your own bin edges and names:  
```
bin_labels = ['0-500', '500-1000', '1000-5000', '5000-15000', '15000+']
bins = [-1, 500, 1000, 5000, 15000, 5000000000]


df['bucket'] = pd.cut(df['column_to_sort'], bins=bins, labels=bin_labels)
```
