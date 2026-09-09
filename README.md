# Introductory R for Social Sciences

Course materials — website and slides — for the **Introductory R for Social Sciences** workshop run by [SMU Libraries](https://library.smu.edu.sg/) in collaboration with [School of Social Sciences](https://socsc.smu.edu.sg/) for undergraduate students at [Singapore Management University](https://www.smu.edu.sg/).

🌐 **Live site:** <https://smu-libraries.github.io/r-socsci/>

The workshop is a hands-on, five-session introduction to coding and statistical analysis in R, aimed at students with some foundational statistics knowledge who are new to R (or to programming in general). Rather than treating R as a set of recipes to memorise, the sessions emphasise building a **mental model** — reading your variables, choosing the right approach, checking whether a result can be trusted, and interpreting and reporting it honestly.

## The sessions

| # | Topic | What it covers |
|---|-------|----------------|
| 1 | Introduction to R and RStudio | Setting up RStudio, basic data types and structures, importing data |
| 2 | Data wrangling with tidyverse | Filtering, selecting, mutating, and grouping data with `dplyr` |
| 3 | Data visualization & descriptive statistics | Building plots with `ggplot2`; means, medians, spread |
| 4 | Basic inferential tests | Chi-square, correlation, t-tests, and ANOVA — plus checking assumptions |
| 5 | Regression & presenting your results | Linear and logistic regression; reporting and result tables |

Each session's slides are a [Quarto](https://quarto.org/) Reveal.js deck (`0X-*.qmd`). The website's home page (`index.qmd`) holds the schedule and pre-workshop setup instructions.

## The dataset

All examples use a teaching extract of the [World Values Survey](https://www.worldvaluessurvey.org/) (Wave 7), covering four countries — **Hong Kong SAR, Indonesia, Malaysia, and Turkey** — with 15 selected variables. The raw file lives at [`data/wvs-4-countries.csv`](data/wvs-4-countries.csv); a cleaned version produced during the workshop is in [`data-output/`](data-output/). See [`dataset.qmd`](dataset.qmd) for the full data dictionary and source citation.

Note that we may change the dataset from time to time, e.g. changing the country data used, or the variables used in the dataset. 

## Building locally

You'll need [R](https://cran.r-project.org/) and [Quarto](https://quarto.org/docs/get-started/) installed, plus the R packages used across the sessions:

```r
install.packages(c(
  "tidyverse", "DescTools", "moments", "corrplot",
  "apaTables", "gtsummary", "car", "huxtable"
))
```

Then, from the project root:

```bash
quarto preview   # live preview in your browser
quarto render    # build the full site into _site/
```


## License

The materials are released under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) — see [`LICENSE`](LICENSE). You're welcome to reuse and adapt them, with attribution and under the same license.
