# FDE course notebooks

The Google Colab notebooks for the free course *Forward Deployed AI/ML Engineer*. Most of the course's code runs in your browser, on the lesson page. A few libraries cannot run there, so their parts of a day live here as notebooks.

| Day | Notebook | What it does |
| --- | --- | --- |
| Week 3, Day 2 | [`notebooks/week-3/day-2-catboost.ipynb`](notebooks/week-3/day-2-catboost.ipynb) | Fits CatBoost on the logistics client's late deliveries, with category columns as plain text, and puts it on the day's scorecard. About 25 minutes. |
| Week 3, Day 4 | [`notebooks/week-3/day-4-umap.ipynb`](notebooks/week-3/day-4-umap.ipynb) | Draws the digits and the client's accounts in two dimensions with UMAP, beside t-SNE and PCA, and places new rows on a picture already drawn. About 15 minutes. |

## Open it in Colab

[Open Week 3 Day 2 in Colab](https://colab.research.google.com/github/talhaturab/fde-course-notebooks/blob/main/notebooks/week-3/day-2-catboost.ipynb)

[Open Week 3 Day 4 in Colab](https://colab.research.google.com/github/talhaturab/fde-course-notebooks/blob/main/notebooks/week-3/day-4-umap.ipynb)

Colab needs a Google account. Once it opens, press **Runtime → Run all**. The first cell installs the library the notebook needs, and the notebook reads its data from this repository, so there is nothing to upload.

## Read it without a Google account

Click the notebook in the table above. GitHub shows it with every output from the saved run already printed, so you can follow the whole thing without running anything.

## Run it on your own computer

You need Python 3 and these packages.

```bash
git clone https://github.com/talhaturab/fde-course-notebooks.git
cd fde-course-notebooks
python -m venv .venv
source .venv/bin/activate        # on Windows: .venv\Scripts\activate
pip install catboost==1.2.10 pandas scikit-learn jupyter
jupyter notebook notebooks/week-3/day-2-catboost.ipynb
```

For Week 3 Day 4, install `umap-learn==0.6.0 matplotlib` in place of CatBoost and open `notebooks/week-3/day-4-umap.ipynb`.

Each notebook reads its data from GitHub by default. To use the copies in `data/` instead (for example, offline), set `DATA_DIR` before starting Jupyter:

```bash
DATA_DIR=../../data jupyter notebook notebooks/week-3/day-2-catboost.ipynb
```

The path is relative to the notebook's own folder.

## The data

`data/shipments_history.csv` (21,511 delivered shipments, January 2024 to September 2026) and `data/customers_history.csv` (240 accounts) belong to the course's fictional logistics client. The client, its accounts, names and shipments are all made up for the course. No real company, person or shipment is described.
