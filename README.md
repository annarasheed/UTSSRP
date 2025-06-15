
# UTSSRP - Dimensionality Reduction and Clustering Techniques for Hi-C Genomic Data Analysis
This project was completed during the inaugural University of Toronto Statistical Sciences Research Program.
It focuses on constructing and analyzing chromosome contact matrices based on genomic interaction data. The goal of the project was to evaluate the performance of various dimensionality reduction methods such as PCA, UMAP, and t-SNE, in effectively separating the 4 different cell types available in our dataset.
The main objectives of the project are:

#### 1. Data Preprocessing
- Process raw Hi-C data to form block-diagonal contact matrices where each block represents intra-chormosonal contacts between gene loci pairs for that chromosome
- Binarized the contact matrices to emphasize the presence of absence of interactions.
- Flatten the upper-triangular part of each cell's block-diagonal contact matrix into a one-dimensional feature vector, stacked vertically to form the data matrix X.

#### 2. Filtering
- Ranked cells by the mean number of non-zero entries in their contact matrices and removed the bottom 25% of cells.
- Ranked chromosomes based on their average absolute PC1 loading values and retained the top 75% of chromosomes for further analysis. 

#### 3. Dimensionality Reduction Techniques
- Applied:
    - PCA
    - PCA + UMAP
    - Weighted PCA
    - t-SNE
    - Kernal-style PCA
    - Kernal-style PCA + UMAP
  
#### 4. Analysis and Comparison
- Applied K-means clustering and Spectral clustering to each technique
- Calculated ARI scores for each technique using the filtered and unfiltered data
- Calculated run-times for each technique

## Contributors
- Anna Rasheed [@annarasheed](https://github.com/annarasheed)
- Kini Chen [@kinichen](https://github.com/kinichen)
- Benjamin Jagdeo 
- Saladin Shaurov [@saladinshaurov](https://github.com/saladinshaurov)
- Supervisor: Professor Elena Tuzhilina





