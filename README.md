~ cognitive-decline-state-analysis ~
Predicts what percentage of a demographic group in a state reports cognitive decline from the state, topic, demographic, and year.


Originally, this project was coursework for an artificial intelligence and machine learning class. 

The program in this form lacks the dataset it is supposed to analyze, however, some 
aspects of the project are dependent on the type or amount of values inside a particular category.

The program takes a given dataset (CSV) and separates/stores a specified class from the dataset that relates to
cognitive mental decline. This speaks to the original purpose of the program, in the context of the dataset,
to clean and simplify data from the set, label and cluster that data, and then produce unsupervised clustering
of states that have similar values inside 4 defined categories (SCD rate, functional difficulties, 
needs daily help, talked to a doctor) and supervised predictions on, if given 5 values from 5 defined categories,
can the model guess the amount of the specified demographic reported cognitive decline.

The clustering algorithm used is K-means and in order to make predictions we use linear and random forest regression.


In absence of the original dataset, the output of the algorithm on said dataset has been placed below as an example
of what its functionality looks like.

(22182, 31)
dropped 8046 rows with no Data_Value
final shape: (14039, 28)
Topic    Functional difficulties associated with subjective cognitive decline or memory loss among older adults  ...  Talked with health care professional about subjective cognitive decline or memory loss
cluster                                                                                                          ...                                                                                        
0                                                      0.4                                                       ...                                                0.4                                     
1                                                      0.3                                                       ...                                                0.4                                     
2                                                      0.7                                                       ...                                                0.6                                     

[3 rows x 4 columns]
cluster 0 -> ['Alabama', 'Arizona', 'Arkansas', 'District of Columbia', 'Florida', 'Georgia']
cluster 1 -> ['Alaska', 'California', 'Colorado', 'Connecticut', 'Delaware', 'Hawaii']
cluster 2 -> ['Puerto Rico']
linear regression -> r2: 0.008 mae: 0.14
random forest -> r2: 0.806 mae: 0.05
Topic_enc              0.682221
Stratification2_enc    0.124758
LocationDesc_enc       0.086878
Stratification1_enc    0.053385
YearStart              0.052757
dtype: float64
