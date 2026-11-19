# Predicting Post-Fire Permafrost Thaw Depth with ML (COSC 74 Final Project)

Course project for COSC 74 (Machine Learning), Dartmouth College, Fall 2026.

I used the FireALT dataset (active layer thickness measurements in burned and unburned Arctic/boreal sites) to predict thaw depth, and I test how well models generalize to new sites, how much random splits overestimate performance, and which features the models rely on.

## Repository contents

| File | Description |
|---|---|
| `FireALT_final.ipynb` | All code: data cleaning, models, cross-validation experiments, figures |
| `FireAltEstimatedRawData.csv` | FireALT dataset (estimated raw data), used as input |
| `requirements.txt` | Python package versions used |

## Data

The dataset is the FireALT synthesis dataset, published on the NSF Arctic Data Center:
https://arcticdata.io/metacat/d1/mn/v2/object/urn:uuid:c424189c-3ef2-4c98-8656-cfb26664ad6a

A copy is included in this repo. If `FireAltEstimatedRawData.csv` is missing, the notebook downloads it automatically from the URL above. Missing values coded as `-9999` are converted to NaN when the file is loaded.

## How to reproduce

```bash
git clone https://github.com/<your-username>/firealt-cosc74.git
cd firealt-cosc74
pip install -r requirements.txt
jupyter notebook FireALT_final.ipynb
```

Then run all cells (Kernel → Restart & Run All). Figures are saved to `figures/`. Random seeds are fixed (`SEED = 74`), so results should match the report.

Tested with Python 3.13, numpy 2.4.6, pandas 2.2.3, scikit-learn 1.6.1, matplotlib 3.10.0. The notebook also runs in Google Colab.

## Author

Gary Ding
