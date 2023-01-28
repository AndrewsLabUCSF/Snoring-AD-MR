# Snoring-AD-MR
Investigating the causal relationship between snoring and Alzheimer's disease. 

## Background
Loud snoring is a symptom commonly associated with obesity and obstructive sleep apnea (OSA), which have both been suggested as risk factors for Alzheimer’s disease (AD). However, it remains unclear whether snoring might be causally linked to AD and if body mass index (BMI) may play a role in this relationship. Here we use bidirectional and multivariable Mendelian randomization (MR) analysis to investigate the causal relationship between snoring and AD.

## Methods 
### Datasets
Snoring

* Campos, A. I. et al. Nat Commun 11, 817 (2020).
* Genome-wide association study on snoring (n ~ 408,000; snorers ~ 152,000) using data from the UK Biobank. Identified 42 genome-wide signiﬁcant loci, with an SNP based heritability estimate of ~10% on the liability scale
* Also Snoring adjusted for BMI

Sleep Apnea + Snoring

* Campos, A. I. et al. Sleep (2022).
* genome-wide association study (GWAS) meta-analysis of sleep apnoea across five cohorts (NTotal=523,366), followed by a multi-trait analysis of GWAS (MTAG) to boost power, leveraging the high genetic correlation between sleep apnoea and snoring. Replicated top findings in 23andMe. 49 Signficant loci, with twenty nine replicated in 23andMe

BMI

* Lock et al Nature 2015
*  To understand the genetic basis of obesity better, here we conduct a genome-wide association study and Metabochip meta-analysis of body mass index (BMI), a measure commonly used to define obesity and assess adiposity, in up to 339,224 individuals. This analysis identifies 97 BMI-associated loci, 56 of which are novel.  

Alzheimer's disease 

* Kunkle, B. W. et al. Nat Genet 51, 414–430 (2019).
* Genome-wide association study on Alzheimer's disease (n = 94,437) using data from the International Genomics Alzheiemr's Project. Identified 20 genome-wide signiﬁcant loci

## Aim 1. 

**Determine if snoring is causally associated with Alzheimer's disease** 

Genetic instruments were obtained by selecting independent genome-wide significant SNPs (p < 5e-8, r2 = 0.001, window = 10Mb) for each exposure and harmonizing their effects with each outcome. We used fixed-effects inverse-variance weighted (IVW) meta-analysis as the primary method, and MR-Egger, Weighted mode, Weighted median, radial-MR, estimators as sensitivity analyses. Heterogeneity was assessed using Cohcrans Q test, and pleiotropy using the MR-Egger intercept.

## Aim 2. 
**Estimate if Alzheimer's disease is causally associated with snoring**

Genetic instruments were obtained by selecting independent genome-wide significant SNPs (p < 5e-8, r2 = 0.001, window = 10Mb) for each exposure and harmonizing their effects with each outcome. We used fixed-effects inverse-variance weighted (IVW) meta-analysis as the primary method, and MR-Egger, Weighted mode, Weighted median, radial-MR, estimators as sensitivity analyses. LHC-MR was further used to investigate birectional effects accounting for potential heritable confounders. Heterogeneity was assessed using Cohcrans Q test, and pleiotropy using the MR-Egger intercept.

## Aim 3. 

**Evaluate if the causal effect of Alzheimer's disease on snoring is mediated by BMI**
The study employed a multivariable Mendelian randomization (MR) approach to investigate the causal relationship between body mass index (BMI) and Alzheimer's disease (AD) and their potential mediation by snoring. Independent genome-wide significant SNPs (p-value < 5e-8, linkage disequilibrium (LD) r2 = 0.001, window = 10Mb) for BMI and AD were extracted from their respective GWAS studies, and from each other to generate a combined list of SNPs. Proxy-variants (r2 > 0.8, EUR) were used in place of SNPs not available in the GWAS. The combined list of SNPs was then clumped to retain only independent genome-wide significant SNPs (p-value < 5e-8, LD r2 = 0.001, window = 10Mb) across both exposures. These SNPs were then extracted from the outcome variable, snoring. Multivariable MR extensions, including IVW, MR-Egger, Weighted mode, Weighted median, and radial MR, were subsequently used to evaluate the causal effect of AD on snoring, mediated by BMI.