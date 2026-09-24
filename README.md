# Phylogeny_Basics
A beginner bioinformatics project analyzing and comparing the genetic sequences of SARS-CoV-2 and SARS-CoV using Python. 
Basic phylogenetic analysis comparing COVID-19 and SARS virus genomes using Pandas and Google Colab.

# Phylogeny_Basics: Genetic Comparison of Coronaviruses 🧬

This project is a fundamental evolutionary bioinformatics (phylogenetic) study comparing the genetic sequences of SARS-CoV-2 (COVID-19) and SARS-CoV (2003) viruses using Python.

## 🎯 Project Objective
The main objective of this study is to analyze real biological data (in FASTA format) to calculate nucleotide distributions, determine GC content, estimate basic sequence similarity, and construct a phylogenetic tree to visualize the evolutionary relationship and structural differences between coronavirus strains.

## 🛠️ Technologies Used
* **Python**: Data analysis and programming language.
* **Pandas**: Used for organizing genetic data into a tabular format.
* **Matplotlib**: Used for visualizing nucleotide distributions and genomic metrics.
* **Biopython**: Used for sequence alignment, mutation analysis, and generating the phylogenetic tree.
* **Google Colab**: Cloud-based development environment.
* **NCBI Database**: The data source from which genetic sequences (FASTA) were obtained.

## 📊 Analysis Steps
1. **Data Collection:** Reference genomes of the current COVID-19 (NC_045512) and 2003 SARS (NC_004718) viruses were downloaded from the NCBI database in FASTA format.
2. **Data Processing:** Headers in the FASTA files were cleaned using Python to extract only the pure genetic codes.
3. **Genomic Metrics (Length & GC Content):** The total genome length and the GC content (percentage of Guanine and Cytosine) were calculated for both viruses to evaluate genomic stability.
4. **Nucleotide Counting:** The total number of Adenine (A), Thymine (T), Guanine (G), and Cytosine (C) bases was computed.
5. **Basic Mutation Analysis:** The sequences were compared to estimate the basic structural differences and genetic similarity percentage.
6. **Phylogenetic Tree Construction:** A basic evolutionary tree (dendrogram) was generated using Biopython to visually represent the genetic divergence and ancestral relationship between the viral strains.
7. **Visualization:** The obtained data and genomic metrics were plotted comparatively as bar charts using Pandas and Matplotlib.

## 🚀 How to Run the Project
1. Download the `.fasta` files from this repository.
2. Open the `COVID19_SARS_Comparative_Genomics.ipynb` file in Google Colab.
3. Upload the FASTA files to the Colab environment.
4. Run the code cells sequentially to examine the charts, calculations, and the phylogenetic tree!

---
*This project was created to learn how biological data can be analyzed using software tools.*
