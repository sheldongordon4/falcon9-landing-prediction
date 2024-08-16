# Winning the space Race

## Project Overview
This project aims to enhance the predictive capabilities of a private space launch company by determining the factors that influence the successful landing of the Falcon 9 first stage by leveraging extensive data collection from sources such as the SpaceX API and historical launch records from Wikipedia.

we performed rigorous data wrangling and exploratory data analysis (EDA) to ensure data quality and uncover critical insights. Key variables affecting landing success were identified and analyzed through SQL querying and feature engineering, leading to a deeper understanding of the launch dynamics.
Machine learning techniques, including SVM, classification trees, and logistic regression, were employed to build robust predictive models. An interactive dashboard application, developed using Plotly Dash, provides real-time visual analytics, enabling stakeholders to explore launch data dynamically. The analysis revealed that optimizing launch site selection and understanding payload characteristics significantly impact success rates. These insights offer strategic guidance for future launches, potentially reducing costs and increasing the competitive advantage of the company in the space launch market.

### Dataset Used
Data was collected from multiple sources, including the SpaceX API and historical launch records from Wikipedia. Data was retrieved using API requests and web scraping techniques with BeautifulSoup.

### Tools
- JupyterLab Notebook

### Data cleaning/preprocessing
Data wrangling techniques such as cleaning, formatting, and converting data into a suitable structure for analysis were applied.

### Exploratory Data Analysis
Visualizations:
1. Visualization of relationship between Flight number and launch site (bar & scatter)
2. Visualization of relationship between payload and launch site (bar & scatter)
3. Visualization of relationship between success rate and each orbit (bar & scatter)
4. Visualization of relationship between flight number and orbit type (bar & scatter)
5. Visualization of relationship between payload and orbit type (bar & scatter)
6. Visualization of yearly launch success trend

SQL:
1. Display the names of the unique launch sites in the space mission
2. Display 5 records where launch sites begin with the string ‘CCA’
3. Display the total payload mass carried by boosters launched by NASA (CRS)
4. Display average payload mass carried by booster version F9 v1.1
5. List the date when the first successful landing outcome in ground pad was achieved
6. List the names of the boosters which have success in drone ship and have payload mass greater than 4000 but less than 6000
7. List the total number of successful and failure mission outcomes
8. List the names of the booster versions which have carried maximum payload mass
9. List the records which will display the month names, failure landing outcomes in drone ship, booster versions, launch site for the months in year 2015
10. Rank the count of landing outcomes (such as Failure (drone ship) or Success (ground pad)) between the date 2010-06-04 and 2017-03-20, in descending order

### Results
<img width="868" alt="Launch Site Map with Class Markers" src="https://github.com/user-attachments/assets/80a1e7ee-665d-4fbc-b69a-689754bd4819">
<img width="874" alt="Launch Site Proximity to nearest City" src="https://github.com/user-attachments/assets/5e8d3485-4244-4a45-9286-764c63f33bb5">
<img width="976" alt="Pie Chart showing Success Contribution of All Sites" src="https://github.com/user-attachments/assets/8036002f-8c44-497c-9c29-74e956fcb89f">
<img width="976" alt="Screenshot 2024-07-17 at 12 19 15" src="https://github.com/user-attachments/assets/bed30387-f22e-4637-b56d-f91bca17b530">

### ML Model Development, Training and Eveluation
- Used the function train_test_split to create X and Y training and test datasets
- Created logistic regression, support vector machine, decision tree and k nearest neighbor models
- Used GridSearch to find the best parameters for each model as well as used the score method to calculate accuracy of each

<img width="911" alt="Screenshot 2024-07-16 at 13 39 42" src="https://github.com/user-attachments/assets/3d578df3-6d7e-41a1-9a82-7b9147d0bfe5">

### Conclusions
- Launch success is generally greater for higher payload masses.
- Orbit type and booster version are also a very important factors in launch success.
- Success rate increased with time and number of flights due to constant learning and feedback.
- Launch sites are typically located several kilometers from cities while being close to coastlines.
- The most successful launch site is KSC LC-39A with a success rate of 76.9%.
- Using the decision tree model, we can predict, with an 88% accuracy the successful outcome of launches.
