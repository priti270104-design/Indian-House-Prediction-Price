**🏠 Indian House Price Predictor AI**
An interactive, machine-learning-powered web dashboard built with Streamlit. This application predicts house prices across major Indian cities using a Random Forest Regressor trained on 12,000+ real estate records. It also features live currency conversion to provide valuations in both INR and USD.

**🚀 Description**
This project serves as a "Real-Time" valuation tool for the Indian real estate market. Unlike static calculators, this app uses a data-driven approach to understand how different variables like Location Tier, City, Furnishing, and Square Footage interact to determine a property's market value.

**Key Features**

**AI-Driven Predictions:** Uses a RandomForestRegressor to capture non-linear relationships between property features and prices.
**Live Forex Integration:** Connects to an external API to fetch the current USD/INR exchange rate every hour.
Dynamic Data Handling: Automatically processes categorical text data (like "Premium" localities or "Semi-Furnished" statuses) using One-Hot Encoding.
**Interactive UI:** Sidebar controls for user-friendly adjustments of area, bedrooms, and bathrooms.

**🛠️ Tech Stack**

**Frontend:** Streamlit (Python-based Web Framework)

**Machine Learning:** Scikit-learn (Random Forest Regressor)

**Data Manipulation:** Pandas

**API Integration:** Requests (for Live Currency Rates)

**📋 Installation & Setup**

Clone or Download this project to your local machine.
Ensure you have Python 3.9+ installed.
Install the required libraries:

**Bash**

pip install streamlit pandas scikit-learn requests
Place the dataset file (house_price_dataset_india_12k.csv) in the same directory as your Python script.

**Run the application:**
Bash
streamlit run your_filename.py
📊 How the Model Works
The application follows a standard Data Science pipeline to ensure accurate results:

**Preprocessing**: The app cleans the input data, removing unique IDs and target-leaking columns (like Price per Sqft).

**Encoding**: It uses One-Hot Encoding to transform text-based categories (City, Locality, Furnishing) into a binary format the AI can understand.

**Training**: A Random Forest model creates an "ensemble" of decision trees to find patterns in the 12,000 records.
Real-Time Conversion: Once a price is predicted in the base currency (INR), the app fetches the latest exchange rate from exchangerate-api.com to provide a global valuation.

**📁 Dataset Details**

The model is trained on house_price_dataset_india_12k.csv, which includes:
**City:** Mumbai, Delhi, Bangalore, Pune, Hyderabad, etc.

**Locality Tier:** Budget, Mid, Premium.

**BHK:** 1 to 5 Bedrooms.

**Area_sqft:** Total floor area.

**Furnishing:** Unfurnished, Semi-Furnished, Fully-Furnished.

**⚠️ Limitations**

Data Age: Predictions are as accurate as the records in the provided CSV file.
External Factors: The model does not account for hyper-local factors like specific street noise, proximity to specific high-end schools, or sudden local infrastructure changes unless represented in the "Locality Tier."
