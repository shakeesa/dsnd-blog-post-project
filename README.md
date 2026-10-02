# 2024 Stack Overflow Developer Compensation

This project uses six reported work and career characteristics to estimate whether an eligible 2024 Stack Overflow Developer Survey respondent reported annual compensation above the training sample's worldwide median.

## Motivation

A single worldwide dollar cutoff is easy to explain, but it can hide large geographic differences. This project builds one transparent prediction model, compares it with a naive baseline, and explains both its useful patterns and its limits. It follows the CRISP-DM sequence: business understanding, data understanding, preparation, modeling, evaluation, and communication.

## Business questions

1. Which reported characteristics does the model rely on most, what do they mean, and how do they move its estimate?
2. Does “above the global training cutoff” mean the same thing in countries with the most compensation responses?
3. How accurately can the model identify unseen respondents above the cutoff, and how much better is it than a naive baseline?
4. What does the model predict for two fictional profiles that differ only in professional coding experience?

## Dataset

The project uses Stack Overflow's official [2024 Developer Survey](https://survey.stackoverflow.co/2024/), [methodology](https://survey.stackoverflow.co/2024/methodology), [work and compensation report](https://survey.stackoverflow.co/2024/work), and [data archive](https://github.com/StackExchange/Survey/tree/main/packages/archive/2024). The source files were retrieved on September 28, 2026.

The repository includes `data/results_project.csv.gz`, a compressed extract of all 65,437 response rows containing the identifier, outcome, and six predictors used in this analysis. It also includes the official `data/schema.csv`. These files make the notebook executable immediately after cloning. The complete official [`results.csv`](https://github.com/StackExchange/Survey/blob/main/packages/archive/2024/results.csv) is about 152 MB and is intentionally excluded from this repository.

One row represents one retained survey response. Modeling uses the 23,435 rows with numeric, finite, positive `ConvertedCompYearly` values. Stack Overflow licenses the database under the [Open Database License 1.0 and Database Contents License 1.0](https://github.com/StackExchange/Survey#license-and-data-attribution).

## Libraries used

The verified environment used Python 3.9.6 with these direct dependencies:

- Jupyter 1.1.1
- pandas 2.2.3
- NumPy 2.0.2
- scikit-learn 1.6.1
- Matplotlib 3.9.4
- seaborn 0.13.2

Exact versions are pinned in `requirements.txt`.

## Repository files

| Path | Purpose |
|---|---|
| `.gitignore` | Keeps raw data, environments, caches, and temporary notebook outputs out of Git. |
| `README.md` | Explains the project, setup, results, and limitations. |
| `instructions.md` | Preserves the supplied project brief and rubric. |
| `requirements.txt` | Pins the six direct Python dependencies. |
| `stackoverflow_salary_analysis.ipynb` | Contains the complete documented CRISP-DM analysis. |
| `blog_post.md` | Presents the findings for a general audience. |
| `index.html` | Publishes the standalone blog through GitHub Pages. |
| `data/results_project.csv.gz` | Contains all survey rows and the eight fields required by the analysis. |
| `data/schema.csv` | Contains the official 2024 survey field definitions. |
| `images/country_median_comparison.png` | Compares training compensation medians for the ten largest country samples. |
| `images/feature_importance.png` | Shows held-out permutation importance for all six source fields. |
| `images/confusion_matrix.png` | Shows the four held-out logistic-regression outcomes. |

The optional full `data/results.csv` download remains ignored because it is not needed to reproduce the committed analysis.

## How to reproduce the analysis

From the repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter notebook stackoverflow_salary_analysis.ipynb
```

To verify a complete non-interactive run:

```bash
jupyter nbconvert \
  --to notebook \
  --execute stackoverflow_salary_analysis.ipynb \
  --output stackoverflow_salary_analysis.executed.ipynb \
  --output-dir /tmp \
  --ExecutePreprocessor.timeout=600
```

The notebook checks file presence, rejects Git LFS pointers, validates required fields and identifiers, and uses only relative project paths. It regenerates the three committed figures under `images/`. No separate data download is required.

## Summary of results

- **Important predictors:** Country of residence ranked first: shuffling it reduced held-out ROC-AUC by 0.2647 on average. Professional coding experience ranked second with a 0.0579 decrease. These are predictive associations, not causes.
- **Geographic insight:** The worldwide training cutoff was $65,000. Among 3,527 held-out respondents in supported countries, 27.4% changed above/below labels when each country's exact training median replaced the global cutoff.
- **Model performance:** On 4,687 held-out rows, logistic regression achieved 82.0% accuracy, 79.8% recall, 81.6% F1, and 0.897 ROC-AUC. Baseline accuracy was 49.9% and baseline ROC-AUC was 0.500.
- **Fictional scenario:** With the other five fields fixed, the 4-year and 14-year profiles received 92.3% and 97.0% above-cutoff probabilities. Both remained in the above-cutoff class; the 4.8 percentage-point difference is illustrative, not causal.

The cutoff is the eligible training sample's worldwide median reported compensation. It is not an industry median or a definition of career success.

## Limitations

The survey is voluntary and was recruited mainly through Stack Overflow channels. Compensation is self-reported total annual pay before tax, including salary, bonuses, and perks. Respondents who disclosed compensation may differ from those who did not. Converted U.S. dollars do not account for purchasing power, taxes, inflation, or local living costs. The model omits many relevant factors, and one survey year cannot show how an individual's career changes. Results apply to eligible survey respondents and do not establish cause.

## Blog post

Read the published blog, [Above the Median—But Whose Median? Four Lessons from Stack Overflow's 2024 Developer Survey](https://shakeesa.github.io/dsnd-blog-post-project/), view its [Markdown source](blog_post.md), or inspect the full [executed analysis notebook](stackoverflow_salary_analysis.ipynb).

## Acknowledgments

Stack Overflow created and published the 2024 Developer Survey, schema, methodology, and aggregate findings. All figures are the author's analysis of the official 2024 survey data. The project structure and deliverables follow the supplied Udacity data science blog post brief in `instructions.md`.
