
# Data Visualization with Seaborn

## Introduction

 - Seaborn: A Python library for data visualization that works well with pandas and builds on matplotlib.
 - Benefits:
 
    -Introduces new chart types and layouts.

    -Simplifies the process of creating attractive and informative statistical graphics.

    -Designed to work seamlessly with pandas DataFrames.
    
    -Automatically handles aggregation and missing data.

## Installation:

   - Install Via pip

```bash
pip install seaborn

```

## Basic Usage:

  - Import Seaborn

```bash
import seaborn as sns

```

## Key Features

- High-Level Interface: Provides a high-level interface for drawing attractive and informative statistical graphics.

- Built-in Themes: Includes several built-in themes to style your plots.

```bash
sns.set_theme(style="darkgrid")

```

## Basic Formatting options

 - Matplotlib Compatibility: Use matplotlib arguments to format Seaborn charts.

    python

```bash
sns.lineplot(x="date", y="LodgingRevenue", data=hotels, estimator=sum, ci=None, ls='--', color='green')
```
      
```bash 
sns.despine()  # Removes top and right borders
```

## Bar Charts and Histogram

 - Bar Charts:

    python

```bash
sns.barplot(x='cut', y='carat', data=diamonds)
sns.barplot(x='carat', y='cut', data=diamonds)  # Horizontal bar chart
sns.barplot(x='cut', y='price', data=diamonds, hue='clarity', palette='husl')  # Grouped bar chart
```
 - Histograms

      python

```bash
sns.histplot(x='price', data=diamonds.query("clarity in ['I1','IF']"), hue='clarity', bins=10, kde=True, palette='husl')

```

## Box and Violin Plots

 - Box Plots:

    python

```bash
sns.boxplot(x='price', data=diamonds, color='orange')
sns.boxplot(x='cut', y='price', data=diamonds, color='orange')
```
 - Violin Plots

      python

```bash
sns.violinplot(x='cut', y='price', data=diamonds)
```

## Linear Relationship Charts

 - Scatter Plots:

    python

```bash
sns.scatterplot(x='x', y='price', data=diamonds, hue='carat', size='carat', palette='husl')
```
 - Regression Plots

      python

```bash
sns.regplot(x='x', y='y', data=data)
```

- LM Plots

    python
    
```bash
sns.lmplot(x='x', y='y', hue='hue', row='row', col='col', data=data)
```

- Joint Plots

    python
    
```bash
sns.jointplot(x='x', y='y', kind='kde', data=data)
```

- Pair Plots

    python
    
```bash
sns.pairplot(data, corner=True)
```

## Heatmaps

 - Heatmap:

    python

```bash
sns.heatmap(diamonds_pivot, annot=True, fmt='g', cmap='RdYlGn')
sns.heatmap(top5_countries_pivot.iloc[:,:10].corr(), annot=True, cmap='vlag')
```

## FacetGrid

 - FacetGrid:

    python

```bash
g = sns.FacetGrid(ca_housing, col='region_name', col_wrap=2)
g.map_dataframe(sns.barplot, x='price_bins', y='inventory')
```

## Matplotlib Integration

 - Integration: Seaborn plots can be customized using Matplotlib commands:

    python

```bash
plt.figure(figsize=(10, 6))
sns.lineplot(x='date', y='value', data=data)
plt.title('Sample Title')
plt.xlabel('Date')
plt.ylabel('Value')
```
 

   


## Documentation

Official Documentation: (https://seaborn.pydata.org/tutorial/introduction.html)

