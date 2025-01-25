# ChefBot
This is a group project of me and Elisa Degara, in order to create a Telegram Bot for recommending recipies to the user given specific metrics, some in PDV which stands for percentage daily value, i.e. the percentage of that kind of nutrient based on the day:
 - **ingredient list**
 - **calories**
 - **carbohydrates (PDV)**
 - **fats (PDV)**
 - **saturated fats (PDV)**
 - **proteins (PDV)**
 - **sodium**
 - **time**
   
In order to do this, Elisa trained a **Doc2Vec** model to represent recipies as documents and ingredient componing those recipies as vectors. Moreover, given a list of ingredients the model will find the closest recipie. My part consisted into speeding up the whole inference part and build a **kNN** model by treating all metrics as a vector inserted by the user (if user did not put some metrics they will replaced by the median value of the whole dataset), and find the k-th closest recipies in the one found by the previous model.
Note: We use a refined dataset based on the Food.com kaggle dataset [1] which we cannot upload here due to its size, if interested contact me for more information!

# Bibliography
[1] https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions/data?select=RAW_recipes.csv
