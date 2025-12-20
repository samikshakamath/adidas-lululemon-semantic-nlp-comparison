# A Comparative Analytical Study of Adidas and Lululemon based on Customer Sentiment

 - **Author**: Samiksha Kamath 
- **Project Date**: 29/4/2025


## NLP-Based Brand Sentiment Analysis – Adidas vs. Lululemon

This project conducts a comparative analysis of consumer discourse surrounding Adidas and Lululemon by applying advanced natural language processing (NLP) techniques to unstructured Twitter data. Leveraging Latent Dirichlet Allocation (LDA) for unsupervised topic modeling and sentiment-aware text preprocessing, it uncovers latent thematic structures, emotional tone distributions, and brand-specific conversational patterns. The analysis reveals nuanced differences in customer perception, loyalty drivers, and experiential expectations, offering actionable insights for strategic marketing, brand positioning, and customer engagement optimization within the competitive apparel sector.
This repository presents a **comparative social media analytics study** examining public perception, engagement patterns, and influencer dynamics for **Adidas** and **Lululemon** on Twitter.  
The analysis applies a structured analytics pipeline combining **text mining, sentiment analysis, topic modelling, time-series analysis, and network-based influencer identification**.

Rather than focusing solely on volume metrics, the project emphasises **brand positioning, emotional resonance, and community structure**, providing actionable insight into digital brand strategy.

---

## Project Objective

The objective of this project is to understand how two major activewear brands differ in their **digital engagement strategies and audience response** by answering:

- How do public sentiment and engagement differ between Adidas and Lululemon?
- What themes dominate brand conversations over time?
- How do campaign-driven spikes compare with community-driven engagement?
- Which users function as high-potential micro-influencers for each brand?

The analysis is designed to inform **brand strategy, influencer marketing, and audience targeting** decisions.

---

## Dataset Overview

- **Platform:** Twitter  
- **Time window:** 93 days (October 2021 – January 2022)  
- **Total tweets:** 44,380  
  - Adidas: 38,212 tweets  
  - Lululemon: 6,190 tweets  
- **Unique users:** ~33,000  
- **Features:**  
  - Tweet text  
  - Timestamps  
  - User metadata (followers, verification status)  
  - Engagement metrics (retweets, favourites)  
  - User location (self-reported)

This shared temporal window ensures **fair, controlled brand comparison**.

---

## Data Preprocessing

A comprehensive preprocessing pipeline was implemented to ensure analytical validity:

- Removal of duplicate tweets by tweet ID
- Standardisation of timestamp formats
- Cleaning of tweet text:
  - lowercasing
  - removal of URLs, mentions, emojis, and stopwords
  - lemmatisation using NLP libraries
- Creation of a `clean_text` field for downstream NLP tasks
- Imputation of missing user location values as `"Unknown"`
- Normalisation of geographic labels for location analysis

Over 8,000 tweets became empty after cleaning due to non-informative content; these were retained to preserve temporal consistency across analyses.

---

## Exploratory Data Analysis

### Tweet Activity and Engagement
- Adidas demonstrated substantially higher tweet volume and daily activity
- Adidas showed pronounced engagement spikes linked to campaigns and collaborations
- Lululemon exhibited lower volume but more consistent posting behaviour

### User Characteristics
- Verified users contributed a significantly larger share of Adidas-related tweets
- Adidas tweets contained more hashtags and mentions, indicating campaign amplification
- Lululemon tweets were longer on average, suggesting more narrative-driven communication

---

## Sentiment Analysis

Sentiment analysis was performed using **VADER**, selected for its effectiveness on short, informal social media text.

Tweets were classified as:
- Positive (≥ 0.05)
- Neutral (between −0.05 and 0.05)
- Negative (≤ −0.05)

### Key Findings
- Overall sentiment was predominantly positive (~47%)
- Lululemon exhibited slightly higher positive sentiment but also higher negativity
- Adidas sentiment fluctuated sharply over time, reflecting event-driven engagement
- Lululemon sentiment remained more stable, indicating sustained emotional connection

This highlights two contrasting strategies:
- **Adidas:** campaign-led emotional spikes  
- **Lululemon:** steady, values-driven engagement

---

## Topic Modelling

Topic modelling was conducted to uncover latent themes in brand conversations.

### Methodology
- Vectorisation using `CountVectorizer`
- Models tested: LDA, NMF, TF-IDF + KMeans
- **LDA** selected based on coherence and interpretability
- Optimal topics:
  - Adidas: 5 topics
  - Lululemon: 4 topics

### Adidas Themes
- Product launches and limited editions
- Athlete collaborations
- Sweepstakes and cross-brand promotions
- Sports event tie-ins
- Innovation and exclusivity

### Lululemon Themes
- Wellness and yoga advocacy
- Mental health initiatives
- Sustainability and climate activism
- Community-focused lifestyle messaging

Topic trends over time revealed **short-lived campaign peaks for Adidas** and **sustained thematic engagement for Lululemon**.

---

## Network Analysis and Micro-Influencer Identification

A mention-based network was constructed for each brand:

- Nodes: Twitter users  
- Edges: user mentions  

### Metrics Used
- In-degree centrality
- Betweenness centrality
- Closeness centrality
- Follower count
- Engagement rate
- Sentiment alignment

All metrics were normalised and combined into a **composite influencer score**.

### Recommended Micro-Influencers
- **Adidas:** @NicholasFerroni  
  - Moderate reach, balanced engagement, structurally central
- **Lululemon:** @Elamite  
  - High engagement rate, strong positive sentiment, community resonance

These users demonstrate **high influence without celebrity-scale reach**, making them suitable for targeted influencer partnerships.

---

## Key Insights

- Adidas excels at generating **high-impact, campaign-driven engagement**
- Lululemon builds **consistent, emotionally resonant communities**
- Campaign virality and sustained advocacy represent two distinct but effective branding models
- Micro-influencers offer scalable, authentic amplification opportunities for both brands

---

## Business Recommendations

- Leverage micro-influencers during campaign peaks to sustain momentum
- Balance short-term promotional bursts with long-term narrative engagement
- Expand influencer-driven content beyond product launches
- Continuously monitor sentiment shifts to manage reputational risk
- Extend analysis to additional platforms and international markets

---

## Tools and Technologies

- **Python**: data processing and analysis  
- **Pandas / NumPy**: data manipulation  
- **NLTK / spaCy**: text preprocessing  
- **VADER**: sentiment analysis  
- **Scikit-learn**: topic modelling  
- **NetworkX**: network analysis  
- **Matplotlib / Seaborn**: visualisation  
_This project exemplifies the power of unstructured data transformation into actionable brand intelligence, delivering measurable insight into consumer sentiment, product perception, and competitive positioning._
