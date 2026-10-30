# Antibiotic Resistance in Cutibacterium acnes: A Python-Based Analysis
Project Overview

This project explores antibiotic resistance in Cutibacterium acnes, a bacterium associated with acne vulgaris, and examines whether combining topical clindamycin with benzoyl peroxide (BPO) may improve treatment outcomes.

Using published clinical trial data, I performed a descriptive secondary data analysis with Python to visualize changes in antibiotic-resistant bacterial counts and acne lesion reduction over a 16-week treatment period.

Research Questions

How does topical antibiotic treatment relate to antibiotic resistance in C. acnes?

How do resistant bacterial counts change over time during treatment?

How does clindamycin combined with benzoyl peroxide compare with clindamycin alone?

Data Source

Cunliffe et al. (2002). A randomized, double-blind comparison of a clindamycin phosphate/benzoyl peroxide gel formulation and a matching clindamycin gel with respect to microbiologic activity and clinical efficacy in the topical treatment of acne vulgaris.

Original publication

Data were manually extracted from Tables III and V of the published study.

Methods

Organized published clinical trial summary data using Python and Pandas.

Visualized treatment outcomes over 4, 8, 12, and 16 weeks using Matplotlib.

Compared mean log10 changes in clindamycin-resistant C. acnes counts.

Compared median percentage changes in total acne lesion counts.

Calculated descriptive differences between treatment groups.

Results

1. Antibiotic Resistance



At week 16, the mean log10 change in clindamycin-resistant C. acnes counts was -0.2 in the combination therapy group and +1.2 in the clindamycin-only group. The original study reported a statistically significant between-group difference (p = 0.018).

2. Clinical Efficacy



At week 16, the median reduction in total acne lesion counts was 52.7% for combination therapy and 27.5% for clindamycin alone, representing a 25.2-percentage-point difference in reduction.

Tools Used

Python

Pandas

Matplotlib

Google Colab

GitHub

Limitations

This project uses published aggregate data rather than individual patient-level observations. It is a descriptive secondary analysis, not an independent clinical trial or a new statistical evaluation. Findings from this single study should not be generalized to all acne patients.

Future Directions

I plan to expand this project by reviewing additional studies on antibiotic resistance mechanisms, antibiotic exposure, and non-antibiotic acne treatment strategies.

Author

Undergraduate student studying Molecular and Cellular Biology with a minor in Data Science at the University of Illinois Urbana-Champaign.
