# IR Assignment 2


### Q1. Image Feature Extraction
Using python’s torch library, significant transformations are applied to the images loaded from the dataset.  
Afterwards, using the pre-trained ResNet model, features of all images have been extracted.  
These features are stored in a dictionary where keys are the links to the images and their corresponding values are the features that have been extracted.  
All the data from the dictionary is dumped into a pickle file labelled image_features.pkl    


### Q2. Text Feature Extraction
In this part of the assignment the task was to process features of the textual data and compute all TF-IDF scores.  
Using python’s NLTK library preprocessing tasks such as lowercasing, stopword and punctuation removal and lemmatization were applied.  
Three functions are then implemented to calculate the TF-IDF scores from scratch.  
The scores are then stored in the pickle file tf_idf_scores.pkl

### Q3. Image Retrieval
For this part, we take all the features calculated from Q1 and then compare them with an image input by the user.  
The query is handled using a class called Query.  
The pipeline is as follows:    
- Take the input and download the image    
- Extract features from the input image    
- Compare these from the features of all images present in the dataset using cosine similarity as a measure.  
- Cosine similarity is calculated using torch library.    
- Results are then reverse sorted order (most similar to least similar).
<a/>
After this in a function to process the query, we use the above pipeline and show the desired output.

