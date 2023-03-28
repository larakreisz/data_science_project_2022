# Data Science Project 2022

### key results, lessons learned and achievements

+ One should not unknowingly use the target variable (tips) indirectly to calculate the input variables that one later wants to transfer to the machine learning model. This was a problem for us when we created the feature for the past tipping behavior. This unintentionally tells the machine learning model the result - which becomes problematic as soon as the model is supposed to calculate actual future data. With error, the forecast accuracy on the training set was about 89%, after correction of the corresponding feature 74%. The forecast accuracy on the validation set is 78,6%


+ One should try to avoid including future values in the calculation, because this also trains the machine learning model in the wrong direction. This was also a problem with Past Tipping Behaviour.



+ After correcting the model and fixing the bugs, we didn't have as much time to investigate further. As a first step, we checked whether we could find products for which a tip was given particularly frequently. This was not promising, however, as it tended to worsen our forecast. It would be to check if we simply chose the wrong products there and if one can find better products related to this. For example, by selecting the 100 most common products and examining which of them have the highest tip rate.


+ The section with the departments could also be improved. Other departments to look for are: Bulk, Snacks, Deli, International, Pantry


+ One could also examine whether the weight of the order also influences the betting behavior of the users. For this, however, new data would have to be collected from the company, since the weight of the individual products was not given.


+ We also noticed that the order_id doesn't sort the orders in the right order. The order_id seems to be randomly assigned to anonymize the data. Therefore, it is not optimal that we sorted the orders by the order_id for our training and testing split. It would be better if you could sort the orders by date, for example, or if you could modify the test data to only contain the user's most recent order.


+ As a final point, we would recommend that the company not only investigate whether someone has tipped, but also how much the tip was. A customer who tips only a very small amount, for example €1, may be less valuable than a customer who tips €12.
