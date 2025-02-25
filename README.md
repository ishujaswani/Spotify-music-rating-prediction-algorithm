# 🎵 Spotify Music Rating Prediction Algorithm 🎵

![Spotify Music Analysis](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTQ2bDVrYmkydzNnYnZwZzBhdXZnczVrNGZzaGhzZTlpbWdrdnhmMCZlcD12MV9naWZzX3NlYXJjaCZjdD1n/EFGXDUBXcUd131C0CR/giphy.gif)

## 🚀 Overview
This repository contains the code and analysis for **Spotify's Predictive Analytics Competition** on Kaggle. The goal of this project is to **predict song ratings** using multiple parameters such as artist, genre, quality, and tempo of the music.

## 📊 Dataset
The dataset consists of various attributes of songs, including:
- 🎼 **Genres** (One-hot encoded top 10 genres)
- 🎚️ **Tempo**
- 🔥 **Quality**
- 🎤 **Artist Information**
- ⭐ **Ratings (Target Variable)**

### 🛠️ Data Preprocessing
✅ Removed missing values (~1% of data)  
✅ Expanded the **genres column** into individual categories  
✅ Dropped non-informative columns (e.g., performers)  

## 📉 Methodology
The project follows a structured **machine learning pipeline**:

1️⃣ **Data Wrangling & Cleaning** 🧼  
   - Removed missing values  
   - One-hot encoded genres  
   - Dropped non-informative columns  

2️⃣ **Data Visualization** 📊  
   - Used `ggplot` and `ggcorplot` to visualize feature relationships  

3️⃣ **Model Training & Evaluation** 🤖  
   - Applied **23 different regression models**  
   - Selected **Random Forest (Ranger Package)** as the best model with the lowest RMSE  
   - Hyperparameter tuning for **optimal performance**  

## 🔥 Model Performance

| 🏆 Model                   | 🎯 RMSE (Train) | 🎯 RMSE (Test) |
|----------------------------|---------------|---------------|
| 📏 Regression             | 15.2378       | 15.2145       |
| 🏹 Lasso                  | 15.3012       | 15.2769       |
| 🌳 Decision Tree         | 15.7629       | 15.7159       |
| 🌲 **Random Forest (Ranger)** | **6.68**  | **14.87**  |
| 🛠️ Tuned RF (Pro Max)   | **10.79**  | **14.85**  |
| 🚀 XGBoost               | 13.80         | 15.09         |

🏅 **Best-performing model:** **Tuned Random Forest (Ranger)** with an RMSE of **14.85** on the test set.

## 🔑 Key Takeaways
💡 **Feature Engineering Matters**: Properly encoding categorical variables and selecting key features significantly improved model performance.  
💡 **Hyperparameter Tuning is Essential**: Adjusting parameters like the number of trees, `mtry`, and `min-node-size` **reduced RMSE**.  
💡 **Computational Limitations**: Some models took **hours** to run. Using **PCA or shrinkage models** could optimize computation.  

## 📁 Files in the Repository
📜 `PAC_ishu.Rmd` - R Markdown file with full analysis and implementation  
📂 `scoringData.csv` - Dataset used for predictions  
📑 `PAC.pdf` - Report documenting project methodology and results  
📄 `Spotify PAC.pdf` - Summary document on the competition  
📜 `LICENSE` - License for this project  
📘 `README.md` - Project documentation  

## 📜 License
This project is licensed under the **MIT License**. See `LICENSE` for more details.

## 👤 Author
**Ishu Jaswani**  
🎓 **Master’s in Analytics, Columbia University**  

📧 Contact: [ij2243@columbia.edu](mailto:ij2243@columbia.edu)  

---
