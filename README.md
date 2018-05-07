Recommendation System

参见BMA笔记 - 2.8.8节 推荐系统

Content-based recommendations（基于同一主题域下的推荐）和Collaborative filtering (ItemCF, UserCF)两类

UserCF, 基于不同用户对同一物品评分的相似性来衡量用户之间的相似性，然后根据其他用户的购买记录给当前用户推荐。简言之，就是给当前用户推荐跟他兴趣爱好相似的其他用户购买过的商品。

ItemCF, 基于同一用户对不同物品评分的相似性来衡量物品之间的相似性，然后将与这个物品相似的其他物品推荐给用户。简言之，就是给当前用户推荐跟他已购买过的商品类似的其他种类的商品。

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