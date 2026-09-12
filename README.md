# Fatigue Life Reliability Modeling

> 🏆 **Finalist — NSTC College Student Research Creativity Award (2025)**
> 國科會大專學生研究計畫研究創作獎 入圍(2025)

Statistical modeling of the fatigue life of metallic materials using **accelerated life testing (ALT)** data. This project builds and compares parametric lifetime models, estimates parameters by **maximum likelihood estimation (MLE)**, and selects models in a data-driven way using information criteria and likelihood-based tests.

> 本研究以加速壽命試驗 (ALT) 資料,對金屬材料的疲勞壽命進行統計建模,並以資料導向的方式選擇最適模型。

---

## Overview

In corrosion-fatigue reliability research, lifetime data are commonly fitted with **Weibull** or **log-normal** distributions. However, the model chosen by AIC alone is not always Weibull. This project:

- Constructs fatigue-life models under both **Weibull** and **log-normal** distributions.
- Estimates model parameters — including the **Basquin S–N relationship** and a **fatigue limit** — by **maximum likelihood estimation (MLE)**.
- Builds families of lifetime models by allowing the **scale parameter** to vary across stress levels.
- Selects and compares models using the **likelihood ratio test (LRT)** and **AIC**.
- Compares fitted **p-quantile** lifetime estimates across models to visualize where the models diverge.
- Proposes a **standardized analysis workflow** that lets researchers select an appropriate lifetime model quickly, accurately, and conservatively.

## Methods

| Component | Approach |
|---|---|
| Lifetime distributions | Weibull, log-normal |
| S–N relationship | Basquin equation (with / without fatigue limit) |
| Parameter estimation | Maximum likelihood estimation (MLE) |
| Model selection | Likelihood ratio test (LRT), AIC |
| Output | p-quantile lifetime estimates & confidence intervals |

## Data

Fatigue test datasets for several materials (stress vs. cycles-to-failure):

- `copper_fatigue_data.csv` — annealed electrolytic copper wire
- `aluminum_fatigue_data.csv` — aluminum
- `Superalloy.csv` — superalloy
- `248.csv`, `248_adjusted.csv`, `758.csv` — additional experimental datasets
- `fatigue_demo_data.csv`, `fatigue_demo_data_no_outlier.csv` — demonstration data

## Analysis Code

R Markdown notebooks containing the full modeling pipeline:

- `Model_summary.Rmd` — main model summary and comparison
- `Model_summary_random_effect_ver2.Rmd` — extended version with random effects
- `basquin_model_with_without_fatigue_limit.Rmd` — Basquin models with and without a fatigue limit
- `each_stress_modeling.Rmd` — per-stress-level modeling

## Report

- `abstract.pdf` / `abstract.docx` — project abstract and full write-up (Traditional Chinese)

## Tech Stack

- **R** / **R Markdown**
- Reliability & survival modeling, MLE, information-criteria-based model selection

---

*大專生研究計畫 (Undergraduate Research Project) · Department of Statistics & Institute of Data Science.*

## How to Reproduce

Open any `.Rmd` file in RStudio and knit it, or run the chunks interactively. All datasets are in the repository root.
