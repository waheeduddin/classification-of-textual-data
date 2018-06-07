# classification-of-textual-data
a hackathon experience
Content collected by the customer support team of T-mobile networks was analyzed. there were two challenges:
1. identify which cases were priority cases
2. which cases should be directed to which department of the support staff.
I worked on the classification task and used Support Vector Classifier to identify which cases can be a priority. the model was not very successful as the data was not balanced. Also I was not able to integrate a german language model that could help with the analysis of the text and so in the classification.
# data fields:
SichterGruppe: customer channel from where the customer data was collected
SichterName: The team at the T-mobile support staf that should handle this question.
kind: A number ranging from 1-4. it is an encoding of 4 actions such as whether the question is a new question, a reply by staff, a reply by the original user, a reply by any other user.
Datetime: datetime
Content: the content of the question and answers
URL: URL
Tag: A binary variable that suggests wethere the question is a non-priority or a priority case.
some other anonymous and self explanatory fields.
# reuslts
The SVC model performed to an average F1 score of 0.49. the gradient boosting did not fair any better as well.

# files
data_prep.ipynb: cleans some text in the contents and puts content, tag, and SichterName in three different pickle Files
SVC and xgboost Classififcation: using the models
documents.pl, labels.pl,tags.pl: pickle files that contain prepared data of almost 70% of the data provided in hackathon.
documents_test.pl, labels_test.pl: pickle files that contain prepared data of sample data file.
stopwords-de.txt,stopwords-de-wo-n.txt: some stopwords in german language
sample_with_header.csv: sample data

