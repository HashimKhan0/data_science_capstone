# SpaceX Falcon 9 Landing Prediction

**Capstone project: IBM Data Science Professional Certificate**

Can we predict whether a Falcon 9 first stage will land successfully? Reusing the first stage is a big part of why SpaceX launches cost less than competitors', so predicting landing success is a proxy for estimating launch cost. The project runs a full data-science workflow, from data collection to a deployed dashboard and a tuned classifier.

## Pipeline

| Step | Notebook / file | What it does |
|---|---|---|
| 1. Data collection (API) | `api_call.ipynb` | Pulls launch records from the SpaceX REST API and filters to Falcon 9 launches |
| 2. Data collection (scraping) | `web_scraping.ipynb` | Scrapes historical launch tables from Wikipedia with BeautifulSoup |
| 3. Data wrangling | `data_wrangling.ipynb` | Cleans the data, handles missing values, builds the binary landing-outcome label |
| 4. EDA with SQL | `exploratory_data_analysis_with_SQL.ipynb` | Queries launch data in SQLite (`my_data1.db`) |
| 5. EDA with visualization | `visualization.ipynb` | Relationships between flight number, payload, orbit, launch site and success rate |
| 6. Geospatial analysis | `interactive_visual_analytics.ipynb` | Folium maps of launch sites, outcomes and proximity to coastlines, railways and cities |
| 7. Dashboard | `board2.py` | Interactive Plotly Dash app: success by launch site and payload vs. outcome |
| 8. Prediction | `prediction.ipynb` | Logistic regression, SVM, decision tree and KNN tuned with `GridSearchCV`, compared on test accuracy and confusion matrices |

## Running the dashboard

```bash
pip install pandas dash plotly
python board2.py
```

## Tech stack

Python · pandas · NumPy · scikit-learn · SQLite / SQL · BeautifulSoup · requests · Folium · Plotly Dash · matplotlib / seaborn
