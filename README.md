# ✈️ Flight Delay Prediction Using Big Data Pipeline

A scalable machine learning pipeline to predict airline flight delays using a large-scale dataset and distributed computing with PySpark on Google Cloud Platform.

---

## 🎯 Objective

This project aimed to build an end-to-end big data pipeline to process, clean, and analyze airline on-time performance data and to train predictive models for flight delay classification.

---

## 📚 Dataset

- **Source**: Bureau of Transportation Statistics (BTS)
- **Size**: 10+ GB of CSV data
- **Records**: Millions of flights from U.S. airports
- **Target Variable**: `IsDelayed` (1 = delayed, 0 = on-time)

---

## ⚙️ Technologies Used

- **PySpark** on **Google Cloud Dataproc**
- **Google Cloud Storage (GCS)**
- **MLlib** (Spark's ML library)
- **Pandas**, **Matplotlib**, **Seaborn** (for post-modeling visualization)
- **Google Colab** (for local EDA)

---

## 🔄 Pipeline Overview

1. **Data Ingestion**  
   - Uploaded CSV data to Google Cloud Storage (GCS)
   - Mounted GCS bucket in Dataproc for scalable processing

2. **Data Cleaning & Preprocessing**  
   - Dropped nulls, handled time fields, and created `IsDelayed` column
   - Selected relevant features like Carrier, DepartureTime, Distance

3. **Feature Engineering**  
   - Categorical encoding of carriers
   - Time-of-day transformation (early, mid-day, late)

4. **Modeling with MLlib**  
   - Trained classification models using Logistic Regression
   - Used `Pipeline`, `VectorAssembler`, `StandardScaler`

5. **Evaluation**  
   - ROC-AUC on test data: ~74%  
   - Model evaluated using BinaryClassificationEvaluator  
   - Future work includes hyperparameter tuning and model comparison

---

## 📁 Project Structure

flight-delay-prediction-bigdata/
├── bigdata_pipeline_notebook.ipynb # PySpark code for data prep, modeling, and evaluation
└── README.md # Project documentation

---

## 📌 Key Takeaways

- End-to-end ML pipelines can scale efficiently using PySpark and Google Cloud
- Logistic Regression worked well for sparse airline delay data
- Cloud integration helped manage 10GB+ data efficiently
- Feature engineering significantly impacted model performance

---

## 👤 Author

**Khushwant Khatri**  
📧 khushwant.khatri03@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/khushwantkhatri)

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
