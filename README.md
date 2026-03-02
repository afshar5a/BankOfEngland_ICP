# Bank of England Individual Capstone Project  
## Sentiment in Central Bank Speeches and UK Economic Conditions

**Student:** Afshar Sanam
**University:** London School of Economics and Political Sciences  
**Programme:** Post Graduation in Data Analytics  
**Academic Supervisor:** James Abdey  

---

## Approved Research Question

**How does sentiment in Bank of England speeches evolve over time, and how does it relate descriptively to key UK macroeconomic indicators and market conditions, such as the FTSE 250 index, during both benign and turbulent economic periods?**

This project is intentionally **exploratory and descriptive**. Predictive modelling and causal inference are explicitly out of scope, in line with supervisor guidance.

---

## Research Design & Scope

- Exploratory, descriptive analysis  
- Primary sentiment method: **LSE sentiment-labelled wordlist**  
- Narrative and visual storytelling emphasis  
- Correlation interpreted descriptively  

---

## Data Sources

- Bank of England speech corpus  
- LSE sentiment-labelled wordlist  
- UK macroeconomic indicators (**CPI / CPIH**)  
- Market indicators: **FTSE 250 (primary)**, **FTSE 100 (secondary)**  

---

## Methodology Overview

Dictionary-based sentiment scoring aggregated monthly/quarterly, followed by time-series visualisation and descriptive correlation analysis. No predictive modelling or causal inference.

---

## Economic Regime Framing

- **Benign periods:** stable inflation, steady growth  
- **Turbulent periods:** Brexit, Covid-19, inflation surge  

---

## Notebook

- `BankOfEngland_LSE_Project.ipynb` — end-to-end workflow:
  - Data loading and filtering (UK speeches)
  - Text cleaning and tokenisation
  - Lexicon-based sentiment scoring (primary method)
  - Optional comparison sentiment scoring (VADER, TextBlob)
  - Monthly aggregation and alignment with FTSE and CPIH series
  - Visual analysis and rolling correlations
  - Export of datasets, figures, and report-assembly helper files

---

## Key Outputs

The notebook generates intermediate datasets, analysis tables, and figures used for reporting and interpretation.

### Data exports (CSV)
- `speeches_uk_scored.csv`
- `speech_sentiment_monthly_aggregation.csv`
- `merged_monthly_speech_sentiment_ftse_macro.csv`
- `rolling_corr_sentiment_ftse250.csv`
- `rolling_corr_comparison_ftse250_ftse100.csv`
- `ftse100_ftse250_normalized.csv`
- `regime_summary.csv`
- `regime_summary_table.csv`
- `corr_summary.csv`
- `figure_registry.csv`
- `table_registry.csv`

### Figures (PNG)
- `fig_sentiment_vs_ftse250_shaded.png`
- `fig_rollcorr_sentiment_ftse250.png`
- `fig_ftse100_vs_ftse250_levels.png`
- `fig_ftse100_vs_ftse250_normalized.png`
- `fig_cpih_vs_sentiment.png`
- `fig_11_sentiment_vs_ftse250_shaded.png`
- `fig_11_rolling_corr_sentiment_ftse250.png`
- `fig_12_ftse100_vs_ftse250_normalized.png`
- `fig_12_rolling_corr_comparison_ftse250_ftse100.png`

### Report assembly helpers
- `latex_snippets.tex`
- `ICP_tables_pack.xlsx`

---

## Implications, Takeaways, and Interpretation

### Implications of the Findings
Based on the descriptive analysis, several implications emerge:

- Bank of England speech sentiment appears to **co-move with domestic market conditions**, particularly during periods of heightened economic uncertainty.
- The **FTSE 250** (more domestically oriented) shows **stronger alignment** with speech sentiment than the **FTSE 100**, which is more internationally exposed.
- During “exciting” periods (e.g. Brexit, COVID, inflation surges), both sentiment volatility and market volatility increase, suggesting that **central bank communication tone becomes more responsive during stress episodes.**
- These patterns are **indicative rather than causal**, and should be interpreted as descriptive associations.

### Relevance for Market Participants
This analysis may be of interest to:

- **Market participants**, who monitor central bank communication as part of broader macro-financial assessment.
- **Policy analysts**, interested in how communication tone changes across economic regimes.
- **Researchers**, studying the interaction between narrative economics, market sentiment, and macro conditions.

Speech sentiment may provide **contextual signals**, rather than predictive signals, for market conditions.

### Key Takeaways
- Central bank communication tone is **not constant** and varies meaningfully across time and regimes.
- Domestic equity indices (FTSE 250) appear more sensitive to sentiment dynamics than global indices (FTSE 100).
- Inflationary environments coincide with **more pronounced sentiment shifts**, reflecting policy uncertainty and communication challenges.
- Correlation patterns **change across regimes**, reinforcing the importance of contextual interpretation.

---

## Limitations

While this study provides descriptive insights into the relationship between Bank of England (BoE) speech sentiment, market indicators, and inflation dynamics, several limitations should be acknowledged.

### 15.1 Descriptive Nature and Absence of Causal Inference
The analysis is explicitly exploratory and descriptive in nature. Although correlations and co-movements between BoE speech sentiment, FTSE indices, and inflation measures are examined, these relationships should **not be interpreted as causal**. Observed associations may reflect contemporaneous responses to shared economic conditions rather than any direct influence of central bank communication on markets or inflation outcomes.

### 15.2 Sentiment Measurement Constraints
Sentiment scores are derived using a lexicon-based approach applied to central bank speeches. While this method offers transparency and interpretability, it has inherent limitations. Lexicon-based sentiment analysis may fail to fully capture contextual nuance, irony, or the strategic ambiguity often present in central bank communication. Additionally, sentiment scores are sensitive to vocabulary choices and may underweight the importance of tone conveyed through structure, emphasis, or delivery rather than word frequency alone.

### 15.3 Aggregation and Temporal Alignment
Speech sentiment and macroeconomic indicators are aggregated to a monthly frequency to enable comparability. This aggregation may obscure short-term dynamics or intra-month reactions, particularly around major policy announcements or market shocks. Timing differences between speeches and market movements can also introduce misalignment.

### 15.4 Choice of Market and Inflation Indicators
The FTSE 250 is used as a proxy for domestically oriented market conditions, supplemented by comparison with the FTSE 100. These indices do not capture the full complexity of financial markets or investor expectations. Inflation is represented using the CPIH annual rate, which reflects backward-looking price changes and may not fully capture forward-looking inflation expectations that influence communication strategies.

### 15.5 Sample and Structural Breaks
The study spans multiple structural regimes, including the global financial crisis, Brexit, the COVID-19 pandemic, and recent inflation surges. Structural breaks and regime shifts may affect the stability of observed relationships over time, limiting uniform conclusions across periods.

### 15.6 External Validity
Findings are specific to the UK context and the Bank of England. Communication styles, mandates, and market structures vary internationally, limiting generalisability to other central banks or economies.

---

## Ethical & Responsible Analytics

Academic use only. Results are presented with transparency and caveats.

---

## Future Research

Extensions suggested by the notebook include predictive modelling, event studies, and more advanced NLP methods.

---

## Conclusions

Speech sentiment evolves over time and aligns descriptively with macroeconomic and market conditions across economic regimes.
