

# \~Core Workflow\~
## Params
- Project name
- In/Out directories
- output figures Y/N?
- output data Y/N?
- aesthetic parameters (default font, color palettes,  gg theme)

## ## Step 1 Package/Helper Import and Housekeeping


## Step 2 Data Import & Pre-Processing
#### Input from search tools
- MaxQuant
- Spectronaut
- Fragpipe
- DIANN ?
Combine multiple input files if necessary
Remove imputed values
Ensure standardized run names
#### Normalization 
Method determination (eq median, ... other?)
plot intensity distributions before-after normalization
#### Summarize to protein-level data OR to PTM Sites

***Data Out:*** 
- *Protein Level Intensity Data*
- *Peptide Level Intensity Data*
- ( *Site Level Intensity Data* )

## Step 3 Basic Quality Control
- *Plot run-by-run distributions of peptide id count and protein id count*
- *plot run-by-run correlation matrix*
- *Plot run-by-run PCA*
- *Plot run x Protein ID Heatmaps*, unclustered to see trends directly, clustered to verify within-treatment consistency

Circle back to protein summarization for any runs removed

Circle back to normalization if batch correction of some kind needs to be applied or median normalization is inappropriate

## Step 4 Differential Expression Analysis
#### Compute difference between discrete conditions with MSS
- *plot volcano* 
- *plot violin/density distribution
- ***Data Out:*** 
	- *Group Comparison Data*
#### Perform gene set enrichment
- wrappers for easy preparation of gene groups to pass to enrichment (ex: test upregulated, downregulated, and all significant as separate sets by rbinding) 
- fisher test and KS test methods, GO and msigdb and CORUM and own provided gene sets
- *plot enrichment heatmap* of top N enrichments for many groups 
- *plot lollipop plot* for < 8  gene sets
- ***Data Out:*** 
	- *Enrichment Table Data*


# \~Modality-Specific Workflow\~

## PPI Scoring

## Kinase Enrichment

## Multivariate  Expression Analysis 

# \~Accessory Segments\~
## Detailed Heatmap Builder
