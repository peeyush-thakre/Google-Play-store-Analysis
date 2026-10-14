Google Play Store Analytics — Plotly Dashboard Package

Run locally:
1. Extract the ZIP.
2. Open a terminal in the extracted folder.
3. Install dependencies: python -m pip install -r requirements.txt
4. Start dashboard: streamlit run app.py

Dashboard:
- Plotly interactive charts for all six tasks.
- No time-window hiding; all chart sections stay visible.
- Filters in sidebar: category, minimum rating, app-name search.
- Uses the original googleplaystore.csv and optional User_Reviews_Google_Play.csv.

Data limitations:
- The standard Google Play Store CSV has no country-level installs, so Task 2 is shown as a category-level chart, not a world choropleth.
- It has no genuine dated monthly install snapshots, so Tasks 3–4 are clearly labeled snapshot summaries rather than fabricated historical trends.
- Task 6 paid-app revenue is only an estimate (listed price × install count); actual revenue and free-app ad/IAP revenue are not provided.
- Strict filters may yield too few rows; in those cases the dashboard shows an explicit fallback message/chart where appropriate.
