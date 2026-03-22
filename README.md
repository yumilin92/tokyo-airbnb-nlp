# 💬 Tokyo Airbnb Reviews — Multilingual Sentiment Analysis

NLP analysis of 400K+ Tokyo Airbnb reviews across 43 languages — 
using TextBlob for English and a BERT transformer model for Japanese.

---

## 🔍 Key Findings

1. **Tokyo attracts a truly global audience** — 43 languages detected 
   in 50,000 sampled reviews
2. **92.7% positive sentiment** in both English and Japanese — 
   Tokyo hosts deliver consistently excellent experiences
3. **Location and transport** dominate English positive reviews — 
   "station", "location", "clean", "walk"
4. **Cleanliness is #1 for Japanese guests** — 清潔 (clean) and 
   綺麗 (beautiful) lead Japanese positive word clouds
5. **Room size is the top complaint** in both languages — 
   "small" in English, 部屋 (room) in Japanese negative reviews
6. **コンビニ (convenience store)** proximity uniquely matters 
   to Japanese guests — not mentioned by international reviewers
7. **Japanese guests leave 4x more negative reviews** (2.8% vs 0.7%) — 
   cultural difference in feedback style, not lower satisfaction

---

## 📊 Results Summary

### Sentiment Distribution

| Sentiment | English | Japanese |
|-----------|---------|----------|
| Positive | 92.7% | 92.7% |
| Neutral | 6.6% | 4.5% |
| Negative | 0.7% | 2.8% |

### Language Distribution (50K sample)

| Language | Count | Share |
|----------|-------|-------|
| English | 24,976 | 49.9% |
| Japanese | 14,561 | 29.1% |
| Korean | 3,552 | 7.1% |
| Chinese (Simplified) | 3,531 | 7.1% |
| Other (39 languages) | 3,380 | 6.8% |

---

## 🛠️ Methods

### English — TextBlob
- Lexicon-based sentiment analysis
- Polarity score: -1.0 (negative) to +1.0 (positive)
- 24,990 English reviews analyzed
- Average polarity: 0.375

### Japanese — BERT Transformer
- Model: `koheiduck/bert-japanese-finetuned-sentiment`
- Context-aware deep learning approach
- 2,000 Japanese reviews analyzed
- Average confidence score: **0.955**

### Japanese Word Analysis — Janome
- Morphological analysis for Japanese tokenization
- Extracts nouns, adjectives, verbs
- Generates Japanese word clouds with proper font rendering

---

## 📁 Repository Structure

```
tokyo-airbnb-nlp/
│
├── data/
│   ├── reviews.csv               # raw Airbnb reviews (407K)
│   └── listings_clean.csv        # cleaned listings for neighbourhood merge
│
├── visuals/
│   ├── english_sentiment.png     # sentiment distribution + neighbourhood chart
│   ├── wordclouds.png            # English positive/negative word clouds
│   ├── wordclouds_japanese.png   # Japanese positive/negative word clouds
│   └── en_vs_jp_sentiment.png    # cross-language sentiment comparison
│
├── 01_sentiment_analysis.ipynb
└── README.md
```

---

## 🛠️ Tech Stack

- **Python 3.12**
- **TextBlob** — English sentiment analysis
- **transformers (BERT)** — Japanese sentiment analysis
- **langdetect** — automatic language detection
- **Janome** — Japanese morphological tokenization
- **WordCloud** — word cloud generation
- **NLTK** — English stopwords
- **pandas / numpy** — data processing
- **matplotlib / seaborn** — visualization

---

## 📦 Dataset

**Source:** [Kaggle — Tokyo Airbnb Open Data 2023](https://www.kaggle.com/datasets/lucamassaron/tokyo-airbnb-open-data-2023)  
**Original source:** Inside Airbnb (insideairbnb.com)  
**Size:** 407,670 reviews | 43 languages detected  
**Period:** 2011–2023

---

## 🚀 Getting Started

```bash
git clone https://github.com/yumilin92/tokyo-airbnb-nlp.git
cd tokyo-airbnb-nlp

pip install pandas numpy matplotlib seaborn textblob langdetect \
            wordcloud nltk transformers torch fugashi unidic-lite janome

jupyter notebook
```

---

## 👤 Author

**Yulia Vovk**  
Economics background + Data Science  
📍 Tokyo, Japan  
🔗 [Kaggle](https://kaggle.com/yuliavovk) | [GitHub](https://github.com/yumilin92)
