# ChefBot
This is a group project of me and Elisa Degara, consisting in creating a Telegram Bot for recommending recipies to the user, given specific metrics, some in PDV which stands for percentage daily value, i.e. the percentage of that kind of nutrient based on the day. 
Those are the metrics used as input:
 - **ingredient list**
 - **calories**
 - **carbohydrates (PDV)**
 - **fats (PDV)**
 - **saturated fats (PDV)**
 - **proteins (PDV)**
 - **sodium**
 - **time**
   
In order to develop the bot, Elisa trained a **Doc2Vec** model on Food.com kaggle dataset [1] to represent recipies as documents and their ingredients as vectors. Moreover, given a list of ingredients the model will find the closest recipie in the dataset (using cosine similarity). Lastly, she took care of the creation of the telegram API. My contribution consisted into speeding up the whole inference part (by creating a specific dataset) and build a **kNN** model by treating all metrics as a vector inserted by the user (if user did not put some metrics they will replaced by the median value of the whole dataset), and find the k-th closest recipies between the ones found by the previous model.

We created two versions:
- **Chefbot**: the raw version
- **InteractiveChefBot**: a nicer interface has been added for selecting metrics (two buttons **Use Deafult**, **Custom**)

Note: The dataset have not been added due to their upload size, if interested contact me!

# Bibliography
[1] https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions/data?select=RAW_recipes.csv
