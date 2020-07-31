Example from https://towardsdatascience.com/combo-charts-with-seaborn-and-python-2bc911a08950  

```
#Create combo chart
fig, ax1 = plt.subplots(figsize=(12,6))
color = 'tab:green'

#bar plot creation
ax1.set_title('Opportunity Count & Win Rate by Material', fontsize=16)
ax1.set_xlabel('Material Category', fontsize=16)
ax1.set_ylabel('Count of Opportunities', fontsize=16)
ax1 = sns.barplot(x='material_category', y='ct_opportunities', data=opp_win, ci=False, palette='husl')
ax1.tick_params(axis='y')

#specify we want to share the same x-axis
ax2 = ax1.twinx()
color = 'tab:blue'

#line plot creation
ax2.set_ylabel('Opportunity Win Rate %', fontsize=16)
sns.lineplot(x='material_category', y='pct', data=opp_win.query('is_won==True'), color=color)
ax2.tick_params(axis='y', color=color)

#show plot
plt.show()
```
