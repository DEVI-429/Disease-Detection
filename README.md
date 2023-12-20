## Disease Detection and Identification based on Symptoms

# INTRODUCTION:

This project uses IR  methods to identify diseases by their symptoms.
Even someone with little medical background may easily operate the system, which can be helpful for early illness diagnosis and detection. They will gain a basic understanding of the disease's severity from this.

# DATASET USED:

We used 'Kaggle Health Analytics' dataset which contain following contents: 

Each tuple of our dataset consists of multiple coloumns and tuple size is equivalent to the number of unique diseases.

Diseases: List of Diseases and each disease has a row of symptoms, 1 is marked if the symptom is valid for the disease and 0 if otherwise

Symptoms: List of symptoms

*dis_sym_dataset_comb -> dataset generated by combining symptoms for each disease.*

*dis_sym_dataset_norm -> dataset which contains a single row for each diseases with the symptoms for that corresponding disease.*

*dis_symp_dict -> contains list of symptoms*

# How to run the project:

1. Install all the necessary requirements - **pip install -r requirements.txt**

2. To run the system - **python -m streamlit run TF_IDF_NN.py**

# COMPONENTS:
1. Index Component -
  It generally refers to the ordering of information, it reduces the documents to the informative terms in them

2. Search Component -
   We calculate the tf and idf values and assign the weights to the each document by creating vector.Then we calculate the similarity between query and each document by using cosine similarity ,based on that we rank the document and return the top relevant document.

3. Query expansion using Thesaurus -
   Using thesaurus we find all of the synonyms for each user symptom and adding them to the pre-processed symptom string.

4. Refine search based on co-occuring symptoms -
   For more accurate prediction we ask the user to select the co-occuring symptoms that he notice and refine the results.User can simply type 'no' to stop generating co-occuring symptoms and '-1' skip this step.

5. Capturing feedback and suggesting relevant documents -
   Relevance feedback is taken and the results are again filtered based on it.

6. Assessment Components (Precision,Recall,P-R curve,Mean Average Precision) -
    We calculate the Precison , Recall, MAP and plot P-R Curve.

# GROUP CONTRIBUTIONS:
1. Reddi Devi Vara Prasad - S20210010190

- Index component

- Search component

- Query Expansion using thesaurus

2. Praghna Kakani - S20210010101

- Refine Search based on co-occuring symptoms

- Capturing Feedback and giving Relevant Documents

- Assessment Components (Precision, Recall, P-R Curve, Mean Average Precision)

# Github link
https://github.com/Praghna2004/IR_Project