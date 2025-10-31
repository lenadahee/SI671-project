# The Hidden Palette: Mining Co-Occurring Fashion Attributes
## [SI 671 / Group 3, "RLV"] Lena Choi, Robert Collis, Vaishnavi Venkataraghavan

### OVERVIEW
**Research Question:** What attribute combinations frequently occur together across fashion products?
Can we uncover fashion item clusters using categorical features?

**Why it matters:** The fashion industry moves fast. Understanding how product attributes (color × season × category) cluster helps retailers plan next season’s palette,   optimize inventory, and improve recommender systems.
Ultimately,this project explores how product attributes co-occur and form patterns across a large fashion catalog.

### BACKGROUND / OBJECTIVES:
Traditional retail analytics relies on market-basket analysis to find products that appear together  and clustering to reveal broader style groups.
We combine these approaches:
- **Association Rules (Apriori)** to extract “if–then” patterns among attributes
- **Dimensionality Reduction (MCA / PCA)** to map categorical data into a 2-D space
- **Clustering (K-Means)** to form interpretable product segments


### DATA OVERVIEW:
- **Source:** [Fashion Product Images (Small) – Kaggle](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-small/data)
- **Format:** CSV (excluding images) = 'styles.csv'. [**NOTE:** Our group has already converted into a CSV file]
- **Rows:** 44,424 products
- **Columns Used:** `gender`, `subCategory`, `articleType`, `baseColour`, `season`
-  **Primary categories:** 48 % apparel / 25 % accessories / 26 % other

### REPRESENTATION: **Itemsets**
- Each product in `styles.csv` is treated as a transaction / basket of categorical attributes.

### PRE-PROCESSING:
- Standardized text case & whitespace
- Normalized seasons - {spring, summer, fall, winter }
- Encoded categorical attributes → transaction matrix for Apriori / MCA / Clustering

### TECHNIQUES:
- **Association Rule Mining (Apriori):** Identify frequent co-occurring attributes with support, confidence, and lift
- **Dimensionality Reduction (MCA / PCA):**   Compress high-dimensional categorical space for visualization
- **Clustering (K-Means):** Group similar products into interpretable style segments

### EVALUATION METRICS:
- **Apriori:** Support, confidence, lift (+ redundancy pruning)
- **Dimensionality Reduction:** Variance explained by components
- **Clustering:** Silhouette score for k optimization

### VISUALIZATIONS:
- MCA scatterplots showing season and gender groupings
- Heatmaps of cluster profiles (top colors × item types × seasons)
- Table of top Apriori rules (support, confidence, lift)
- Trend lines for color frequency by year and season

### TOOLS & LIBRARIES USED:
- Python: pandas, mlxtend, prince, scikit-learn, matplotlib
- Jupyter Notebook: data analysis and visualization
- VS Code: coding, documentation, and local development
- GitHub: version control and team collaboration

### PROJECT REPOSITORY:
GitHub Repository: https://github.com/lenadahee/SI671-project