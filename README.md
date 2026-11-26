# email
email classifier
Email_Classifier.ipynb is a Python Jupyter Notebook that builds a simple machine-learning email spam classifier. Its purpose is to take an email message as input and predict whether the message is SPAM or NOT SPAM.

What the notebook does
1. Imports machine-learning tools
   - CountVectorizer converts email text into numerical word-count features.
   - train_test_split divides the dataset into training and testing data.
   - MultinomialNB provides the Naive Bayes classification model.

2. Creates a small email dataset
   - The notebook contains 20 example emails.
   - The first 10 are promotional/scam-style messages such as prize claims, discounts, lottery winnings, and money-making offers.
   - The remaining 10 are normal academic/work-related messages such as meeting reminders, lecture notes, assignments, seminars, and examination information.

3. Labels the emails
   - 1 represents spam.
   - 0 represents not spam.
   - Therefore, the dataset contains 10 spam and 10 non-spam examples.

4. Splits the data
   - The dataset is divided into 70% training data and 30% testing data.
   - random_state=42 makes the split reproducible.
   - stratify=labels preserves the spam/non-spam distribution between the two sets.

5. Converts text into numerical features
   - CountVectorizer learns the vocabulary from the training emails.
   - Each email is represented by counts of the words it contains.
   - The same vectorizer is then used to transform the test emails.

6. Trains a Naive Bayes classifier
   - A MultinomialNB model is trained using the vectorized training emails.
   - The notebook reports an accuracy of approximately 83.33% on the test set.

7. Provides an interactive classifier
   - The notebook uses ipywidgets to create a text box where a user can enter an email.
   - The trained model immediately predicts:
     - SPAM, or
     - NOT SPAM
   - It also displays the model's estimated confidence for each class.

Overall workflow
Email text → Word-count vectorization → Naive Bayes model → Spam/Not Spam prediction → Confidence score
