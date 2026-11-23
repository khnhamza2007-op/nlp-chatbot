# NLP Chatbot: Ethical Study Assistant

A simple chatbot that answers short questions about studying, honesty, stress, and AI ethics. It mixes basic rules (if/elif) with a small machine learning step (TF-IDF + cosine similarity) to guess what the user means.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/khnhamza2007-op/nlp-chatbot/blob/main/AI_Chatbox.ipynb)

## How it works

1. **Rule-based part**: handles greetings (`hi`, `hello`) and goodbyes (`bye`).
2. **Machine learning part**:
   - The keywords (`ai ethics`, `study`, `honesty`, `stress`) are turned into numbers with `TfidfVectorizer`.
   - Your message is turned into numbers the same way.
   - `cosine_similarity` finds the keyword closest to your message.
   - If the match score is above `0.3`, the bot gives the answer for that keyword. Otherwise it says it can only answer simple educational questions.

## Topics the bot knows

| Keyword | Reply |
|---|---|
| `ai ethics` | AI ethics means using AI responsibly and fairly. |
| `study` | Study regularly, avoid plagiarism, and be honest. |
| `honesty` | Honesty helps build trust and improves learning. |
| `stress` | You can reduce stress by resting and managing time. |

## Run it

### Option 1: Google Colab (easiest)
Click the **Open In Colab** badge above and run the cell.

### Option 2: On your computer

1. Install Python 3 and scikit-learn:
   ```bash
   pip install scikit-learn
   ```
2. Open the notebook:
   ```bash
   pip install notebook
   jupyter notebook AI_Chatbox.ipynb
   ```
3. Run the cell and chat. Type `bye` to stop.

## Example

```
Chatbot started. Type 'bye' to stop.
You: ai ethics
Bot: AI ethics means using AI responsibly and fairly.
You: bye
Bot: Goodbye! Keep learning ethically 📘
```

## Built with

- Python
- scikit-learn (`TfidfVectorizer`, `cosine_similarity`)

## Ideas to improve it

- Add more keywords and answers
- Use full sentences as training data instead of single keywords
- Add a simple web or app interface

## Author

Hamza ([@khnhamza2007-op](https://github.com/khnhamza2007-op))
