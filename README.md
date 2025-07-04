# 🚗 AutoScout24 Smart Car Price Estimator & Dynamic Scraper

A professional-grade, dual-purpose application that combines:

- 📊 **Dynamic scraping** from AutoScout24 for real-time car listing extraction
- 🧠 **Machine learning-based price prediction** using structured model-based training

Built with Python, Selenium, Streamlit, and XGBoost.

---

## 🎯 Project Goals

- Efficiently **scrape structured vehicle listing data** from AutoScout24
- Enable **real-time user prediction** of car prices based on mileage, fuel type, gearbox, and power
- Serve as a scalable **assistant module** for second-hand car marketplaces or analytics platforms

---

## ✨ Features

### 🔍 Intelligent Web Scraping
- Filter by brand, model, fuel type, gearbox, mileage, and power
- Dynamically scrape matching listings from AutoScout24
- View listings in card-based format with export to CSV

### 💡 Smart Price Estimation
- Predict car prices using a model trained on the scraped dataset
- Brand-model specific training logic for more localized estimations
- Displays result in a modern Streamlit interface with metric widgets

### 🧪 Data Cleaning & Model Logic
- Cleans numeric data (price, power, mileage)
- Filters listings outside the defined valid ranges
- Uses OneHotEncoding and XGBoostRegressor inside an sklearn pipeline

---

## 🖥️ Interface Overview


# 🎯 **Ask to The Model** 
> Prediction Workflow
![Prediction Flow](images/predictor.gif)


# 🔍 **Search Car Data**

> Main Without Filtration
![filters](images/ss1.png) 

> Sidebad With Filtration
![filters](images/ss2.png) 

> Program's Look While Fetching Data
![filters](images/ss3.png) 

> Fetched Data With Detailed Look
![filters](images/ss4.png) 

> After Fetching The Data Download it
 ![filters](images/ss5.png) 

--- |


## 🚀 Installation

### 1. Clone the repository
```bash
> git clone https://github.com/BurakCANKURT/autoscout24-smart-estimator.git
> cd autoscout24-smart-estimator/autoscout24-smart-estimator

### 2. Install dependencies
> pip install -r requirements.txt


### 📦 Dataset
Due to GitHub’s file size limitation, the full dataset is included as a compressed .rar file:

autoscout24.rar

### 🔓 How to Use
Extract the file using any archive tool (e.g., WinRAR, 7-Zip, macOS Archive Utility).

Place the extracted autoscout24.csv file in the root directory of the project.

Then you can run the app as usual:

> streamlit run Main.py



📂 Project Structure
├── Main.py                      # Streamlit interface, ML model logic
├── OnlineData.py                # Web scraping logic for live data
├── OnlineAutoscout24.py         # Detailed scraping handler
├── ScrapElements.py             # UI element definitions (brands, filters)
├── KFoldTargetEncoderWrapper.py# (Optional) advanced encoding module
├── autoscout24.rar              # Cleaned and preprocessed base dataset / It should be here after extracting the .rar
├── requirements.txt             # Project dependencies
├── README.md                    # Project documentation
└── images/                      # Visual assets (screenshots)


⚠️ Notes on Model Design
Models are trained on-the-fly using filtered data (per brand or brand-model)

If sufficient brand-model data is not available, the model falls back to brand-only data

Prediction model uses OneHotEncoding and an XGBoost regressor (no external ML API required)


📦 Output
Feature	    Format
Prediction	💶 Estimated Euro price
Export	    📄 CSV File (filtered listings)
Deployment	🖥️ Streamlit UI



🧠 Tech Stack
├──Python 3.8+
├──Streamlit
├──Selenium
├──Pandas
├──XGBoost
├──Scikit-learn
└──Category Encoders



🤝 Contributions
Pull requests are welcome. For major changes, please open an issue first to discuss.

