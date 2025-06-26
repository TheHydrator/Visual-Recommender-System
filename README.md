# Visual Recommender System for Amazon Pantry

An intelligent, multimodal recommendation engine designed to enhance product discovery in online retail. This system allows users to either **upload an image** or **enter a product name**, and it returns pantry items that are visually or semantically similar — making online shopping more intuitive and engaging.

---

## Project Overview

This system is **built entirely from scratch** using deep learning, without relying on any pre-trained models. It combines the power of computer vision and natural language processing to create a flexible, dual-pathway recommender system. Despite lower raw accuracy due to custom implementation, the performance demonstrates solid conceptual learning and real-world applicability.

By understanding **what a product looks like** and **what it’s called**, the system intelligently recommends relevant alternatives — even when little to no user data is available.

---

## Dataset

The system uses a curated subset of the [Amazon Product Dataset](https://nijianmo.github.io/amazon/index.html) (Pantry category), featuring:

- Product images  
- Titles and descriptions  
- Star ratings and purchase frequencies  
- Co-purchase patterns  

After preprocessing, ~1300 high-quality items remain for training and evaluation.

---

## Architecture Summary

### Visual Encoder (Custom Vision Transformer)
- Learns visual features from product images  
- Understands packaging, structure, and layout  
- Encodes images into high-dimensional embeddings for comparison  

### Text Encoder (Transformer-Based)
- Processes product titles and descriptions  
- Captures semantic similarities and context  
- Maps text into a shared embedding space for flexible retrieval  

### Multimodal Integration
- Both encoders map data into a shared latent space  
- Enables input via either modality (image or text)  
- Similarity is computed using Cosine Similarity for efficient retrieval  

---

##  Key Features

 **From-scratch implementation** of core ML models  
 **No user history required** — great for cold-start problems  
 **Handles both image and text inputs**  
 **Reusable embeddings** for fast, real-time recommendation  
 **Modular design** — easy to extend and improve  

---

## Tools & Libraries

- Python, PyTorch, Torchvision  
- Pandas, NumPy, Scikit-learn  
- Matplotlib, Seaborn for visualization  
- Google Colab / Jupyter for experimentation  

---

## How It Works

- A user uploads a product image or types in a description.  
- The system encodes the input into a numeric vector.  
- It compares that vector to precomputed product embeddings.  
- The most similar items are retrieved and displayed as recommendations.  

**Example Use Cases:**
-  Upload a juice bottle → get similar beverages  
-  Type "oatmeal cereal" → get related pantry items  
-  Combines vision and language cues for better ranking  

---

##  Why It Stands Out

 **Complete custom architecture** — shows mastery of both vision and NLP modeling  
 **Improves shopping experience** with visual discovery  
 **Conceptual rigor** — implements contrastive learning, cosine similarity, and embedding reuse  
 **Qualitative validation** through semantic clustering and product similarity maps  

This is not just a proof of concept, but a **blueprint** for next-gen recommender systems that go beyond clicks and ratings to understand products like a human does.

---

##  Project Structure
NeuralNetworkProject/
├── Recommendation System.ipynb # Core notebook with model training & testing
├── best_image_text_matches.csv # Precomputed image-text match scores (images/ # Dataset of product images)
├── system_architecture/ multimodal_similarity_diagram.jpg # design of the project
└── README.md # You're here!


---

## Authors

Rohit Goutam Maity, Kunal Tamhane, Jaya Prakash Yadav Gorla, Preshita Soni, Rashi Jain  
🎓 CSC 578, DePaul University  
📅 June 2025

---

## Contact

For questions, suggestions, or collaboration, reach out to [rmaity@depaul.edu](mailto:rmaity@depaul.edu)

---

> **“We built this system like it thinks visually and reads semantically — just like humans do.”**


