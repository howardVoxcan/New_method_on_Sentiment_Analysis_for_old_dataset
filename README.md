###Vietnamese Social Media Text Classification

This repository presents a comprehensive system for **Vietnamese emotion classification** from social media text. We leverage traditional machine learning (ML), deep learning (DL), transformer-based models, and large language models (LLMs) with integration of **VnEmoLex** – an emotion lexicon for Vietnamese.

---

## 🎯 Project Objectives

- Build a robust pipeline for sentiment and emotion analysis on Vietnamese user-generated content (UGC)
- Compare models across three domains: social media (VSMEC), student feedback (VSFC), and hate speech detection (ViCTSD)
- Incorporate VnEmoLex into the learning process to improve accuracy

---

## 📁 Folder Structure

```

.
├── Preprocessing material/                # Emoji, teencode, stopwords, spelling correction resources
│   ├── emoji2word.xlsx
│   ├── vietnamese-emoticon.csv
│   ├── vietnamese-misspell.csv
│   ├── vietnamese-stopwords\*.txt
│   └── vietnamese-teencode.txt

├── VSFC/                                 # Student feedback classification
│   ├── Baseline/
│   │   ├── svm\_lg\_tune.ipynb             # SVM & Logistic Regression
│   │   ├── deep\_vsfc\_clean.ipynb         # TextCNN & BiGRU
│   │   ├── phobert\_vsfc\_clean.ipynb      # PhoBERT fine-tuning
│   │   ├── prompt\_vsfc.ipynb             # LLM (Gemini) evaluation
│   │   └── 5\_model\_vsfc\_clean.ipynb      # Summary of all 5 approaches
│   ├── Dataset/
│   │   ├── df\_train\_clean.csv, ...
│   │   └── VnEmoLex.xlsx
│   └── Preprocessing/
│       └── pre\_paper.ipynb

├── VSMEC/                                # Social media sentiment classification
│   ├── Baseline/
│   │   ├── svm\_lg\_tune.ipynb
│   │   ├── bi\_gru\_emolex.ipynb
│   │   ├── prompt\_vsmec.ipynb
│   │   └── text\_paper\*.ipynb             # Emotion vector experiments
│   ├── Dataset/
│   │   ├── df\_train\_clean.csv, ...
│   │   └── VnEmoLex.xlsx
│   └── Preprocessing/
│       └── test.ipynb

├── ViCTSD/                               # Hate speech detection
│   ├── Baseline/
│   │   ├── svm\_lg\_tune.ipynb
│   │   ├── prompt\_vstsd\_clean.ipynb
│   │   ├── phobert\_vctsd\_clean.ipynb
│   │   └── bi\_vnemolex.ipynb
│   ├── Dataset/
│   │   ├── df\_train\_clean.csv, ...
│   │   └── VnEmoLex.xlsx
│   └── Preprocessing/
│       └── Copy of paper\_pre.ipynb

├── Slide thuyết trình.pptx               # Final presentation slide (in Vietnamese)
├── README.md                             # You are here
└── Vietnamese social media text classification.pdf  # Final report

````

---

## 🧠 Method Highlights

- **Text Preprocessing**: emoji normalization, teencode conversion, misspelling correction, stopword filtering.
- **Model Pipeline**:
  - ML: SVM, Logistic Regression
  - DL: TextCNN, BiGRU (+ VnEmoLex vector)
  - Transformer: PhoBERT
  - LLM: Gemini 2.0 Flash (zero-shot & few-shot)
- **Emotion Feature Integration**: Use VnEmoLex to convert text into 8-dimensional vectors (one per emotion).
- **Datasets**:
  - `VSMEC`: 7 emotion classes from social media
  - `VSFC`: Student feedback with 3 polarities
  - `ViCTSD`: Toxic speech detection (Clean, Offensive, Hate)

---

## 📊 Experimental Results

| Model Type | Best Accuracy |
|------------|---------------|
| SVM        | 89.2% (ViCTSD)|
| BiGRU + EmoLex | 90.2% (VSFC) |
| PhoBERT    | 93.4% (VSFC)  |
| Gemini Few-shot | 93% (VSFC) |

---

## 📎 Demo

🔗 [Demo video using Django](https://drive.google.com/drive/u/0/folders/1zIfNzn-w4r5RVcDAjDffU0qIgK9dvJ1j)

---

## 🛠 Requirements

- Python 3.8+
- Transformers (for PhoBERT)
- PyTorch / Tensorflow
- Pandas, Numpy, Scikit-learn
- Openpyxl (for `.xlsx` preprocessing files)

```bash
pip install -r requirements.txt
````

---

## 👨‍💻 Authors

This project was developed by:

* **Vo Quang Nhat Hoang**
* **Do Thanh Dat**
* **Tran Cong Hien**
* **Phan Vo My Huyen**
* **Doan Minh Tuan**

---

## 📌 License

For academic or educational purposes only.
