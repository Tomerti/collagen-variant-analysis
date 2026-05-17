# Collagen Variant Analysis Pipeline

Computational genomics project analyzing 35,000+ collagen-gene variants across 1TB of biological annotation data.

The pipeline integrates ClinVar, Ensembl VEP, gnomAD, dbNSFP, and Mutalyzer to perform HGVS normalization, large-scale functional annotation, pathogenicity scoring, glycine-hotspot mapping, and ECM candidate-gene prioritization.

## Research Brief

[View Research Brief](docs/hEDS-research-brief.pdf)

## Highlights

- Processed 35,788 collagen-gene variants
- Integrated ClinVar, Ensembl VEP, gnomAD, dbNSFP, and Mutalyzer
- Processed 1TB of biological annotation data
- Generated collagen-family glycine hotspot mapping
- Prioritized ECM candidate genes including COL12A1 and COL6A3
- Reduced large-scale annotation lookup time from 22h → 40m using SQLite indexing

## Pipeline Architecture

```text
ClinVar Extraction
        ↓
HGVS Generation / Normalization
        ↓
Ensembl VEP Annotation
        ↓
dbNSFP + gnomAD Annotation
        ↓
Mutalyzer Validation / Protein HGVS Conversion
        ↓
Rare & Damaging Variant Filtering
        ↓
SQLite Indexed Storage / Query Optimization
        ↓
Structural Domain Mapping
        ↓
Statistical Analysis
        ↓
Glycine Hotspot Mapping & Candidate Prioritization
```

## Tech Stack

Python · Pandas · SQLite · ClinVar · Ensembl VEP · gnomAD · dbNSFP · Mutalyzer

## Note

This is a public showcase repository for an independent computational genomics project. The full research pipeline is not currently published.
