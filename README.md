# US Tariffs & Their impact 

---

## Why

### Motivation
Trade policies like tariffs affect stock prices, import volumes, produces prices, public sentiment, etc. 

This project aims to explore those effects using open data and ML 


---

## How

### Env
```bash
conda env create -f environment.yml
conda activate tariff-env
```

### Data sources
- X: tariff events (annoucements dates, sectors affected, rate)
  - Federal Registry - tariff events & announcements
  - [Presidential Actions](https://www.whitehouse.gov/presidential-actions)
  - HTS Archive (USITC) - ?
- y: market or economic response (sector stock prices, import volumes, PPI, sentiment indices)
  - Yahoo Finance - sector ETF prices
  - ? - PPI
  - ? - import volumes
  - GDELT - news sentiment (https://github.com/alex9smith/gdelt-doc-api)

### Pipeline
1. Fetch
2. Clean and extract features
3. EDA
4. Merge
5. Model

### Notebooks
- 01_fetch_fedregister.ipynb - download raw tariff data
- 02_clean_fedregister.ipynb - deduplicate, clean, extract features

## Future ideas
- [Tariff Announcements, News Sentiment, and S&P 500 Returns: A High-Frequency, Multi-Model Event Study](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5224176)
- https://www.sciencedirect.com/science/article/abs/pii/S1478409224000037
- [HTS Archive](https://www.usitc.gov/harmonized_tariff_information/hts/archive/list)

---