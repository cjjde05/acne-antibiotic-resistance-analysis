# Antibiotic Resistance in Cutibacterium acnes: A Python-Based Analysis
## Project Overview

This independent research project explores antibiotic resistance in *Cutibacterium acnes*, a bacterium associated with acne.

Using published research data and Python, I conducted four descriptive analyses focusing on topical antibiotic treatments, resistance rates across studies, genetic mutations linked to resistance, and changes in bacterial resistance during combination treatment.

The goal is to better understand antibiotic resistance in acne treatment while building skills in data analysis, visualization, and scientific research.

## Research Questions

1. What patterns of antibiotic resistance are reported in *C. acnes* across published studies?
2. What genetic mutations are associated with antibiotic resistance in *C. acnes* and related bacteria?
3. How does clindamycin monotherapy compare with combination treatment in terms of antibiotic resistance and acne improvement?
4. How do bacterial detection and resistance change during long-term topical combination treatment?

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

#### Project Files: [Analysis_2_Zhu_2025](https://github.com/cjjde05/acne-antibiotic-resistance-analysis/tree/main/Analysis_2_Zhu_2025)

## Analysis 3: Genetic Mechanisms of Antibiotic Resistance

#### Source: Ross et al. (1997), study of antibiotic-resistant clinical isolates.
https://pmc.ncbi.nlm.nih.gov/articles/PMC163871/

#### Methods

I used published data from Ross et al. (1997) to examine genetic mutations associated with antibiotic resistance in acne-related bacteria.

Using Python, Pandas, and Matplotlib, I:
- Organized data from 26 mutation-positive resistant clinical isolates.
- Calculated the frequency of three reported 23S rRNA mutations.
- Compared mutation patterns and reported antibiotic susceptibility.
- Created graphs to show the distribution of resistance-related mutations.

The 26 clinical isolates included 22 P. acnes isolates (now called C. acnes) and 4 isolates from other related species.

#### Key Findings

Mutation frequencies: A2058G was found in 13 isolates (50.0%), A2059G in 7 isolates (26.9%), and G2057A in 6 isolates (23.1%).

Resistance mechanisms: These mutations affect the bacterial ribosome, which is a target of certain antibiotics. Changes in this region can reduce antibiotic effectiveness.

Genetic differences: The results show that different mutations can be associated with antibiotic resistance.

These findings help explain how antibiotic resistance can develop at the molecular level. However, this analysis only describes the resistant isolates reported in the study and does not measure how common these mutations are in the general C. acnes population.

#### Project Files: [Analysis_3_Ross_1997](https://github.com/cjjde05/acne-antibiotic-resistance-analysis/tree/main/Analysis_3_Ross_1997_files)


## Analysis 4: Topical Combination Treatment and Antibiotic Resistance

#### Source: Ghannoum et al. (2025), 24-week analysis of topical combination treatment.
https://pubmed.ncbi.nlm.nih.gov/41187231/

#### Methods

I used published data from Ghannoum et al. (2025) to examine changes in C. acnes detection and clindamycin resistance during treatment with clindamycin, adapalene, and benzoyl peroxide.

Using Python, Pandas, and Matplotlib, I:
- Organized bacterial detection and resistance data from 45 participants who completed the study.
- Compared C. acnes detection and susceptibility at baseline and Week 24.
- Examined how participants' bacterial detection and resistance status changed over time.
- Analyzed acne lesion improvement at Week 12 among participants with resistant bacteria.
- Calculated the percentage of resistant cases among participants with detectable C. acnes.
- Created five graphs to visualize the results.

This was a descriptive analysis of published data from two pooled, open-label studies without a control group.

#### Key Findings

Bacterial detection: The percentage of participants with detectable C. acnes decreased from 82.2% (37/45) at baseline to 44.4% (20/45) at Week 24.

Antibiotic resistance: The number of participants with clindamycin-resistant C. acnes remained at 5. No participants without detectable resistance at baseline had resistant bacteria detected at Week 24.

Acne improvement: All 5 participants with resistant bacteria at baseline showed reductions in acne lesions at Week 12.

Resistance percentage: Among participants with detectable C. acnes, the percentage with resistant bacteria increased from 13.5% to 25.0%. This increase occurred because fewer participants had detectable C. acnes overall, while the number with resistant bacteria stayed the same.

These findings show that a decrease in bacterial detection does not necessarily mean a decrease in antibiotic resistance. However, because the original studies had no control group, the results cannot prove that combination treatment prevents resistance.

#### Project Files: [Analysis_4_Ghannoum_2025](https://github.com/cjjde05/acne-antibiotic-resistance-analysis/tree/main/Analysis_4_Ghannoum_2025)


## Tools and Skills
- Python: Data analysis and reproducible workflows
- Pandas: Data organization and descriptive calculations
- Matplotlib: Data visualization
- Google Colab: Notebook development and execution
- GitHub: Project organization and documentation

## Limitations

This project uses published data rather than original patient-level data. All four analyses are descriptive and cannot establish cause-and-effect relationships.

- **Analysis 1:** Results come from one clinical trial and may not apply to all patients.
- **Analysis 2:** Studies used different methods and sample sizes, making direct comparisons difficult. The calculated percentages are not pooled meta-analysis estimates.
- **Analysis 3:** The dataset includes only selected resistant isolates, including some bacteria other than *C. acnes*.
- **Analysis 4:** The study had no control group, so it cannot show whether combination treatment prevents antibiotic resistance.

## Future Directions

Future research could compare long-term antibiotic and non-antibiotic acne treatments, examine how resistance develops over time, and explore ways to improve acne while reducing antibiotic resistance.

## Author

Claire Jeong  
University of Illinois Urbana-Champaign  
Major: Molecular and Cellular Biology  
Minor: Data Science
