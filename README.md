# 🤖 Abstractive Text Summarizer (Deep Learning)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Hugging Face](https://img.shields.io/badge/Model-Google_Pegasus-yellow)
![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-red)

## 📌 Project Overview
This is an advanced **Generative AI** application that performs **Abstractive Summarization**. Unlike traditional summarizers that just pick important sentences, this model understands the context and generates a completely new, concise summary in its own words.

**The Tech:**
It utilizes **Google's PEGASUS (Pre-training with Extracted Gap-sentences for Abstractive SUmmarization Sequence-to-sequence)** model, fine-tuned on the XSum dataset, via the **Hugging Face Transformers** library.

## 🛠️ Features
* **State-of-the-Art Model:** Uses `google/pegasus-xsum`, which is specifically optimized for extreme summarization.
* **Abstractive Capabilities:** Generates human-like summaries rather than just extracting text.
* **Dynamic Length:** Automatically adjusts the summary length based on the word count of the input text.
* **Simple UI:** Built with Streamlit for easy user interaction.

## ⚙️ How It Works
1.  **Input:** User pastes a long paragraph or article into the text area.
2.  **Tokenization:** The `PegasusTokenizer` converts the text into numerical tokens.
3.  **Generation:** The `PegasusForConditionalGeneration` model predicts the most likely sequence of words to form a summary.
4.  **Decoding:** The tokens are converted back into human-readable text and displayed.

## 🚀 How to Run Locally

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/KSAahil/abstractive-summarizer-dl.git](https://github.com/KSAahil/abstractive-summarizer-dl.git)
    cd abstractive-summarizer-dl
    ```

2.  **Install dependencies**
    *Note: This requires PyTorch, which is a heavy install.*
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the App**
    ```bash
    streamlit run src/app.py
    ```

## 📂 Directory Structure
```text
├── src/
│   └── app.py           # Main Streamlit Application
├── requirements.txt     # Dependencies (Torch, Transformers)
└── README.md            # Project documentation