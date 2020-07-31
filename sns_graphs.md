## Graphing examples for Seaborn

**Heatmap**

Should use a dataframe like a pivoted cohort view.

```
plt.figure(figsize=(10,10))

plt.title('Cool Heatmap')

sns.heatmap(df, 
  	    annot=True, # shows numbers
	    fmt= , # how to format values
	    cmap='YlGnBu', # palette
)

plt.show()
```

# optional, add vmin and vmax to control axis values 

```
