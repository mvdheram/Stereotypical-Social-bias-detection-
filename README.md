# Asseessing stereotypical social biases in text sequences using language models (Master Thesis)

**Datasets** 
  * Stereoset [1]
  * Social Bias Frames [2]
  * Crowspair [3]
 
**Problem type**
 * Multi-label classification 

**Labels**
 * Stereotype_category
   * Stereotype (Generalized social beliefs)
   * Anti-stereotype (Not a generalized social beliefs)
   * Unrelated (Not a stereotype)
 * Bias_type
   * Ethnicity 
   * Gender
   * Profession 
   * Religion 

**Experiments and comparitive analysis**:
 * Deep learning transformer based pre-language models using Transfer learning
   * Training process
     * Data preprocessing -> Language model fine-tuning -> Hyperparameter search -> Training -> Evaluation (test set)   
   * Language models tested
     * BERT [4]
     * RoBERTa [5]
     * GPT-2 [6]
     * XLNEt [7] 
   * Environment 
     * Google Colaboratory, NVIDIA Tesla T4 GPU
   * Libraries used:
     * Transformers
     * Ktrain
     * PyTorch lightening
     * RayTune (Hyper parameter search)       
 * Classical machine learning based models
    * Training process 
      * Data preprocessing -> Feature engineering -> Model definition -> Training -> Evaluation (test set)
    * Libraries used 
      * Keras
      * Scikit learn
    * Models with features    
      * Convolutional Neural Network with features
        * Flair word embeddings
        * Glove word embedding
        * Fasttext word embedding
    * Multinomial Naive Bayes, Decision tree, k-Nearest Neighbor, Random Forest, 
      * Bag of words 
      * Term Frequency-Inverse Document Frequency
    * Support Vector Machine 
      * Selected features 
    *  Bi-directional Long Short Term Memory with features
       * Random word embeddings   

**Evaluation Metrics** 
  * Sample based metrics 
    * Subset accuracy (Main metrics - Harsh measure)
    * Hamming loss
    * Hamming score
    * Precsion 
    * Recall
    * F-measure

**Results**  
  * Deep learning based tranformer based lanugage models 
     * RoBERTa - 81% (Subset accuracy)
     * BERT - 71% (Subset accuracy)
     * XLNET = 62% (Subset accuracy)
     * GPT-2 - 37% (Subset accuracy)  
  * Classical machine learning models
     * Decision Tree (Tf-idf) - 59% (Subset accuracy) 
     * Random Forest (Tf-idf) - 48% (Subset accuracy) 



  
  
  References :
  
  [1] : Stereoset: Measuring stereotypical bias in pretrained language models
  
  [2] : Social bias frames: Reasoning about social and power implications of language
  
  [3] : CrowS-Pairs: A Challenge Dataset for Measuring Social Biases in Masked Language Models
  
  [4] : BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
  
  [5] : Roberta: A robustly optimized bert pretraining approach
  
  [6] : Language Models are Unsupervised Multitask Learners
  
  [7] : Xlnet: Generalized autoregressive pretraining for language understanding
