# NCBI PubMed and Bookshelf Gene Query Script

## Overview
This Jupyter Notebook automates the process of searching NCBI's PubMed and Bookshelf databases for papers and books that mention a given list of genes in the context of treatments or interventions. The results, which include the gene name, search terms used, search filters, and the number of results found, are saved to CSV files.

## Dependencies
- Python 3.9+
- Biopython (`Bio`)
- pandas
- csv

## How to Use
1. **Set up the Environment:** Make sure to install all the dependencies listed above. If you haven't installed them, you can do so using pip:
    ```bash
    pip install biopython pandas
    ```
2. **Input:** The genes of interest should be listed in the `genes_of_interest` Python list.
    ```python
    genes_of_interest = ['ABCC8', 'ACTB', 'ACTG1', 'ADAR', 'ADCY5', 'ADNP']
    ```
3. **Configuration:** Set your email address in the `Entrez.email` field. This is required for programmatic access to NCBI databases.
    ```python
    Entrez.email = "your.email@example.com"
    ```
4. **Run the Notebook:** Execute all cells in the notebook. 
5. **Output:** Two CSV files will be generated, `pubmed_output.csv` and `books_output.csv`, which contain the search results for PubMed and NCBI Bookshelf, respectively.

## Output Schema
The generated CSV files will have the following columns:
- `Gene`: The gene of interest.
- `Search Term`: The search term used in the query.
- `Search Filter`: Any filters applied to the query.
- `Number of Results`: The number of search results obtained.
