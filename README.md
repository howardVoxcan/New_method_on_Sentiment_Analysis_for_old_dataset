# New_method_on_Sentiment_Analysis_for_old_dataset

This project focuses on classifying emotions in Vietnamese texts collected from social media using a hybrid approach that combines machine learning, deep learning, transformer-based models, and large language models (LLMs). Additionally, we enhance the system by integrating the VnEmoLex emotion lexicon for better semantic understanding.

🎯 Project Objectives
To develop a robust sentiment/emotion classification system tailored for Vietnamese social media data.

To compare the effectiveness of traditional machine learning, deep learning, and LLMs on real-world datasets.

To utilize VnEmoLex – a Vietnamese emotion lexicon – to improve emotion recognition accuracy.

📌 Key Features
Preprocessing pipeline: Includes emoji normalization, teencode expansion, spelling correction, and abbreviation mapping.

Emotion lexicon integration: VnEmoLex is used to extract emotion vectors from raw text and fused with deep learning features.

Multi-model comparison:

Traditional ML: SVM, Logistic Regression

Deep Learning: Text-CNN, BiGRU

Transformer: PhoBERT

LLM: Gemini-2.0 Flash (zero-shot & few-shot prompting)

Benchmark Datasets:

UIT-VSMEC (Emotion classification from social media)

UIT-VSFC (Student feedback sentiment)

UIT-ViCTSD (Toxic vs. clean speech detection)

🧠 Methodology Overview
Data Preprocessing

Normalize emojis, teencode, and common spelling errors

Convert text into emotion-aware features using VnEmoLex

Feature Extraction

Combine BoW / TF-IDF with emotion vectors

Use tokenized input for PhoBERT and Gemini models

Model Training & Evaluation

Train and evaluate models on each dataset

Use accuracy and macro F1-score as performance metrics

📊 Results Highlights
PhoBERT outperformed traditional and deep learning models on most tasks.

Few-shot prompting with Gemini achieved competitive performance without retraining.

VnEmoLex significantly boosted model accuracy, especially in deep learning setups.

🔬 Limitations
Sarcastic or ambiguous sentences still pose challenges.

VnEmoLex lacks slang/teencode coverage, which affects social media understanding.

LLM token limit issues may affect few-shot performance with large prompts.

🔮 Future Work
Expand and update VnEmoLex with slang and emoji context.

Fine-tune LLMs like GPT or LLaMA specifically for Vietnamese tasks.

Explore POS tagging and dependency parsing for richer contextual embeddings.

