# 01. Topic Modelling on User's Web Activities

![topic_modelling_process](https://github.com/jad-22/business_analytics/blob/main/projects/01_nlp_topic_modelling/01_topic_modelling_process.png)

**Note: Data provided by and code submitted to IPSOS are non-disclosable as per NDA**

### Data Source

Data is provided by IPSOS under Non-Disclosable Agreement.

### Credit

Credit to my team members: Irene Wang, Sonia Zhang, Anne-Fleur Hilbert, Li Zike, Ren Xinyao, Du Diqin, Julia Zhang

### Objectives

To retreive relevant topics from the web URLs that were visited by the users. This topics indicate the users' preferences, which can then further be used for customer segmentation and recommendation by IPSOS.

### Methodology

Since the dataset is relatively large (in the scale of millions of rows), we need to design the script logic to minimise runtime and make it scalable. 
One of the key logic we introduce, which was based on my experience in operational data analyst, was to "cache" the topics that 1) have previously been visited and that 2) are invalid or do not substantial content.
By caching these URLs and the topics modelled, we can potentially reduce the script runtime by approximately 20% based on our test data.

Moving on to the main bulk of the algorithm, we tested various algorithm and processes as follows:

1. Lemmatisation v.s. Stemming
   * Stemming: NLTK's porter stemmer and snowball stemmer
   * Lemmatisation: NLTK's wordnet lemmatiser and SpaCy's lemma 
2. N-gram model
   * uni-gram v.s. bi-gram v.s. tri-gram using gensim
3. Topic model algorithm
   * Latent Dirichlet Allocation: the most popular and widely used topic modelling algorithm, based on Bayesian probability
   * Latent Semantic Indexing: the predecessor to LDA, based on statistical single value decomposition
   * Non-negative Matrix Factorisation: similar to LSI but with non-negative constraint imposed

We then perform various benchmark to test the robustness and accuracy of our topics using the following methods:

1. Coherence score
2. Manual QC/QA
3. RazorText benchmark
