# pandas_reference

Quick reference code snippets for dataframe manipulation and graphing using Pandas and seaborn.


**show more rows** (toggle the 500 value)
```
pd.set_option('display.max_rows', 500)
```
**suppress scientific notation**
```
pd.set_option('display.float_format', lambda x: '%.3f' % x)
```
**suppress scientific notation & round & ADD COMMAS!!!!**
```
pd.options.display.float_format = '{:,.0f}'.format
```
**show all dataframes in memory**
```
%whos DataFrame
```

## Matplotlib

**suppress scientific notation on axes**
```
plt.ticklabel_format(style='plain', axis='y')
```

### Cheatsheets
- https://gist.github.com/bsweger/e5817488d161f37dcbd2

