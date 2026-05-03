# TrendPulse: What's Actually Trending Right Now

TrendPulse is a 4-stage Python data pipeline project built using the public HackerNews API.  
The project collects trending stories, cleans the raw JSON data, performs statistical analysis using Pandas and NumPy, and finally creates visual dashboards using Matplotlib.

This project was developed as part of the TrendPulse assignment series.

---

## 📌 Project Workflow

Task 1 → Task 2 → Task 3 → Task 4

- **Task 1:** Fetch trending story data from HackerNews API and save as JSON
- **Task 2:** Clean the raw JSON data using Pandas and save as CSV
- **Task 3:** Perform analysis using Pandas & NumPy and create new analytical columns
- **Task 4:** Generate visual charts and a dashboard using Matplotlib

---

## 📁 Repository Structure

trendpulse-bhavani/

│── task1_data_collection.py  
│── task2_data_processing.py  
│── task3_analysis.py  
│── task4_visualization.py  
│── README.md  
│  
├── data/  
│   ├── trends_YYYYMMDD.json  
│   ├── trends_clean.csv  
│   └── trends_analysed.csv  
│  
└── outputs/  
    ├── chart1_top_stories.png  
    ├── chart2_categories.png  
    ├── chart3_scatter.png  
    └── dashboard.png

---

## 🔹 Task 1 — Data Collection from API

Used the official HackerNews public API to fetch the top 500 trending story IDs.

For each story:
- fetched full item details
- classified the story into one of five categories using title keyword matching:
  - technology
  - worldnews
  - sports
  - science
  - entertainment
- collected up to 25 stories per category
- saved the final output as a JSON file inside the `data/` folder

### Output:
`data/trends_YYYYMMDD.json`

---

## 🔹 Task 2 — Data Cleaning & CSV Export

Loaded the raw JSON file into a Pandas DataFrame and performed the following cleaning steps:

- removed duplicate stories using `post_id`
- removed rows with missing important values
- converted `score` and `num_comments` to integer type
- filtered out low quality stories where score < 5
- removed extra whitespace from story titles

Saved the cleaned data into:

### Output:
`data/trends_clean.csv`

---

## 🔹 Task 3 — Analysis with Pandas & NumPy

Loaded the cleaned CSV file and explored the dataset using Pandas and NumPy.

Performed:
- shape check
- average score and comments
- mean, median, standard deviation of score
- highest and lowest score
- most frequent category
- story with highest number of comments

Added two new analytical columns:
- `engagement = num_comments / (score + 1)`
- `is_popular = True if score > average score else False`

### Output:
`data/trends_analysed.csv`

---

## 🔹 Task 4 — Visualizations with Matplotlib

Generated 3 different visual charts:

1. **Top 10 Stories by Score** (horizontal bar chart)
2. **Stories per Category** (bar chart)
3. **Score vs Comments** (scatter plot with popular vs non-popular split)

Also created a combined dashboard containing all charts.

### Output:
Stored inside `outputs/` folder as PNG files.

---

## 🛠 Technologies Used

- Python
- requests
- json
- os
- time
- datetime
- Pandas
- NumPy
- Matplotlib

---

## 📊 Final Outputs Generated

### Data Files
- `data/trends_YYYYMMDD.json`
- `data/trends_clean.csv`
- `data/trends_analysed.csv`

### Visual Files
- `outputs/chart1_top_stories.png`
- `outputs/chart2_categories.png`
- `outputs/chart3_scatter.png`
- `outputs/dashboard.png`

---

## 🎯 Key Learning Outcomes

Through this project I practiced:

- working with real-world APIs
- handling JSON data
- data cleaning using Pandas
- performing statistical analysis with NumPy
- feature engineering
- creating visual dashboards with Matplotlib
- saving and organizing project outputs

---

## 🚀 How to Run the Project

Run the Python files in the following order:

1. `task1_data_collection.py`
2. `task2_data_processing.py`
3. `task3_analysis.py`
4. `task4_visualization.py`

Each task uses the output of the previous task.

---

## 👩‍💻 Author

Bhavani
