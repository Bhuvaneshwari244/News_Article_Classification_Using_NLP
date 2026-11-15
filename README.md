# News Article Classification Using NLP

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A machine learning project that automatically classifies news articles into four categories: **World**, **Sports**, **Business**, and **Sci/Tech** using Natural Language Processing (NLP) techniques.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Project Structure](#project-structure)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Project Overview

This project develops an automated NLP system that reads news headlines and descriptions to predict their category. News websites publish thousands of articles daily, and manual categorization is time-consuming and inconsistent. This machine learning solution streamlines the content organization process.

**Project Level:** Intermediate  
**Platform:** Jupyter Notebook  
**Problem Type:** Supervised Multi-class Text Classification  
**Target Classes:** 4 categories (World, Sports, Business, Sci/Tech)

## 💼 Business Problem

**How can we automatically classify a news article into World, Sports, Business, or Sci/Tech based on its text?**

### Expected Business Outcomes:
- ✅ Reduce manual article classification effort
- ✅ Organize news articles consistently
- ✅ Make searching and filtering articles easier
- ✅ Support faster content management
- ✅ Improve user experience by providing better content organization

## 📊 Dataset

### AG News Classification Dataset

- **Source:** [Hugging Face - AG News Dataset](https://huggingface.co/datasets/fancyzhx/ag_news)
- **Training samples:** 120,000 articles
- **Test samples:** 7,600 articles
- **Features:** News title and description
- **Target:** 4 balanced categories

### Category Distribution:
| Category | Label | Count (Train) |
|----------|-------|---------------|
| World    | 1     | 30,000        |
| Sports   | 2     | 30,000        |
| Business | 3     | 30,000        |
| Sci/Tech | 4     | 30,000        |

## 🔄 Project Workflow

1. **Business Problem Definition** → Understanding the classification need
2. **Objective Identification** → Multi-class text classification
3. **Data Collection** → Loading AG News dataset
4. **Exploratory Data Analysis (EDA)** → Understanding data patterns
5. **Feature Engineering** → Text preprocessing and transformation
6. **Data Splitting** → Train-test separation
7. **Text Preprocessing** → Cleaning and normalization
8. **Model Building** → Training multiple classifiers
9. **Model Evaluation** → Performance metrics analysis
10. **Hyperparameter Tuning** → Optimization
11. **Model Selection** → Choosing best performer
12. **Model Deployment** → Saving and loading pipeline
13. **Prediction & Monitoring** → Logging predictions

## 🛠️ Technologies Used

### Core Libraries:
- **Python 3.8+** - Programming language
- **Pandas & NumPy** - Data manipulation and numerical operations
- **Matplotlib & Seaborn** - Data visualization
- **Scikit-learn** - Machine learning algorithms and preprocessing
- **Joblib** - Model serialization and saving
- **Gradio** - Web interface for deployment
- **Hugging Face Datasets** - Dataset loading

### NLP Techniques:
- Text preprocessing (cleaning, normalization)
- TF-IDF vectorization
- Feature extraction
- Multi-class classification

## 🚀 Installation

### Prerequisites
Ensure you have Python 3.8 or higher installed on your system.

### Clone the Repository
```bash
git clone https://github.com/Bhuvaneshwari244/News_Article_Classification_Using_NLP.git
cd News_Article_Classification_Using_NLP
```

### Install Required Packages
```bash
pip install datasets pandas numpy matplotlib seaborn scikit-learn joblib gradio
```

### Alternative: Using requirements.txt
```bash
pip install -r requirements.txt
```

## 💻 Usage

### 1. Open Jupyter Notebook
```bash
jupyter notebook News_Article_Classification_Complete_Detailed.ipynb
```

### 2. Run All Cells
Execute cells sequentially to:
- Load and explore the dataset
- Perform EDA
- Train the classification model
- Evaluate performance
- Save the trained model

### 3. Make Predictions
```python
import joblib

# Load the trained model
model = joblib.load('artifacts/news_article_classifier.joblib')

# Predict category
article_text = "Apple announces new iPhone with advanced AI features"
prediction = model.predict([article_text])
print(f"Predicted Category: {prediction[0]}")
```

### 4. Using the Web Interface (if implemented)
```python
import gradio as gr

# Launch the Gradio interface
interface.launch()
```

## 📈 Model Performance

The project implements and compares multiple classification algorithms:

- **Logistic Regression**
- **Naive Bayes**
- **Support Vector Machine (SVM)**
- **Random Forest**
- **Gradient Boosting**

Performance metrics evaluated:
- ✅ Accuracy
- ✅ Precision
- ✅ Recall
- ✅ F1-Score
- ✅ Confusion Matrix

*(Specific accuracy metrics will be available after running the complete notebook)*

## 📁 Project Structure

```
News_Article_Classification_Using_NLP/
│
├── AG_News_Dataset/
│   ├── train.csv                    # Training dataset
│   └── test.csv                     # Test dataset
│
├── artifacts/
│   └── news_article_classifier.joblib  # Saved trained model
│
├── .ipynb_checkpoints/
│   └── News_Article_Classification_Complete_Detailed-checkpoint.ipynb
│
├── News_Article_Classification_Complete_Detailed.ipynb  # Main notebook
├── prediction_log.csv               # Prediction logging file
├── README.md                        # Project documentation
└── requirements.txt                 # Python dependencies (optional)
```

## 🎯 Results

The model successfully:
- ✅ Classifies news articles into 4 categories with high accuracy
- ✅ Processes text data efficiently using NLP techniques
- ✅ Provides consistent categorization across different news sources
- ✅ Logs predictions with timestamps for monitoring
- ✅ Deploys as a reusable pipeline saved with Joblib

### Sample Predictions:
```
Input: "NASA discovers new exoplanet in habitable zone"
Output: Sci/Tech

Input: "Stock market reaches all-time high amid economic recovery"
Output: Business

Input: "World Cup final attracts record viewership"
Output: Sports
```

## 🔮 Future Enhancements

- [ ] Implement deep learning models (LSTM, BERT, Transformers)
- [ ] Add real-time news article scraping
- [ ] Create REST API for production deployment
- [ ] Implement multi-language support
- [ ] Add more granular subcategories
- [ ] Deploy to cloud platforms (AWS, Azure, GCP)
- [ ] Create interactive dashboard for visualization
- [ ] Implement continuous learning pipeline
- [ ] Add confidence scores for predictions
- [ ] Integrate with news aggregation platforms

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Steps to Contribute:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Bhuvaneshwari**

- GitHub: [@Bhuvaneshwari244](https://github.com/Bhuvaneshwari244)
- Project Link: [News Article Classification Using NLP](https://github.com/Bhuvaneshwari244/News_Article_Classification_Using_NLP)

## 🙏 Acknowledgments

- AG News Dataset providers
- Hugging Face for dataset hosting
- Scikit-learn community
- Open-source NLP community

## 📧 Contact

For questions, suggestions, or collaboration opportunities, please open an issue on the GitHub repository.

---

⭐ If you found this project helpful, please consider giving it a star!
