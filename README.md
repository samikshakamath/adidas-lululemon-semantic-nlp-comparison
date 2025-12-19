# A Comparative Analytical Study of Adidas and Lululemon based on Customer Sentiment

 - **Author**: Samiksha Kamath 
- **Project Date**: 29/4/2025


## NLP-Based Brand Sentiment Analysis – Adidas vs. Lululemon

This project conducts a comparative analysis of consumer discourse surrounding Adidas and Lululemon by applying advanced natural language processing (NLP) techniques to unstructured Twitter data. Leveraging Latent Dirichlet Allocation (LDA) for unsupervised topic modeling and sentiment-aware text preprocessing, it uncovers latent thematic structures, emotional tone distributions, and brand-specific conversational patterns. The analysis reveals nuanced differences in customer perception, loyalty drivers, and experiential expectations, offering actionable insights for strategic marketing, brand positioning, and customer engagement optimization within the competitive apparel sector.

---

## Objective

To transform unstructured tweet data into structured brand intelligence by:

- Detecting latent topics of discussion using unsupervised learning (LDA)
- Comparing sentiment distribution across brands
- Uncovering brand-specific thematic clusters (e.g., delivery, quality, service, sustainability)
- Supporting evidence-based marketing and customer experience (CX) design

---

## Tools & Technologies

| Area                  | Tools Used                                              |
|-----------------------|----------------------------------------------------------|
| Programming           | Python (Jupyter Notebook)                                |
| Text Preprocessing    | NLTK, spaCy, Gensim, Regular Expressions                 |
| Topic Modeling        | Gensim LDA, pyLDAvis, Coherence Scoring                  |
| Visualization         | Matplotlib, pyLDAvis (interactive HTML exports)         |
| Data Source           | Twitter-scraped CSVs: `adidas_tweets.csv`, `lululemon_tweets.csv` |

---

## Dataset Overview

Two brand-specific datasets of raw tweets were used:

- `adidas_tweets.csv` – 5,000+ Adidas tweets
- `lululemon_tweets.csv` – 5,000+ Lululemon tweets

Each entry contains tweet text, timestamp, and metadata fields. All tweets were in English and collected using a consistent scraping window for fairness.

---

## Preprocessing Pipeline

- Lowercasing & punctuation stripping  
- Stopword removal using NLTK  
- Lemmatization with spaCy  
- Tokenization & bigram formation  
- Vectorization using `CountVectorizer`  
- Topic coherence tuning (multiple k values evaluated)

---

## Topic Modeling Results

### Adidas

| Topic ID | Dominant Themes                         | Keywords                          |
|----------|------------------------------------------|-----------------------------------|
| 0        | Delivery Delays, Customer Service        | delay, order, help, refund        |
| 1        | Footwear Quality & Performance           | shoe, fit, size, comfort          |
| 2        | Promotions and Product Drops             | drop, collection, release, sale   |

### Lululemon

| Topic ID | Dominant Themes                         | Keywords                          |
|----------|------------------------------------------|-----------------------------------|
| 0        | Gratitude for Service Staff              | thank, help, store, great         |
| 1        | Product Fit & Aesthetic                  | leggings, soft, look, color       |
| 2        | Brand Ethos & Lifestyle Connection       | yoga, vibe, self-care, love       |

---

## Comparative Insight Summary

- **Tone & Sentiment**:  
  Adidas tweets skew toward **transactional and issue-oriented** language (support, delay), whereas Lululemon tweets tend toward **emotionally positive, lifestyle-aligned** narratives.

- **Thematic Focus**:  
  Adidas customers emphasize **delivery logistics, quality expectations**, and occasional frustration.  
  Lululemon's audience reflects **community, gratitude, and aesthetic alignment** with the brand’s wellness identity.

- **Brand Implication**:  
  Adidas can enhance experience through **post-purchase CX and fulfillment communication**.  
  Lululemon should capitalize on its emotional resonance via **community-driven content and loyalty reinforcement**.

---

## Repository Structure

- `README.md` – This documentation  
- `20703562_K_ASA_CW2_BUSI4370_SPR1 24-25.pdf` – Final report  
- `20703562_S_ASA_CW2_BUSI4370_SPR1_24-25.ipynb` – Full Jupyter notebook with code  
- `adidas_tweets.csv` – Adidas tweet dataset  
- `lululemon_tweets.csv` – Lululemon tweet dataset  
- `Adidas_lda_visualization_adidas.html` – Interactive LDA visualization for Adidas  
- `Lululemon_lda_visualization_4topics.html` – Interactive LDA visualization for Lululemon  

---

## Key Deliverables

- Brand-level LDA topic models with coherence validation  
- pyLDAvis interactive visualization exports for stakeholder review  
- Sentiment & tone mapping across thematic dimensions  
- Strategic recommendations for marketing personalization, voice tone refinement, and CX priorities

---

_This project exemplifies the power of unstructured data transformation into actionable brand intelligence, delivering measurable insight into consumer sentiment, product perception, and competitive positioning._
