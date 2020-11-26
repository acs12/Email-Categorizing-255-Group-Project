# Email-Categorizing-255-Group-Project



- There are two 2 seperate jupyter Notebooks to run the project there no extra requirements except

1. Email Ham Spam Filter

    - About Notebook
  
    - Importing the data

      - The dataset is split into two separate folders - Ham and Spam. In each folder there are various subfolders. A process is developed to read each email into their respective categories.

    - Organizing the data

      - Both Ham and Spam files is combined into a pandas dataframe which will allow ease of use in later stages.
    
   - Cleaning the data

      - Regular expressions functions clears the email messages of html tags and other non alphanumeric noise. A lemmatizer is applied to the emails in order to reduce words to their base format, for example: 'walking' will be converted to 'walk'.

   - Creating a train and test set

      - The dataset is then divided into a training set and test set for use in model training. The models will be trained on the training set, and validated using the test data as 'unseen' data.

   - Feature Extraxtion with TfidfVectorizer

      - The dataset is then analysed for word frequencies. This converts the data into a numerical format which is required for the machine learning algorithms.

   - Model Training and Evaluation

      - Model training begins at this step. Multiomial Naive Bayes, K Nearest Neighbour, Decision Tree, Random Forest and Logisitic Regression models will be trained in the training data, then validated on the test data.

    - Model Selection and Fine Tuning

      - The best perfoming model from the previous training segment is tunned via Gridsearch to find its optimum parameters.

    - Before runnning this script:

      Download the Enron Email Ham and Spam Dataset: https://drive.google.com/file/d/1c0Zbp4tSRsRPcxbswYDCYzmE66GRGv_L/view?usp=sharing

      Extract the files. You will see two folders: Ham Unprocessed and Spam Unprocessed

      In the python script, set these directories as:

      hamdir = r'....\Ham Unprocessed' (remove 'r' for MacOS)
      spamdir = r'.....\Spam Unprocessed (remove 'r' for MacOS)

      After setting the directories run the python notebook

2. Email Categorization

  - About Notebook

    -  Categorize Email for user defined folders like resumes, study, etc.
  
    -  Import, Organize, Clean Data 
                    
        - Import, organize and filter the data for each employee by removing unwanted folders and just keeping X-Folders i.e. user defined folders. Data is then visualized using histograms and other graphs to see the size of data we are dealing with.
    - Preprocessing and Feature Extraction 
      - After that form an Assemble bag for the words by tokenizing them and removing stop words.
    - Splitting Data and Evaluating Model 
      - Form a logistic regression model for the model each employee by splitting the data into train test into 80% train and 20% test and then find the accuracy for each trained model.

    - Download the Enron Email Dataset: https://www.kaggle.com/wcukierski/enron-email-dataset
  
    - Install wordcloud

          !pip install wordcloud

    - In the python script, set these directories as:

          filepath = r"...\emails.csv"
    
    - After setting the directories run the python notebook.
    
    **Note** : We have uploaded a pickle file for a trained model for an employee with test data.
    **Note** : employee_predicted_results.zip are the predicted results for email categorization for each employee's personalized folder
