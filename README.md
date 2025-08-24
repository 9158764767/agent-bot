# Agentic Excel AI Bot

This repository contains a FastAPI-based web application that provides a chat-like interface for uploading and analyzing Excel or CSV files. The bot performs common data-analysis tasks without calling external APIs; everything runs locally using pandas and matplotlib.

## Features

- Upload Excel (.xlsx/.xls) or CSV files.
- Chat-based commands:
  - `summary`: view the dataset shape, columns, missing values and data types.
  - `describe`: see descriptive statistics and a correlation matrix.
  - `clean`: fill missing numeric values with the median and non-numeric values with the mode, and download a cleaned workbook.
  - `visualize`: generate histograms for up to three numeric columns and download the plots in a ZIP file.
  - `forecast target=<column>`: predict the mean of a numeric column and download a single-row workbook with the forecast.

## Local Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/9158764767/agent-bot.git
   cd agent-bot
   ```

2. **Create a virtual environment and install dependencies**  
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows use .venv\\Scripts\\activate
   pip install -r requirements.txt
   ```

3. **Run the server**  
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```
   Open your browser at `http://localhost:8000` to access the web interface.

## Project Structure

```
.
├── main.py              # FastAPI application code
├── templates/
│   └── index.html       # HTML template for the UI
├── static/
│   └── style.css        # CSS for styling
├── LICENSE              # Licensing information (all rights reserved)
└── requirements.txt     # Python dependencies
```

## License

Copyright (c) 2025 Abhishek Hirve. All rights reserved.

This project is proprietary; unauthorized copying, distribution or use is prohibited without prior permission.
