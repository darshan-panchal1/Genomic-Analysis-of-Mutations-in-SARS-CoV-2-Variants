# Comparative Analysis of Wuhan-Hu-1 and Delta-1/2021 Strains in SARS-CoV-2 RNA Sequences

## Problem Statement

The genetic material of the SARS-CoV-2 virus, responsible for COVID-19, is composed of RNA. RNA sequences play a vital role in the virus's replication and protein synthesis. Understanding the specific RNA sequences is crucial for tracking the virus's evolution and identifying emerging variants. This project focuses on comparing the RNA sequences of the Wuhan-Hu-1 (reference) and Delta-1/2021 strains, examining variations that may impact the virus's behavior, transmissibility, and immune response evasion.

## Background

The coronavirus's RNA serves as a template for viral protein synthesis, and changes in the RNA sequence can significantly influence the virus's properties. The study involves extracting relevant insights from a dataset containing information on different SARS-CoV-2 variants. By analyzing and comparing RNA sequences, researchers can gain valuable information for developing targeted interventions, including vaccines and treatments.

## Project Overview

1. **Data Collection**: The dataset of coronavirus variants was obtained from the NCBI website.

    ```python
    import pandas as pd

    # Read the dataset
    df = pd.read_csv("ncbi_datasets.csv", low_memory=False)
    ```

2. **Data Cleaning and Exploration (EDA)**: Examined data types, missing values, and performed exploratory data analysis.

    ```python
    # Data cleaning
    df['Collection Date'] = df['Collection Date'].apply(parse_date)
    df["Continents"] = df["Geo Location"].str.replace(";.+", "", regex=True)

    # Exploratory Data Analysis
    # (e.g., checking null values, data types, and summary statistics)
    ```

3. **Comparative Analysis**: Analyzed the nucleotide lengths, number of samples collected per month, and performed comparisons between different strains.

    ```python
    # Comparative Analysis
    # (e.g., nucleotide length statistics, samples per month, strain comparisons)
    ```

4. **Sequence Alignment**: Utilized BioPython to align RNA sequences and calculate the similarity percentage.

    ```python
    # Sequence Alignment
    # (e.g., using BioPython to align RNA sequences and calculate similarity)
    ```

5. **Mismatches Visualization**: Visualized sequence mismatches to identify deletions, substitutions, and insertions.

    ```python
    # Mismatches Visualization
    # (e.g., color-coded display of sequence mismatches)
    ```

## Results and Conclusions

The project provides a comprehensive analysis of the Wuhan-Hu-1 and Delta-1/2021 SARS-CoV-2 strains, highlighting variations in RNA sequences. The percentage similarity, deletions, substitutions, and insertions were examined to understand the impact of mutations. This information is crucial for monitoring the virus's evolution and guiding public health strategies.

## Acknowledgments

The project acknowledges the National Center for Biotechnology Information (NCBI) for providing the dataset and tools used in the analysis.

## References

- Cleveland Clinic. (2020). Image source: [clevelandclinic.org](https://my.clevelandclinic.org/health/articles/18081-coronavirus-covid-19-infection-and-spike-proteins)

- Images: [biologydictionary.net](https://biologydictionary.net), [National Human Genome Research Institute](https://www.genome.gov), [Thomas Splettstoesser](https://www.scientificanimations.com), [freepik.com](https://www.freepik.com)
