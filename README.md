# AI-Powered-Text-Summarizer-Python-CLI-Tool-
AI-Powered Text Summarizer (Python CLI Tool)
ai-text-summarizer/
├── summarizer.py
├── requirements.txt
└── README.md
from transformers import pipeline

def summarize_text(text):
    summarizer = pipeline("summarization", model="sshleifer/distilbart-cnn-12-6")
    summary = summarizer(text, max_length=100, min_length=30, do_sample=False)
    return summary[0]['summary_text']

if __name__ == "__main__":
    print("Paste the text you want to summarize (end with ENTER + Ctrl+D):")
    user_input = ""
    try:
        while True:
            user_input += input() + "\n"
    except EOFError:
        pass

    summary = summarize_text(user_input)
    print("\n🧠 Summary:\n", summary)
transformers
torch
# 🧠 AI Text Summarizer (CLI)

This is a simple CLI tool that uses Hugging Face Transformers to summarize long pieces of text.

## 🚀 Features
- Uses `distilBART` model from Hugging Face
- Command-line interface
- Summarizes long paragraphs into short summaries

## 🛠️ How to Use
1. Clone the repo  
```bash
git clone https://github.com/yourusername/ai-text-summarizer.git
cd ai-text-summarizer
pip install -r requirements.txt
python summarizer.py
Paste long text and press Ctrl+D (or Ctrl+Z on Windows) to get the summary.Paste the text you want to summarize (end with ENTER + Ctrl+D):
[PASTE HERE]
🧠 Summary:
[SUMMARIZED OUTPUT]

---

I'll now zip it for you. One moment…
👉 Click here to download your AI Text Summarizer project
pip install -r requirements.txt
python summarizer.py
