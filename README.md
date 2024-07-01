# IPL Win Percentage Predictor

This project predicts the win percentage of an IPL team based on given match details such as batting team, bowling team, city, target score, current score, wickets out, and overs completed. It uses a machine learning model trained on IPL match data to provide real-time predictions.

## Overview

The IPL Win Percentage Predictor uses a trained machine learning pipeline to estimate the probability of a team winning based on current match statistics. The model considers various factors including the batting team, bowling team, match location, target score, current score, number of overs completed, and wickets out.

## Setup

To run this project locally, follow these steps:

1. ### Clone the Repository

```sh
git clone https://github.com/YOUR_USERNAME/IPL_win_predictor.git
cd IPL_win_predictor
```





2.  ### Create and Activate a Virtual Environment 
	Using venv (for Python 3.x) 
	#### Create a virtual environment 
	```bash
	 # Create a virtual environment named 'venv'
	  python3 -m venv venv
	  ```
    ####  Activate the Virtual Environment 
    ##### On Windows 
    ```bash 
    .\env\Scripts\activate
    ```
    ##### on macOS
     ```bash
      source env/bin/activate
      ```
3. ### Install dependencies

    Ensure you have Python 3.x installed along with the necessary libraries. Install them using:

    ```bash
    pip install pandas nltk scikit-learn
    ```

    You also need to download NLTK data:

    ```bash
	python -m nltk.downloader wordnet
	```

4.  ### Download the dataset

    -   Download the IPL Dataset from [Kaggle](https://www.kaggle.com/datasets/ramjidoolla/ipl-data-set?resource=download&select=deliveries.csv).
    -   Place the `deliveries.csv` and `matches.csv` files in a directory accessible to your Python environment.
5.  ### Run the preprocessing script

    Execute the model builder script (`IPL ML train.ipynb` or similar) in Google Colab or Jupyter notebook
    This script cleans the data, extracts relevant features, applies lemmatization, and computes TF-IDF vectors .

6.  ### Run the prediction system:

    Start the Streamlit application:

    ```bash
	streamlit run app.py
	```

    Open a web browser and navigate to `http://localhost:8501` to access the prediction system.

## Usage

-  **Select the Batting Team:** Choose the batting team from the dropdown menu.
-  **Select the Bowling Team:** Choose the bowling team from the dropdown menu.
-  **Select the Host City:** Choose the city where the match is being played.
-  **Enter the Target Score:** Input the target score for the batting team.
-  **Enter the Current Score:** Input the current score of the batting team.
-  **Enter the Overs Completed:** Input the number of overs completed.
-  **Enter the Wickets Out:** Input the number of wickets out.
-  **Predict Probability:** Click the button to view the predicted win percentage for both teams.
