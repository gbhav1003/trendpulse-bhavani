# trendpulse-bhavani
# TrendPulse Task 1 - Data Collection

This project is the first part of the TrendPulse pipeline.

## Objective
Fetch trending stories from HackerNews public API, classify them into five categories, and save the collected data into a JSON file.

## Categories Used
- technology
- worldnews
- sports
- science
- entertainment

## Technologies Used
- Python
- requests
- json
- os
- time
- datetime

## Output
The script creates a `data/` folder and stores a file in the format:

data/trends_YYYYMMDD.json

Each story contains:
- post_id
- title
- category
- score
- num_comments
- author
- collected_at
