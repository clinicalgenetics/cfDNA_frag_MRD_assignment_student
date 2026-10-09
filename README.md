# Assignment: Exploring cfDNA Fragmentomics for MRD Detection

**Author:** Dmytro Kryvokhyzha ([dmytro.kryvokhyzha@ki.se](mailto:dmytro.kryvokhyzha@ki.se)), Karolinska Institutet

*Estimated completion time: 3–4 h*

## Background

You are given targeted sequencing data from several longitudinal plasma samples from a lymphoma patient. A set of candidate SNVs identified from the patient's baseline tumour is provided.

The aim is to explore whether cfDNA fragment characteristics could provide additional information for detecting low-frequency MRD variants.

## Data provided

All files are in the `data/` folder of this repository:

- `baseline.vcf` — candidate SNVs identified from the baseline tumour
- `T1.bam`, `T2.bam`, `T3.bam` — three longitudinal plasma samples (paired-end, with `.bai` index files)
- `reference.fa` — reference sequence of the targeted region (with `.fai` index)

*The data is simulated.*

## Tasks

### 1. Explore the candidate variants

For each candidate SNV, calculate or extract:

- VAF at baseline
- number of supporting reads
- VAF across the three time points

Create one figure showing how the VAF of the candidate SNVs changes over time.

Briefly identify which variants you consider most likely to represent MRD and explain why.

### 2. Explore fragment length

For reads overlapping the candidate SNVs:

- calculate the fragment size
- compare fragment-length distributions between variant-supporting and non-supporting reads

Create one figure illustrating your findings.

### 3. Test in-silico ctDNA enrichment (optional)

Tumour-derived cfDNA fragments tend to be shorter than those from healthy cells. Keep only fragments shorter than 150 bp, then:

- recalculate the VAF and the number of supporting reads for each candidate SNV and time point
- compare the results with those obtained using all fragments

Does size selection make MRD easier to detect? What are the trade-offs? You may add one figure or table for this task.

### 4. Short interpretation

In **~200–300 words** (in your README), answer:

Do your results suggest that fragmentomics could potentially improve MRD detection? What would you investigate next?

Please mention any important limitations of your analysis or problems you could not solve.

## Deliverables

Please submit your solution as a pull request to this repository, containing:

- **R/Python/Bash scripts or a notebook**
- **two figures** (plus an optional figure or table for Task 3)
- **a short README** that:
    - explains how to run your analysis
    - includes your **~200–300-word interpretation** (Task 4)

We will assess your approach to the problem, data analysis, biological interpretation, and code.

**It is completely fine if you are not able to complete all parts of the assignment.** If you encounter something that does not work or that you are not sure how to solve, please describe what you tried, why you chose that approach, and what happened. We are interested not only in the final results, but also in how you approach unfamiliar problems and troubleshoot them.
