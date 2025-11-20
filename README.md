# 📓📒📓AI-Diary-Companion
A simple Streamlit-based AI-powered diary app that stores your entries in a local SQLite database and provides **emotion detection**, **sentiment analysis**, and **motivational messages**.

🚀 Features

* 🧠 **Emotion Detection** using keyword analysis
* 😊 **Sentiment Analysis** using TextBlob
* 📦 **Local Storage** using SQLite
* 💬 **Motivation Messages** based on detected emotion
* 🖥️ **Beautiful UI** built with Streamlit
* ✍️ Save and view all previous diary entries

📁 Project Structure

AI-Diary-Companion/
│
├── app.py          # Main Streamlit UI
├── db.py           # Database operations (SQLite)
├── nlp.py          # Emotion & sentiment analysis
├── diary.db        # Database (auto-created)
├── requirements.txt
└── README.md


📦 Installation

1️⃣ Clone the repository
#bash
git clone https://github.com/your-username/AI-Diary-Companion.git
cd AI-Diary-Companion


2️⃣ Create a virtual environment (optional but recommended)

#bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

3️⃣ Install dependencies

Create this file:

### **requirements.txt**
streamlit
textblob
sqlite3-binary

Then run:
#bash
pip install -r requirements.txt
python -m textblob.download_corpora

▶️ Running the App

#bash
streamlit run app.py
Open your browser → **[http://localhost:8501](http://localhost:8501)**

🧠 NLP Logic
Sentiment:
* Uses **TextBlob** polarity score
* Ranges from **-1** (negative) to **+1** (positive)
Emotion:
* Determined using
  * Sentiment
  * Keyword matching (e.g., love, angry, scared)

🗃️ Database

The app uses **SQLite** (`diary.db`) with columns:

| Column     | Type      |
| ---------- | --------- |
| id         | INTEGER   |
| created_at | TIMESTAMP |
| text       | TEXT      |
| emotion    | TEXT      |
| sentiment  | REAL      |

Automatically created when running the app.

📌 Example Analysis

"I love spending time with my family!"
→ Emotion: Love | Sentiment: +0.80

"I'm terrified of the dark."
→ Emotion: Fear | Sentiment: -0.20

