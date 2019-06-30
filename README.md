# Association-Rule-Learning
A Practice section from course on Udemy. Here, we have to optimize the sales of products of a grocery store. Use Association rule learning to know where to place the products in the store.

Association rule learning is a rule-based machine learning method for discovering interesting relations between variables in large 
databases. This concept can be best understood with the supermarket example. In a supermarket, they infer data about the customer 
purchasing pattern for various products. With the help of association rule, the supermarket can distinguish which products are often 
bought together and this information can be used for marketing objectives. Association Rules work on the basis of if/then statements. 
These statements help to reveal associations between independent data.

Three important metrics to understand the strength of association:
a. Support: This measure gives an idea of how frequent an itemset is in all the transactions. Support is the fraction of the total number
of transactions in which the itemset occurs.
b.Confidence: This measure defines the likeliness of occurrence of consequent on the cart given that the cart already has the antecedents.
For example, confidence of an item "Butter" given the transaction already has item "Bread" in it is very high.
c. Lift: Lift controls for the support (frequency) of consequent while calculating the conditional probability of occurrence 
of {Y} given {X}. Lift is the rise in probability of having {Y} on the cart with the knowledge of {X} being present over 
the probability of having {Y} on the cart without any knowledge about presence of {X}

Apriori Algorithm:
Apriori uses the prior knowledge of frequent itemset frequencies. Generate all frequent itemsets (support ≥ minsup) having only one item. 
Next, generate itemsets of length 2 as all possible combinations of above itemsets. Then, prune the ones for which support value 
fell below minsup. Now generate itemsets of length 3 as all possible combinations of length 2 itemsets (that remained after pruning) 
and perform the same check on support value. We keep increasing the length of itemsets by one like this and check for the threshold 
at each step. Once the frequent itemsets are generated, rules are formed by binary partition of each itemset. From a list of all possible 
candidate rules, we aim to identify rules that fall above a minimum confidence level (minconf). Now, this subset of rules thus 
generated can be searched for highest values of lift to make business decisions.
