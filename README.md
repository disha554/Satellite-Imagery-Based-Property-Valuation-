# Satellite-Imagery-Based-Property-Valuation-

This project predicts **house prices** by combining **traditional housing data** with **satellite images** of the surrounding neighborhood.  
The idea is simple: *a home’s value depends not just on its size, but also on where it is and what surrounds it.*

By using satellite imagery, the model captures visual cues like greenery, roads, water bodies, and urban density—things that aren’t fully represented in tabular data.
https://drive.google.com/drive/folders/1-1MvZ4wETSjtYwpgcgWT_RWtXhiY8wgS?usp=drive_link

## What This Project Does

- Predicts property prices using a **multimodal model**
- Fetches satellite images using latitude & longitude
- Extracts visual features from images using **CNNs**
- Combines image features with tabular housing data
- Compares tabular-only models with image-based and fusion models
- Generates final predictions for unseen test data


##  How It Works (Workflow)

### 1. Satellite Image Collection  
Satellite images are fetched using the **ESRI World Imagery API** based on each property’s coordinates and saved using the property ID.

### 2. Data Cleaning & EDA  
Missing images are removed, prices are log-transformed, and both tabular and geospatial patterns are explored.

### 3. Image Feature Engineering  
From satellite images, we estimate:
- **Green cover** (vegetation)
- **Urban density** (buildings/roads)
- **Water presence**

### 4. CNN Feature Extraction  
A pretrained **ResNet-18** model is used to extract deep visual embeddings that capture neighborhood context.

### 5. Fusion Modeling  
Tabular features, engineered image features, and CNN embeddings are combined and used to train regression models such as Gradient Boosting and XGBoost.

## Results

- Tabular-only models provide a strong baseline
- **Fusion models perform best**, achieving **R² ≈ 0.89**
- Satellite imagery clearly improves valuation accuracy


##  Tech Stack

- **Python, Pandas, NumPy**
- **PyTorch (ResNet-18)**
- **Scikit-learn, XGBoost**
- **Matplotlib, Seaborn**
- **ESRI World Imagery**


## Output Format

Final predictions are saved in a CSV file with the format in predictions named file
Prediction file cannot be directly updated because of large file size
hence drive link given here:https://drive.google.com/file/d/1Asw9F8EiQtt06u5hX9Eozt7kfvDVq9HB/view?usp=sharing




