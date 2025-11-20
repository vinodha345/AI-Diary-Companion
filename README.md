# 📓📒📓AI-Diary-Companion
A simple Streamlit-based AI-powered diary app that stores your entries in a local SQLite database and provides **emotion detection**, **sentiment analysis**, and **motivational messages**.

# 🧩 Problem Statement

People often experience emotions they struggle to express or understand. Writing a diary helps, but a traditional diary cannot:
1.Analyze how the user feels
2.Give emotional feedback or motivation
3.Store entries in an organized digital format
3.Detect changes in emotional patterns over time
As a result, users miss opportunities for self-reflection, emotional awareness, and mental well-being improvement.

# ✅ Solution Overview
The AI Diary Companion provides an intelligent, user-friendly digital diary that:

✔️ 1. Analyzes the user’s emotions
Using NLP techniques (TextBlob + keyword mapping), it detects:
Emotion category (Happy, Sad, Angry, Fear, Love, etc.)
Sentiment score (-1.0 to +1.0)

✔️ 2. Generates motivational responses
Based on the detected emotion, the app gives personalized motivation to help users feel supported.

✔️ 3. Saves diary entries automatically
All entries are stored in a local SQLite database with:
1.Timestamp
2.Diary text
3.Emotion
4.Sentiment score
This allows users to revisit their emotional journey anytime.

✔️ 4. Simple and accessible UI
A clean Streamlit interface enables users to:
1.Type an entry
2.Analyze emotions
3.Save the entry
4.View past entries

✔️ 5. Lightweight and private
Data is stored locally, ensuring privacy while keeping the app fast and easy to run.

# 🚀 Features
* 🧠 **Emotion Detection** using keyword analysis
* 😊 **Sentiment Analysis** using TextBlob
* 📦 **Local Storage** using SQLite
* 💬 **Motivation Messages** based on detected emotion
* 🖥️ **Beautiful UI** built with Streamlit
* ✍️ Save and view all previous diary entries

# 📁 Project Structure

AI-Diary-Companion/
│

├── app.py          # Main Streamlit UI

├── db.py           # Database operations (SQLite)

├── nlp.py          # Emotion & sentiment analysis

├── diary.db        # Database (auto-created)

├── requirements.txt

└── README.md


# 📦 Installation

 1️⃣ Clone the repository
 #bash
 git clone https://github.com/your-username/AI-Diary-Companion.git
 cd AI-Diary-Companion


 2️⃣ Create a virtual environment (optional but recommended)

 #bash
 python -m venv venv
 source venv/bin/activate   # macOS/Linux
 venv\Scripts\activate      # Windows

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

# 🧠 NLP Logic
Sentiment:
* Uses **TextBlob** polarity score
* Ranges from **-1** (negative) to **+1** (positive)
Emotion:
* Determined using
  * Sentiment
  * Keyword matching (e.g., love, angry, scared)

# 🗃️ Database
The app uses **SQLite** (`diary.db`) with columns:

| Column     | Type      |
| ---------- | --------- |
| id         | INTEGER   |
| created_at | TIMESTAMP |
| text       | TEXT      |
| emotion    | TEXT      |
| sentiment  | REAL      |
Automatically created when running the app.

# 🔗 Example Analysis
"I love spending time with my family!"
→ Emotion: Love | Sentiment: +0.80

"I'm terrified of the dark."
→ Emotion: Fear | Sentiment: -0.20

# 🔚 Conclusion
The AI Diary Companion successfully transforms traditional diary writing into an intelligent and emotionally aware journaling experience. By combining sentiment analysis, emotion detection, and a user-friendly interface, the system helps users better understand their emotional patterns while offering personalized motivation for mental well-being.

With secure local storage, lightweight design, and meaningful feedback, this project demonstrates how AI can positively support daily self-reflection and personal growth. The diary not only records what users write—but also helps them reflect, learn, and feel encouraged every day.
