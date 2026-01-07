

# 🤖 AI Text Detector (RoBERTa + PEFT)

A lightweight, high-accuracy binary classifier designed to distinguish between **Human-Written** and **AI-Generated** text. This project fine-tunes the `FacebookAI/roberta-base` model using **PEFT (Parameter-Efficient Fine-Tuning) / LoRA**, making it efficient to train and deploy.

It includes a user-friendly web interface built with **Streamlit**.

*(Replace this link with a screenshot of your actual app if you upload one)*

## 🚀 Features

* **High Accuracy:** Fine-tuned on a balanced dataset of human and AI text.
* **Efficient:** Uses LoRA (Low-Rank Adaptation) to keep the model size small (~2-5MB for adapters) while maintaining performance.
* **Real-time Interface:** Simple web UI to test text instantly.
* **Confidence Scores:** Visualizes the probability of Human vs. AI.

## 🛠️ Tech Stack

* **Model:** RoBERTa Base (FacebookAI)
* **Technique:** PEFT / LoRA
* **Frameworks:** PyTorch, Hugging Face Transformers
* **Interface:** Streamlit
* **Language:** Python 3.10+

## 📂 Project Structure

```text
├── model/       # The saved model folder
│   ├── adapter_config.json     # LoRA configuration
│   ├── adapter_model.safetensors # The trained adapter weights
│   ├── vocab.json              # Tokenizer vocabulary
│   └── tokenizer_config.json   # Tokenizer settings
├── app.py                      # The Streamlit web application
├── README.md                   # Project documentation
└── requirements.txt            # List of dependencies

```

## ⚙️ Installation

1. **Clone or Download the repository** to your local machine.
2. **Create a virtual environment** (Recommended):
```bash
python -m venv venv
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

```


3. **Install Dependencies:**
Create a `requirements.txt` file (content provided below) and run:
```bash
pip install -r requirements.txt

```



## 🏃‍♂️ How to Run the App

1. Navigate to the project folder in your terminal:
```bash
cd path/to/project

```


2. Run the Streamlit app:
```bash
streamlit run app.py

```


3. A browser tab will automatically open at `http://localhost:8501`.
4. Paste any text into the box and click **"Analyze Text"**.

## 🧠 Model Details

* **Base Model:** `roberta-base`
* **Dataset:** Subset of `artem9k/ai-text-detection-pile` (Balanced 50/50 split).
* **Labels:**
* `0`: **Human-Written**
* `1`: **AI-Generated**



## 📦 Requirements File

Create a file named `requirements.txt` and paste this content:

```text
torch
transformers
peft
streamlit
datasets
accelerate

```

## 🤝 Contributing

Feel free to open issues or submit pull requests if you find bugs or want to improve the training pipeline.

---

