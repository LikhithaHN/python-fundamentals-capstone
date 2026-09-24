# Python Fundamentals Capstone — Employee & Project Analysis

A data-wrangling exercise in **Pandas** and **NumPy** that builds three related datasets (employees, seniority, projects), cleans them, merges them, and applies business rules for bonuses, promotions, and demotions.

   📓 **Notebook:** [capstoneproject.ipynb](https://github.com/LikhithaHN/python-fundamentals-capstone/blob/main/capstoneproject.ipynb)
## Datasets

| DataFrame | Rows | Columns |
|---|---|---|
| `employee` | 5 | ID, Name, Gender, City, Age |
| `seniority` | 5 | ID, Designation Level (1 = highest, 4 = lowest) |
| `project` | 14 | ID, Project, Cost, Status (Finished / Ongoing / Failed) |

## Tasks

| # | Task | Techniques |
|---|---|---|
| 1 | Build DataFrames and save as CSV | `pd.DataFrame`, `to_csv` |
| 2 | Fill missing project costs with the running average of known costs | loop, `pd.isna`, `.loc` |
| 3 | Split `Name` into First / Last Name | `.str.split`, `drop` |
| 4 | Merge all three tables into `Final` | `pd.merge` (left join) |
| 5 | 5% bonus on finished projects | `apply` + `lambda` |
| 6 | Demote employees on failed projects; drop levels above 4 | boolean indexing |
| 7 | Add Mr./Mrs. prefix by gender | `apply`, conditional string logic |
| 8 | Promote employees older than 29 | `apply` + `lambda` |
| 9 | Total project cost per employee | `groupby`, `sum`, `rename` |
| 10 | Employees whose city contains "o" | `.str.contains(case=False)` |

## Key Results

- **Missing costs imputed:** Project 5 → 3,250,500 and Project 9 → 2,061,714 (running average)
- **Total bonus payout:** 632,625 across 7 finished projects
- **Highest total project cost:** Nina (A004) at 9,500,000
- **Promoted by age (> 29):** Nina and Amy
- **Cities containing "o":** London, Newyork

## Tech Stack

Python 3 · Pandas · NumPy · Jupyter Notebook (Anaconda)


*Part of the Skillovilla Data Analytics + Generative AI program.*
