# 📊 My Seaborn Learning Journey  

Hi, I’m **Purvesh** 👋  

This repository documents my journey of learning **Seaborn**, one of the most powerful Python libraries for data visualization.  
I explored step by step with theory, syntax, and practical examples using the **Titanic dataset** and other built-in datasets.  

---

## 🚀 Path of Learning  
### 🔹 1. Getting Started  
- Loaded built-in Seaborn datasets (`penguins`, `titanic`, etc.)  
- Explored data using `head()`, `info()`, `describe()`.  

### 🔹 2. Basic Plots  
- **Scatter Plot** → relationship between two numeric variables  
- **Line Plot** → trends and changes over a variable  
- **Bar Plot** → compare averages between categories  
- **Count Plot** → frequency of categorical values  

### 🔹 3. Distribution Plots  
- **Histogram** → frequency distribution of continuous data  
- **KDE Plot** → smooth probability distribution curves  
- **Box Plot** → spread, quartiles, and outliers  
- **Violin Plot** → combination of box + KDE  

### 🔹 4. Categorical & Point Plots  
- **Strip Plot** → scattered data points on categories  
- **Swarm Plot** → arranged data points without overlap  
- **Bar Plot (with error bars)** → mean + confidence intervals  

### 🔹 5. Advanced & Multivariate Plots  
- **Pair Plot** → relationships between multiple features  
- **Heatmap** → correlation matrix visualization  
- **FacetGrid / Catplot** → multiple plots across subsets of data  
- **PairGrid (on Penguins dataset)** → customized grid for pairwise plots  

---
## 📌 Key Learnings  
- Styling with **themes, palettes, and figure size**  
- Using `hue`, `style`, and `size` for better categorical distinction  
- Adding **titles, labels, and legends** for professional presentation  
- Saving plots using `plt.savefig()` for reports and GitHub  

---

### 🔹 Pair Grid Example  
**About:**  
PairGrid is a subplot grid for plotting pairwise relationships across a dataset.  
It gives you full control over how to visualize upper, lower, and diagonal parts of the grid.  

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Load dataset
penguins = sns.load_dataset("penguins")

# pair grid -> subplot grid for plotting pairwise relationships in a data set
graph = sns.PairGrid(data=penguins, hue="sex", palette="bright")

graph.map_upper(sns.scatterplot)  # upper Triangle
graph.map_lower(sns.kdeplot)      # lower Triangle
graph.map_diag(sns.histplot)      # diagonal

# save figure
plt.savefig("pair_grid.png", dpi=300, bbox_inches="tight")

# add legend
graph.add_legend()
plt.show()
```
## 👤 Author  
**Purvesh**  
📍 Exploring Data Science step by step!  
