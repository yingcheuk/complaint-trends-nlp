# 🗂️ complaint-trends-nlp

Tracking emerging themes in consumer credit reporting complaints using BERTopic and time-based NLP analysis.
Focus on unsupervised learning, semantic clustering, and trend interpretation.

Goal:
Uncover hidden or rising complaint topics over the past 3 months to support issue monitoring and early detection of consumer risks.

---

## 📌 Project Overview

This project applies unsupervised topic modeling on complaint narratives submitted to the CFPB between Jan 9 and Apr 9, 2025.
It focuses on:  

- Cleaning & preprocessing text data  
- Modeling complaint narratives with BERTopic  
- Visualizing topic frequency trends over time  
- Comparing discovered topics to official CFPB issue labels  
- Highlighting new or overlooked themes in consumer complaints  

---

## 💡 Why This Matters

Manual categorization (e.g. CFPB’s “issue” column) may miss nuanced or emerging concerns from consumers.
By applying modern NLP methods, we can:  

- Identify semantic themes in consumer voices  
- Monitor topic evolution over time  
- Detect potential regulatory gaps or early warning signs  

---

## 🧠 Techniques Used 

- Unsupervised NLP: BERTopic with HDBSCAN + UMAP  
- Embeddings: Sentence Transformers (all-MiniLM-L6-v2)  
- Time-based trend analysis by date_received  
- Text preprocessing: stopword removal, lemmatization, deduplication  
- Visualization: BERTopic’s interactive viewer, line plots for topic trends  

---

## 📁 Project Structure

```
complaint-trends-nlp/
│
├── data/                   # Filtered complaints with narratives
├── notebooks/              # Preprocessing, topic modeling, trend analysis
├── src/                    # Reusable preprocessing & modeling functions
│   ├── preprocessing.py        # Text cleaning and filtering
│   ├── topic_modeling.py       # BERTopic training and tuning
│   ├── trend_analysis.py       # Topic time-series and trend tools
└── README.md               # Project documentation
```

---

## 🔧 Function Overview

- 🧼 clean_text()  
    → Lowercase, remove special characters, lemmatize complaints  
- 🪓 filter_complaints()  
    → Keep narratives with sufficient content length  
- 🧠 run_bertopic()  
    → Fit BERTopic model and assign topics to each complaint  
- 📈 analyze_topic_trends()  
    → Aggregate topic frequencies by date  
- 📊 compare_with_official_issues()  
    → Align modeled topics with CFPB-labeled issues and flag mismatches  
- 🖼️ plot_topic_trends()  
    → Visualize top topic changes over time  

---

## 📒 Notebooks

- `01_preprocessing.ipynb`: Clean and filter raw complaint narratives  
- `02_topic_modeling.ipynb`: Train BERTopic model, extract top keywords  
- `03_trend_analysis.ipynb`: Plot topic trends and match to CFPB labels  

---

## 🚀 Current Goals

- Build interpretable NLP pipeline to track consumer complaint trends  
- Highlight topics not explicitly captured by CFPB categories  
- Deliver insights through interactive topic visualizations  
- Set up modular code for future reuse or comparison with other product categories  

---

## 📤 Example Output

After modeling, each complaint has a topic assignment like:

---

## 🔮 Future Improvements

- Add dynamic topic modeling for evolving themes  
- Extend to other categories (e.g., Debt Collection)  
- Create interactive dashboards for stakeholder use  
- Explore supervised models to predict official issue categories  
- Test anomaly detection for early alerting of rare complaint types  

---