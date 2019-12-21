# Detection of Plagiarism

In this study, the objective is to find possible instances of plagiarism in a given dataset of documents. The dataset consists of k = {10,100,1000,10000} documents. In each set of documents, there are some pairs which are tagged as instances of plagiarism. For smaller set of docs (k=10, 100), I use the notion of Jaccard similarity to find highly similar documents. As a first step, I convert all the documents to document shingles using trigrams. For larger set of documents (k=1000, 10000), I leverage the MinHash and Locality-Sensitive Hashing (LSH) algorithms to find instances of plagiarism.

As a part of the study, I also run some experiments to answer the following questions - 

1. What is the effect of sharding length `k' on the Jaccard similarity of plagiarism instances versus instances that are not plagiarized?
2. What is the effect of the number of hash functions used to compute the Minhash signature on the accuracy of the Minhash estimate of Jaccard similarity?
3. What is the sensitivity and specificity of LSH as a function of the threshold value?
