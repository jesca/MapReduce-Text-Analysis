MapReduce-Text-Analysis
=======================

MapReduce to answer a big data problem: Given a word, what other words are statistically associated with it?

A reasonable statistical definition is the co-occurrence, which measures how often two words appear together in documents. Given a target word, we can figure out which words in a body of text (called the corpus) are most closely related to it by ranking each unique word in the corpus by its co-occurrence rate with the target word. To calculate:

    Let Aw be the number of occurrences of w in the corpus. 
    Let Cw be the number of occurrences of w in documents that also have the target word.

   Co-occurrence rate :=  if(Cw > 0)   Cw * (log(Cw))3  / Aw  
                                    else  0
