BMA - 2.8.8

Content-based recommendations
Collaborative filtering (ItemCF, UserCF)

Case: ItemCF - Bayer Product Recommendation, Model Evaluaton: Precision, ROC/AUC, Confusion Matrix

step1 output (user vector):
user1, item1:pref, item2:pref, item3:pref

step2 output (based on user vector to cooccurrence matrix):
item1:item1 1
item1:item2 1
item1:item3 1
item2:item1 1
item2:item2 1
item2:item3 1
item3:item1 1
item3:item2 1
item3:item3 1

step3 output1:
item1, user1:pref, user2:pref, user3:pref, user4:pref, user5:pref

step3 output2:
exactly like step2 output

step4:
multiply

item-item cooccurrence matrix
user-item evaluation matrix
multiply above two matrices -> user-item recommendation evaluation list -> sort by evaluation score -> filter out -> result.