# Text Summarization pipeline 📰✂️🤖

## 📌 Overview  
Text Summarization with T5 This project implements an abstractive text summarization pipeline using the T5 Transformer model. It trains and evaluates on the CNN/DailyMail dataset, with evaluation metrics including ROUGE and BERTScore. The notebook covers data preprocessing, model fine-tuning, evaluation.

## 📂 Dataset  
The project uses the **CNN/DailyMail dataset**:  
- `train.csv` → Training articles & summaries  
- `validation.csv` → Validation set  
- `test.csv` → Test set
- Data link: https://www.kaggle.com/datasets/gowrishankarp/newspaper-text-summarization-cnn-dailymail

## 📝Preprocessing
- Keep only essential columns: `article`, `highlights`  
- Add prefix `"summarize:"` to input text (T5 requirement)  
- Tokenize inputs and summaries  
- Truncate / pad sequences for uniform length  

## ⚙️ Model Used  
- **T5-small** (fine-tuned for summarization)  
- Can be scaled to **T5-base** or **T5-large** for better performance  

## 📊 Feature Extraction  
- Tokenization with Hugging Face `T5Tokenizer`  
- Padding & truncation for long sequences  
- Seq2Seq training with Hugging Face `Trainer`  

## 📈 Evaluation Metrics  
- **ROUGE Score** → n-gram overlap with reference summary  
- **BERTScore** → semantic similarity  


## 📥 Clone Repository  
```bash
git clone https://github.com/Mohamed-Kenawy/Text_Summarization_pipeline.git
cd Text_Summarization_pipeline
