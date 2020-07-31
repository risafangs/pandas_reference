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
optional, add vmin and vmax to control axis values 


**Distplots**

```
# Plot distribution of var1
plt.subplot(3, 1, 1)
sns.distplot(data['var1'])

# Plot distribution of var2
plt.subplot(3, 1, 2)
sns.distplot(data['var2'])

# Plot distribution of var3
plt.subplot(3, 1, 3)
sns.distplot(data['var3'])

# Show the plot
plt.show()
```
