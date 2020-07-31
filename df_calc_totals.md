```
# create sample dataframe 
df = pd.DataFrame({
'cat_bucket': ['pao', 'pao', 'scout', 'scout', 'atticus', 'atticus'],
'is_won': [False, True, False, True, False, True],
'count': [325, 356, 714, 521, 315, 89]
})

# create total by bucket
df['totals'] = df.groupby('cat_bucket')['count'].transform(sum)
df['pct'] = df['count'] / df['totals']

# filter to see only won
df.query('is_won==True')
```
