# Network-Analysis-of-Sjogren-s-Syndrome-Factors
Data Preparation:

We created Sjogren’s syndrome dataset (SSD) with 2530 PubMed abstracts retrieved using keywords Sjogren’s syndrome and its variants. We tokenized these abstracts into a list of sentences. We have round 26000 sentences from this 2350 abstracts, we removed the unnecessary words from these sentences using Excel and made the dataset ready for analysis. The next step is identifying the causal sentences within these sentences to identify cause and effect factors related to Sjogren’s syndrome. For this we created a list of causal words and tried to filter out the sentences that are having these causal words, we used Python for this process. By this process we got around 21770 sentences out of those 26000 sentences as causal. The problem with this approach is the causal word might not be the root word in the sentence but still the sentence might return as causal sentence because it has the word. To overcome this problem, we ran a classification model on this 21770 sentence that gives a probability score whether the sentence is causal or not. Out of 21770 we have around 5655 sentences with probability of being causal sentences. We cleared the unnecessary data that is not required for our analysis and finalized the sentences. For Network Analysis we want to focus on a subset of sentences from these sentences. So, we identified sentences where the root causal word is ‘cause’, we used similar process we used for identifying the causal sentences before. We got around 420 sentences where the root causal word is cause. The next text is identifying cause and effect words within these sentences, we have manually identified cause and effect pairs within each sentence and created the final dataset for network analysis with two columns cause and effect where we have around 430 cause and effect pairs.
![image](https://user-images.githubusercontent.com/91715369/195698289-405d223b-1a4e-4538-92d2-b39022f22432.png)