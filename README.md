# Antibiotic Resistance in Cutibacterium acnes: A Python-Based Analysis
## Project Overview

This independent research project explores antibiotic resistance in Cutibacterium acnes, a bacterium associated with acne vulgaris. It examines patterns of antibiotic resistance across published studies and compares the effects of topical clindamycin alone versus clindamycin combined with benzoyl peroxide (BPO).

Using published research data, I conducted two descriptive secondary analyses with Python. The first examines treatment-related changes in antibiotic-resistant bacterial counts and acne lesions over 16 weeks. The second explores antibiotic resistance rates across 23 published studies involving 2,046 C. acnes isolates.

The goal is to better understand antibiotic resistance in acne treatment while developing practical skills in data extraction, analysis, visualization, and reproducible research.

## Research Questions

1. What patterns of antibiotic resistance are reported in C. acnes across different antibiotics and studies?
2. How do clindamycin-resistant bacterial counts change during topical acne treatment?
3. How does combining clindamycin with benzoyl peroxide compare with clindamycin monotherapy?
4. What limitations should be considered when interpreting published antibiotic resistance data?

## Analysis 1: Clindamycin Monotherapy vs. Combination Therapy

#### Source: Cunliffe et al. (2002)
https://www.sciencedirect.com/science/article/pii/S0149291802800236


#### Methods

I manually extracted published summary data from Tables III and V of the clinical trial.

Using Python, Pandas, and Matplotlib, I:
- Visualized mean log10 changes in clindamycin-resistant C. acnes counts at weeks 4, 8, 12, and 16.
- Compared median percentage changes in total acne lesion counts.
- Calculated descriptive between-group differences over time.

#### Key Findings
Antibiotic resistance: At week 16, the mean log10 change in clindamycin-resistant C. acnes counts was −0.2 for combination therapy and +1.2 for clindamycin alone. The original study reported a statistically significant between-group difference (p = 0.018).

Clinical efficacy: At week 16, the median reduction in total acne lesions was 52.7% with combination therapy and 27.5% with clindamycin alone, a difference of 25.2 percentage points.

Between-group comparison: The descriptive difference in mean log10 changes in resistant bacterial counts increased from 0.0 at week 4 to 1.4 at week 16, with higher values in the clindamycin-only group.

These calculations use published group-level summary statistics. No new statistical significance tests were performed.

#### Project Files: [Analysis_1_Cunliffe_2002](https://github.com/cjjde05/acne-antibiotic-resistance-analysis/tree/main/Analysis_1_Cunliffe_2002) 

## Analysis 2: Antibiotic Resistance Across Published Studies

#### Source: Zhu et al. (2025), systematic review and meta-analysis.
https://pmc.ncbi.nlm.nih.gov/articles/PMC12174412/

#### Methods

I organized study-level antibiotic resistance data from the supplementary material of Zhu et al. (2025), covering 23 studies and 2,046 C. acnes isolates.

Using Python, Pandas, and Matplotlib, I:
- Calculated descriptive aggregate resistance percentages for 11 antibiotics.
- Compared resistance percentages across studies.
- Examined variation in clindamycin resistance by study and country.
- Visualized antibiotic resistance patterns and differences in available reporting.

For each antibiotic, the descriptive aggregate percentage was calculated as the sum of reported resistant isolates divided by the sum of isolates from studies reporting that antibiotic, assuming the reported study sample size represented the number tested.

These calculations are distinct from the pooled resistance estimates reported in the original meta-analysis.

#### Key Findings
Antibiotic differences: The calculated descriptive aggregate resistance percentages were 35.33% for erythromycin, 27.98% for clindamycin, 3.79% for doxycycline, and 1.57% for minocycline.

Variation across studies: Clindamycin resistance percentages varied substantially among the 18 studies reporting this antibiotic, ranging from 0% to approximately 56.82%.

Geographic differences: Descriptive clindamycin resistance percentages also differed across the countries represented in the dataset. However, the number of studies and isolates varied by country, limiting direct comparisons.

These findings describe patterns in the extracted dataset and should not be interpreted as causal relationships or nationally representative resistance estimates.

#### Project Files: https://github.com/cjjde05/acne-antibiotic-resistance-analysis/tree/main/Analysis_2_Zhu_2025

## Tools and Skills
- Python: Data analysis and reproducible workflows
- Pandas: Data organization and descriptive calculations
- Matplotlib: Data visualization
- Google Colab: Notebook development and execution
- GitHub: Project organization and documentation

## Limitations
This project uses published summary data rather than individual patient-level observations. Both analyses are descriptive and do not represent new clinical trials or independent meta-analyses.

In Analysis 1, the findings are based on a single clinical trial and cannot be generalized to all patients or treatment settings.

In Analysis 2, studies differed in geographic location, sample size, antibiotic susceptibility testing methods, and resistance criteria. Not all studies reported results for every antibiotic. The aggregate percentages assume that the study-level isolate counts are appropriate denominators for each reported antibiotic; the supplementary table does not independently confirm antibiotic-specific testing denominators.

The descriptive aggregate resistance percentages should not be confused with the pooled estimates from Zhu et al. (2025), which used meta-analytic methods.

## Future Directions
Future work will focus on reviewing molecular mechanisms of antibiotic resistance in C. acnes, examining evidence related to antibiotic exposure, and evaluating non-antibiotic or combination acne treatment strategies.

## Author

Claire Jeong  
University of Illinois Urbana-Champaign  
Major: Molecular and Cellular Biology  
Minor: Data Science
