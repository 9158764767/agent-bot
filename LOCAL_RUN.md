# Running Agentic Excel AI Bot Locally

Follow these steps to run the chat-based Excel analysis bot on your own machine.

## 1. Clone the repository and set up a virtual environment

...
git clone https://github.com/9158764767/agent-bot.git
cd agent-bot
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

## 2. Install dependencies

```
pip install -r requirements.txt
```

## 3. Start the server

```
uvicorn main:app --host 0.0.0.0 --port 8000
```

## 4. Use the web interface

Open your browser at [http://localhost:8000](http://localhost:8000). Upload your Excel or CSV file once, then use the chat box to send commands like `summary`, `describe`, `clean`, `visualize`, or `forecast target=<column>`.

This application is self-contained and runs locally without calling any external APIs or services.
