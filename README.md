# IBM Data Science Capstone Project – Falcon 9 First Stage Landing Prediction

This project enhances the predictive capabilities of a private space launch company by analyzing key factors that influence the successful landing of SpaceX Falcon 9’s first stage. By integrating data collection, exploratory analysis, SQL querying, and machine learning, we uncover valuable insights from historical launches.

### Project Overview
The primary objective is to build a data-driven system that predicts Falcon 9 first-stage landing success. We leverage data from multiple sources, including the **SpaceX API** and **Wikipedia**, and use tools such as JupyterLab, SQL, and Python machine learning libraries to derive insights and build predictive models.

### Data Sources
- **SpaceX Launch Data** via the SpaceX API
- **Historical Launch Records** scraped from Wikipedia using **BeautifulSoup**

 ### Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- SQL (via Jupyter notebooks and SQLite)
- Web scraping with BeautifulSoup
- JupyterLab Notebooks
- Plotly for interactive dashboard visualizations

### Data Wrangling & Preprocessing
- Cleaned and merged datasets from SpaceX and Wikipedia
- Converted date fields, parsed payload information
- Created flags for landing success and processed payload masses
- Structured data for SQL querying and modeling

### Exploratory Data Analysis
**Visualizations Created:**
- Relationship between flight number and launch site
- Payload mass vs. launch site
- Launch success vs. orbit type
- Payload mass vs. orbit
- Year-over-year launch success trends
- Booster version performance vs. payload

### SQL Query Tasks
- Identified unique launch sites and filtered by name patterns
- Calculated payload mass by booster version and agency
- Retrieved first successful landing outcomes
- Filtered and ranked mission outcomes and landing types
- Analyzed 2015 landing failures by month and launch site

### Interactive Visual Insights
- **Launch site map** with success/failure markers
- **Distance analysis**: Proximity of launch sites to cities, highways, coastlines
- **Dashboard** with:
  - Dropdown filters by launch site
  - Pie charts of launch success by site
  - Slider-controlled scatter plots (payload vs. success by booster version)

<img width="868" alt="Launch Site Map with Class Markers" src="https://github.com/user-attachments/assets/80a1e7ee-665d-4fbc-b69a-689754bd4819">
<img width="874" alt="Launch Site Proximity to nearest City" src="https://github.com/user-attachments/assets/5e8d3485-4244-4a45-9286-764c63f33bb5">
<img width="976" alt="Pie Chart showing Success Contribution of All Sites" src="https://github.com/user-attachments/assets/8036002f-8c44-497c-9c29-74e956fcb89f">
<img width="976" alt="Screenshot 2024-07-17 at 12 19 15" src="https://github.com/user-attachments/assets/bed30387-f22e-4637-b56d-f91bca17b530">

### Machine Learning Models
We trained four classification models to predict Falcon 9 first-stage landing success:
- Logistic Regression
- Support Vector Machine
- Decision Tree
- K-Nearest Neighbors
**GridSearchCV** was used to tune hyperparameters and evaluate the best-performing models.


<img width="911" alt="Screenshot 2024-07-16 at 13 39 42" src="https://github.com/user-attachments/assets/3d578df3-6d7e-41a1-9a82-7b9147d0bfe5">

### Results & Key Findings
- Higher payload masses correlate with higher success rates
- Booster version and orbit type are strong predictors of landing success
- Launch sites near coastlines, far from cities, dominate successful outcomes
- KSC LC-39A is the most successful site, with a 76.9% success rate
- The decision tree model achieved an 88% accuracy in predicting landing outcomes

### Conclusion
This project successfully demonstrates how combining **API data extraction, web scraping, SQL querying, and machine learning** can lead to actionable insights in aerospace operations. The results can help companies like SpaceX or other launch providers optimize mission planning and resource allocation.
