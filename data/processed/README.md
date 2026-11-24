# Population Data Documentation

## Overview

This directory contains the population-level allele-frequency data used in the pharmacogenomic investigation of the **CYP2C19*2 variant (rs4244285)** and its potential influence on clopidogrel response.

The analysis examines the distribution of the variant across different ancestry groups and selected populations using three population datasets.

## Dataset Organization

The population data are organized as follows:

```text
data/
├── README.md
├── raw/
│   └── README.md
└── processed/
    ├── gnomad_frequencies.csv
    ├── south_asian_frequencies.csv
    └── hgdp_frequencies.csv
```

### 1. gnomAD

**File:** `processed/gnomad_frequencies.csv`

Contains CYP2C19*2 allele-frequency information across broad genetic ancestry groups from the combined Exomes and Genomes dataset.

The dataset includes:
- South Asian
- East Asian
- Amish
- African/African American
- European Finnish
- European non-Finnish
- Ashkenazi Jewish
- Admixed American
- Middle Eastern
- Other reported categories

### 2. Selected South Asian Populations

**File:** `processed/south_asian_frequencies.csv`

Contains population-level allele-frequency data for five selected South Asian populations:

- Sri Lankan Tamil (STU)
- Indian Telugu (ITU)
- Punjabi (PJL)
- Bengali (BEB)
- Gujarati Indian (GIH)

### 3. Human Genome Diversity Project (HGDP)

**File:** `processed/hgdp_frequencies.csv`

Contains CYP2C19*2 allele-frequency data for selected HGDP population groups:

- Sindhi
- Balochi
- Burusho
- Brahui
- Makrani
- Hazara
- Pathan
- Uyghur
- Kalash

## Data Dictionary

| Column | Description |
|---|---|
| population | Population or ancestry group |
| population_identifier | Population identifier, where available |
| allele_count (AC) | Number of alternate alleles observed |
| allele_number (AN) | Total number of alleles assessed |
| homozygotes | Number of individuals homozygous for the alternate allele, where available |
| allele_frequency_percent | Alternate allele frequency expressed as a percentage |

## Allele Frequency Calculation

Allele frequency is expressed as:

\[
AF(\%)=\frac{AC}{AN}\times100
\]

Where:

- AC = Alternate allele count
- AN = Total allele number

The reported frequencies are retained in percentage format.

## Data Interpretation

The allele frequencies describe the proportion of sampled alleles corresponding to CYP2C19*2 within each population dataset.

**Allele frequency must not be interpreted as carrier prevalence or the proportion of individuals who will experience reduced clopidogrel response.**

Population-level allele frequencies also do not independently establish individual clinical risk.

## Data Handling and Limitations

- Population datasets have different sampling designs and population classifications.
- Sample sizes vary between population groups.
- Small sample sizes may produce less precise frequency estimates.
- Frequencies from different datasets should not be directly pooled.
- Combined rows represent the reported dataset totals and should not be treated as additional independent populations.
- Original reported population values are retained for this research analysis.

## Data Sources

The analysis uses information from the following population resources:

1. [gnomAD – Genome Aggregation Database](https://gnomad.broadinstitute.org/)
2. [1000 Genomes Project](https://www.internationalgenome.org/)
3. [Human Genome Diversity Project](https://www.coriell.org/1/NHGRI/Collections/Human-Genome-Diversity-Project)

Exact dataset releases, source records and retrieval details should be documented alongside the corresponding processed datasets.

## Research Context

These population datasets support the population genetics component of the project:

**Pharmacogenomic Analysis of CYP2C19*2 and Its Impact on Clopidogrel Response.**
