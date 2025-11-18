# **📞 Telecom Churn Prediction Dashboard**

- This project is a reactive dashboard for predicting customer churn in a telecom dataset. 
- Users can explore data, filter by different customer features, and predict churn probabilities using a trained Logistic Regression model.

## **📁 Project Structure**

    churn_dashboard/

        data/ → Original dataset files

                - telecom_customer_churn.csv
                - telecom_data_dictionary.csv
                - telecom_zipcode_population.csv

        preprocessed data/ → Preprocessed dataset

                - processed_churn_dataset.csv

        models/ → Trained model and supporting files

                - churn_model.pkl
                - age_scaler.pkl
                - feature_columns.pkl

        src/ → Preprocessing and training scripts

                - preprocess.py
                - train.py

        app.py → Streamlit dashboard

        requirements.txt → Python dependencies

        README.md → Project details

## **⚙️ Dependencies**

This project uses the following Python packages:

- pandas

- numpy

- scikit-learn

- streamlit

- joblib

All dependencies are listed in the requirements.txt file.

## **🛠️ Setup Instructions**

1️⃣ Clone the repository

        git clone https://github.com/Faares7/Churn-Dashboard.git
        cd churn_dashboard  



2️⃣ Install dependencies

        pip install -r requirements.txt  


3️⃣ Preprocessing the Dataset 🧹 

        - If you need to preprocess the original dataset:
        python src/preprocess.py  
        - This will create processed_churn_dataset.csv in preprocessed data/.

4️⃣ Train the Model 📊 

        python src/train.py  
        - This will train a Logistic Regression model using the preprocessed dataset.

        Saved files:

            1. models/churn_model.pkl → Trained model
            2. models/age_scaler.pkl → Age scaler
            3. models/feature_columns.pkl → Feature columns list

5️⃣ Run the Dashboard 🚀 

        streamlit run app.py  
        - Open your browser at the URL provided (usually http://localhost:8501)

        1. Dashboard Page: Explore data with filters

        2. Predict Churn Page: Enter customer information to get churn probability

## **💡 Notes**

- Only numeric and one-hot encoded columns are used for model training.

- Original City and Contract columns are preserved for dashboard filters.

- Churn probability is calculated using a Logistic Regression model trained on processed data.
