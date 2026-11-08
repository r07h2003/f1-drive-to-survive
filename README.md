# F1 × Drive to Survive

**Did a Netflix docuseries change who watches Formula 1 in the U.S.? A data analysis of 2017–2024.**

**[View the interactive analysis →](https://r07h2003.github.io/f1-drive-to-survive/)**

Group project for the Rutgers MS in Marketing Analytics. I led the group and built the data pipeline, regression model, sentiment analysis and visualizations.

---

## Key findings

| | Finding | Basis |
|---|---|---|
| **+312K** | U.S. viewers per race in the Drive to Survive era, after controlling for COVID, organic growth and search interest | OLS regression · p < 0.01 · R² = 0.66 |
| **10% → 25%** | Female share of F1 fans, 2017 to 2024, the strongest trend in the dataset | F1 Global Survey · r = 0.98 |
| **2.2×** | ESPN average viewers per race, 554K (2018) to 1,210K (2022) | ESPN Press Room |
| **+0.41 / −0.14** | Reddit sentiment rose overall while traditional fans' sentiment fell | VADER on r/formula1 |

## Method

- **Data:** 96 monthly observations (Jan 2017 – Dec 2024) combining ESPN/ABC and Nielsen viewership, F1 Global Survey demographics, a U.S. search-interest index, Instagram follower counts and r/formula1 posts.
- **OLS regression** of race viewership on a DTS-era flag, a post-Season-4 flag, a year trend, a COVID flag and search interest.
- **Pearson correlation** between search interest, social following, demographics and viewership.
- **VADER sentiment analysis** on r/formula1, splitting traditional and new fans using account age and flair as proxies.

## Limitations

- The data is observational. The model shows a significant association with Drive to Survive, not proof that the show caused the growth.
- The search-interest index is a calibrated estimate built from ESPN/Nielsen anchors and published spikes, not a raw Google Trends export.
- Survey-based and Nielsen-based demographic figures use different bases and aren't directly comparable.
- 2017 races aired on NBC Sports, so 2017 viewership isn't comparable with ESPN years.

## How it was built

Python (pandas, statsmodels, NLTK/VADER). Code was written with AI assistance and run by me. The analytical decisions were mine: which controls to include, how to read the regression output and what the sentiment divergence meant.

The page is a single self-contained `index.html` served with GitHub Pages.

---

[Portfolio](https://r07h2003.github.io) · [LinkedIn](https://linkedin.com/in/rohan-harishchandrakar)
