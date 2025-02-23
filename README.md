# Trendsetters-Across-Borders-Decoding-YouTube-s-Viral-Landscape-2024
This repository analyzes cultural and social patterns in trending YouTube videos through emoji usage, title length vs. HDI, and category popularity across countries.

# Data
1. This study is based on daily snapshots of [YouTube trending videos](https://www.kaggle.com/datasets/asaniczka/trending-youtube-videos-113-countries) from 113 countries for the year 2024.
2. The dataset was enriched with [Human Development Index](https://en.wikipedia.org/wiki/Human_Development_Index) (HDI) data from 2022.

( Live streams and “shorts” were excluded to maintain consistency and limit API anomalies. During preprocessing, missing values and outliers were addressed, global duplicate videos were removed, and only one trending video per channel was retained. Countries with fewer than 500 observations were also filtered out.)

Additional comments and links to dataset are available in "./dat".
NOTE: Since we run our code on cloug platforms there may be need to change paths to datasets in notebooks, but we cared about it as well. The ploblems may also occur due to UNIX / Windows OS differences in path specifications.

# Assumptions
1. The analyses assume that daily trending videos in each country reflect culturally relevant viewing patterns, thus serving as a window into audience preferences.
2. Independence of observations is largely ensured by excluding globally trending content and limiting multiple appearances from the same channel.
3. HDI data from 2022 is considered sufficiently reliable for 2024, under the assumption of minimal changes in two years.
4. Across all tests, a significance level of α = 0.05 was used, with multiple comparison corrections (Benjamini–Yekutieli and Bonferroni) to control for inflated error rates.

# Hypotheses tested
1. The research tests whether Middle Eastern countries consistently use more emojis in trending video titles than Euro-Atlantic nations, employing Welch’s t-tests with a Benjamini–Yekutieli correction for multiple country-pair comparisons.
2. A potential monotonic relationship between national HDI and average title length is investigated, using non-parametric correlation coefficients (Spearman’s ρ and Kendall’s τ).
3. The prevalence of various YouTube categories (People & Blogs, Comedy, Sports) is compared across countries via z-tests of proportions, applying Bonferroni correction for multiple comparisons.

# Results
1. In examining emoji usage, the data show that many Middle Eastern countries feature two to three times more emojis per title than Euro-Atlantic countries, with statistically significant results for around 80% of the pairwise comparisons. Nonetheless, there are exceptions—such as Czech Republic vs. Qatar or Bahrain—indicating unique patterns in some nations.
2. Both Spearman’s and Kendall’s correlation tests reveal a small but statistically significant negative association, suggesting that countries with higher HDI may favor more concise video titles.
3. Cross-country comparisons of category distributions highlight notable differences in viewer preferences—Hong Kong’s trending videos often center on People & Blogs, whereas Russia displays a marked preference for Comedy. Proportion z-tests confirm that these distinctions in category prevalence are statistically significant.
