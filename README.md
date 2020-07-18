# Genomic-Sequence-Analysis-using-SVMs
Classify ncRNA strands using different Support Vector machines and interpret their behaviour with different regularisation parameters and sigma (gamma) values.

Non-coding ribonucleic acids (ncRNA) are believed to have many roles in a cell, many of which remain to be discovered. However, it is difficult to detect ncRNAs using biochemical screening methods. Recent studies have shown that computational methods can accuractely detect ncRNAs, which can be treated as supervised classification. To perform the classification, an 8-dimensional feature vector is used as input to a classifier, including the length of genomic sequence and nucleotide frequencies:

A feature value computed by the Dynalign algorithm http://www.ncbi.nlm.nih.gov/pubmed/11902836

Length of shorter sequence:
1. `A' frequencies of sequence 1
2. `U' frequencies of sequence 1
3. `C' frequencies of sequence 1
4. `A' frequencies of sequence 2
5. `U' frequencies of sequence 2
6. `C' frequencies of sequence 2

Here I have trained different support vector machine (SVM) classifiers to determine if a genomic sequence is an ncRNA strand.

In file, the data is organised as: label index1:value1 index2:value2... where each line contains a training/test example. label is a bipolar value (1 or -1) indicating the class label (1 indicating an ncRNA, the positive class). Index is an integer in the range [1, 8] corresponding to the 8 features listed above and value is a real number corresponding to a feature value which has been scaled to [0, 1]
