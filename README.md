# Multimodal Hate Profiling on Instagram

**Repository for the paper:**  
📄 *Profiling Public Instagram Accounts with a Multimodal Vector for Hate Exposure Analysis*  
👨‍🔬 Asier Gonzalez-Santocildes, Iker Pastor López, Marta Gorraiz-Bengoechea, Pablo Garcia Bringas  
📍 Presented at HAIS 2025

---

## 📌 Overview

This repository provides the code, data structure, and documentation for a fully automated pipeline that collects and models public Instagram data to quantify **hate exposure and dissemination** across public influencer profiles.  

We introduce a **24-dimensional multimodal vector** per post that integrates sentiment, visual affect, facial demographics, and engagement metrics, enabling scalable analysis of public Instagram profiles without violating platform terms or compromising user privacy.

---

## 🧰 What’s Inside

### 🔍 Data Collection Pipeline
- Headless **Selenium crawler** with realistic delays and limits
- Scraping of captions, images, and full comment threads (public content only)
- SHA-256 anonymization of all identifiers (usernames, avatars, links)

### 🧠 Feature Extraction
- **Text:** Polarity and subjectivity (TextBlob), emoji treatment
- **Images:** Facial detection (RetinaFace), emotion + demographic logits (DeepFace)
- **Engagement:** Likes/comments, post timing, presence of text

### 📊 Vector & Modeling
- 24-dim feature vector per post
- CSV export format
- Profile-level aggregation for six domains: politics, news, fashion, fitness, gaming, sports
- Session simulation module for predicting exposure using topic mixes

### 📈 Evaluation Tools
- Hate score benchmarks per domain
- Session-level prediction vs. observed sentiment
- Simple linear blend model for estimating feed hostility

---

## 🔐 Ethics & Privacy

- All content comes from **public profiles**
- Strict **anonymization**: no usernames, URLs, or raw comments stored post-processing
- Fulfills GDPR principles of **data minimization** and ethical research conduct
- Approved by the University of Deusto’s Ethics Committee

---

## 📁 Coming Soon

- 📂 `crawler/` – Selenium scripts + rate limiter  
- 📂 `processing/` – Feature extractors (image/text)  
- 📂 `vectors/` – Example data and post-level vectors (anonymized)  
- 📂 `analysis/` – Session simulation notebooks and hate scoring  
- 📄 `vector_schema.csv` – Full list of 24 vector dimensions  
- 📄 `ethics_statement.md` – Data protection and methodology approval summary

---

## 📚 Citation

If you use this work, please cite it as:
