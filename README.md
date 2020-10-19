# Goal
Create an algorithm in order to classify the intent of a user query in a chatbot.
# Data Exploration
Before diving into training machine learning models, I should look at some examples
first and the number of question in each intent and scenario.
I decided to join the scenario and intent class in order rto have more information
once I will create my model.
I will remove missing values in “question” column, and add a column encoding
the product as an integer because categorical variables are often better
represented by integers than strings.
# Imbalanced Classes
I see that the number of questions per scenario_intent is imbalanced. So, I decided
to reduce randomly the numbers of the majority class and later to apply oversample
to the train data.
# Text Representation
The classifiers and learning algorithms can not directly process the text documents
in their original form, as most of them expect numerical feature vectors with a fixed
size rather than the raw text documents with variable length. Therefore, during the
preprocessing step, the texts are converted to a more manageable representation.
I applied some normalization like stemmer, tokenization, to have a better
interpretation of the data.
# Model
I devided tha data into train and valuation and I create an CNN with some
normalization(Drop 0,5) to avoidoverfitting and I used Bidirectional LSTM because it
performs better for text classification.
# Conclusion
The model performance pretty well and it predicts pretty good the unseen data
