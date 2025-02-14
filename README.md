# Learning-style-aware-abstractive-text-summarization
 

## Overview  
People learn in different ways—some prefer reading, others understand better through audio narration, and some grasp concepts visually.  
This project enhances text summarization by integrating personalized learning styles using Large Language Models (LLMs).  

By fine-tuning Pegasus (`google/pegasus-large`) on the WikiHow dataset, we generate custom summaries that adapt to different learning preferences:  

- **Auditory Learners** → Summaries are converted into speech using gTTS (Google Text-to-Speech).  
- **Visual Learners** → Keywords are extracted using YAKE, and relevant images are generated using Stable Diffusion 2.  

This approach makes learning more engaging and accessible, improving knowledge retention and user experience.  

---

## **Key Objectives**  
✔ Develop a fine-tuned summarization model using Pegasus for improved abstractive text generation.  
✔ Enhance accessibility by integrating Text-to-Speech (gTTS) and Image Generation (Stable Diffusion 2).  
✔ Evaluate performance using ROUGE metrics, optimizing coherence and factual accuracy.  

---

## **Methodology**  

### **◆ Dataset**  
- **WikiHow Dataset (204,004 article-summary pairs)** – Collected via **Scrapy**, covering procedural tasks across multiple domains.  
- **Note:** This dataset is not primary data; it was originally extracted from WikiHow articles and used as an existing resource for fine-tuning the summarization model.  

### **◆ Model Development**  
#### **1. Fine-Tuning Pegasus:**  
- Used Transformers (Hugging Face) for model training.  
- Optimized training using Trainer API and PyTorch.  

#### **2. Personalized Summarization Features:**  
- **Text-to-Speech (gTTS):** Converts summaries into audio format.  
- **Visual Summarization:**  
  - Extracts keywords using YAKE.  
  - Generates relevant images using Stable Diffusion 2.  

#### **3. Evaluation:**  
- Assessed using ROUGE-1, ROUGE-2, and ROUGE-L.  
- Achieved ROUGE-1 F-measure: 31.25.  

---

## **Tools & Technologies**  

| Category            | Technologies Used |
|--------------------|----------------|
| **Programming Language** | Python |
| **Pretrained Model** | Pegasus (`google/pegasus-large`) |
| **Deep Learning Frameworks** | Hugging Face Transformers, PyTorch |
| **Data Processing** | Pandas, NumPy |
| **Model Training** | Trainer API, Torch |
| **Evaluation Metrics** | ROUGE (datasets, rouge_score) |
| **Personalization Features** | gTTS (Text-to-Speech), YAKE (Keyword Extraction), Stable Diffusion 2 (Image Generation) |

---

## **Expected Outcomes**  
✔ Improved abstractive summarization.  
✔ Personalized user experience through audio and visual representations.  
✔ Enhanced accessibility for different learning styles.  

---

## **Future Work**  
- Extend the model to support multi-document summarization.  
- Explore transformer-based keyword extraction instead of YAKE.  
- Optimize image-text alignment for better visual summaries.  

---
 
