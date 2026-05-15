# 🏏 IPL Crunch '26 — Data Analytics Submission

> *17 seasons. 1,090 matches. 260,920 balls. 5 questions. 1 unexpected truth.*

A data-analytics deep-dive into the Indian Premier League, built as my submission for the **IPL Crunch '26** challenge by Wooble × Unstop.

This project goes beyond the usual "top 10 batters" charts. It uses real ball-by-ball data to answer the questions every IPL fan argues about — and surfaces one finding that genuinely surprised me.

---

## 🎯 The Five Questions

| # | Question | Answer (one-liner) |
|---|----------|--------------------|
| Q1 | Does winning the toss = winning the match? | **No.** Toss winners win just 50.8% — barely better than chance. |
| Q2 | Which phase decides the match? | **Death overs.** Winners outscore losers by 1.87 RPO here. |
| Q3 | Who are the all-time top performers? | **Kohli (8,014 runs)** and **Chahal (205 wickets)** lead — but Narine and Bumrah quietly dominate efficiency. |
| Q4 | Has the 2023 Impact Player rule changed scoring? | **Massively.** Average totals jumped 14.4% (163 → 187). 180 is no longer a winning total. |
| Q5 | How much do powerplay wickets really hurt? | **A lot.** Losing 3+ wickets in PP drops your win rate from 68% to 25% — a 44-point swing. |

---

## 🌟 The One Insight That Surprised Me

> **The toss is worth ~1.6 percentage points. Surviving the powerplay is worth ~44. Cricket commentary obsesses over the wrong thing.**

The toss is treated like the most important moment of an IPL match. The data says it's almost a coin flip. The *real* match-decider — fifteen times more impactful than the toss — is whether you can navigate the first six overs without losing wickets.

---

## 📂 Repo Structure

```
ipl-crunch-26/
├── README.md                          ← you are here
├── notebooks/
│   ├── 01_setup_and_toss_analysis.ipynb   ← Day 1-2: data load + Q1
│   └── 02_full_analysis_Q2_to_Q5.ipynb    ← Day 3-12: Q2-Q5 + bonus + summary
├── charts/                             ← all 9 visualizations (PNG)
│   ├── chart_01_toss_myth.png
│   ├── chart_02_phase_impact.png
│   ├── chart_03_top_batters.png
│   ├── chart_04_top_bowlers.png
│   ├── chart_05_death_bowlers.png
│   ├── chart_06_score_evolution.png
│   ├── chart_07_180_myth.png
│   ├── chart_08_pp_wickets.png
│   └── chart_09_clutch_hitters.png
├── deck/
│   └── IPL_Crunch_26_Deck.pptx        ← submission deck (15 slides)
└── data/
    └── README.md                       ← where to get matches.csv + deliveries.csv
```

---

## 🛠️ How to Reproduce

1. **Get the data.** Download the IPL Complete Dataset (2008-2024) from Kaggle. You need `matches.csv` and `deliveries.csv`.
2. **Open in Colab.** Upload either notebook to [Google Colab](https://colab.research.google.com).
3. **Upload the CSVs** to your Colab session (drag-drop into the file sidebar).
4. **Run all cells** (Runtime → Run all). All 9 charts will be regenerated.

Total runtime: ~2 minutes on a free Colab CPU runtime.

---

## ⚙️ Tech Stack

- **Python 3.10**
- **Pandas / NumPy** — data cleaning and aggregation
- **Matplotlib / Seaborn** — visualization
- **Google Colab / Jupyter** — execution environment

No proprietary tools. No external APIs. Fully reproducible from the two CSV files.

---

## 📊 Headline Numbers

| Metric | Value |
|--------|-------|
| IPL seasons analyzed | 17 (2007 → 2024) |
| Matches analyzed | 1,090 |
| Ball-by-ball deliveries | 260,920 |
| Visualizations produced | 9 |
| Unique batters | 600+ |
| Unique bowlers | 500+ |

---

## 🧠 Methodology Notes

- **Team-name standardization** applied (e.g., Delhi Daredevils → Delhi Capitals, Royal Challengers Bangalore → Royal Challengers Bengaluru) so cross-season comparisons are valid.
- **Bowler-credit accounting** excludes run-outs and retired-hurt dismissals; byes/leg-byes are stripped from bowler economy.
- **Phase definitions** follow IPL convention: Powerplay = overs 1-6, Middle = 7-15, Death = 16-20.
- **Strike-rate denominators** exclude wides (which are not "balls faced" by the batter).

---

## 🙌 Acknowledgements

- **Cricsheet** — for maintaining the open ball-by-ball IPL dataset.
- **Wooble** — for hosting a challenge that values proof of work over resume bullets.
- **The IPL** — for 17 seasons of beautiful, chaotic data.

---

## 👤 Author

**Rohit Kumar** — `rohitkumar.ak51@gmail.com`

Built for **IPL Crunch '26** · May 2026.

If this work interests you and you want to discuss the analysis further, my contact is on the deck's closing slide.
