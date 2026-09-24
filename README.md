# Phylogeny_Basics: A Mini Bioinformatics Project on Viral Phylogeny 🧬

An exploratory bioinformatics mini-project analyzing the basic genetic architecture of SARS-CoV-2 (COVID-19), observing its exact mutation rate against SARS-CoV (2003), and mapping its phylogenetic relationships with other Betacoronaviruses using Python and Google Colab.

## 🎯 Project Objective
The main objective of this mini-project is to practice analyzing real biological data using fundamental bioinformatics tools. It focuses on calculating basic genomic metrics (such as nucleotide distribution and GC content), observing exact base-by-base point mutations between two reference strains, and utilizing an automated NCBI BLAST search to construct a modest phylogenetic tree. This provides a visual representation of the genetic distances and host origins of various coronavirus strains.

## 🛠️ Technologies Used
* **Python**: Data analysis and programming language.
* **Google Colab**: Cloud-based development and execution environment.
* **Biopython**: Used for database connection (Entrez), sequence parsing (SeqIO), automated BLAST searches (NCBIWWW), and phylogenetic tree generation.
* **MAFFT**: A multiple sequence alignment (MSA) program used to align viral genomes to detect mutation regions.
* **Pandas**: Used for organizing genetic data and genomic metrics into a tabular format.
* **Matplotlib**: Used for visualizing nucleotide distributions, genomic stability, and the final phylogenetic tree.
* **NCBI Database**: The primary data source from which reference genetic sequences (FASTA) and BLAST relatives were automatically obtained.

## 📊 Analysis Steps
1. **Automated Data Collection**: Reference genomes for COVID-19 (NC_045512) and 2003 SARS (NC_004718) are dynamically downloaded directly from the NCBI server using Biopython's Entrez module.
2. **Genomic Profiling (Length & GC Content)**: The total genome length, exact nucleotide counts (A, T, G, C), and GC content (percentage of Guanine and Cytosine) are calculated to evaluate genomic stability.
3. **Exact Mutation Analysis**: The COVID-19 and SARS (2003) genomes are aligned using MAFFT to perform a precise base-by-base comparison, extracting the total number of point mutations and the exact mutation rate.
4. **Targeted BLAST Search**: An automated BLAST search is executed against the NCBI database. It is intelligently filtered by Taxonomy ID (Betacoronaviruses - `txid694002`) and the Gold Standard RefSeq database to extract 15 distinct, high-quality genetic relatives (e.g., bat, pangolin, camel variants) while preventing server timeouts. 
5. **Multiple Sequence Alignment**: The 15 distinct relatives plus the COVID-19 reference are aligned simultaneously using MAFFT.
6. **Phylogenetic Tree Construction**: An identity-based genetic distance matrix is calculated from the alignment. A COVID-19-rooted phylogenetic tree is then generated, complete with metadata parsing to display exact host origins and genetic similarity percentages.
7. **Visualization**: All findings are exported as high-resolution plots, including comparative bar charts for nucleotide distributions and a comprehensive, color-coded phylogenetic tree.

## 🚀 How to Run the Project
The entire pipeline is fully automated and designed to run seamlessly in the cloud. You do not need to download or upload any biological data manually.

1. Open the `COVID19_SARS_Comparative_Genomics.ipynb` file in **Google Colab**.
2. In **Cell 3** and **Cell 4**, update the `Entrez.email = "your_email@gmail.com"` variable with your actual email address (required by NCBI guidelines to access their servers).
3. Run the code cells sequentially from top to bottom.
4. The script will automatically install the required tools (MAFFT, Biopython), fetch the FASTA files from the internet, run the alignments, and generate the charts and the phylogenetic tree right in your browser!
