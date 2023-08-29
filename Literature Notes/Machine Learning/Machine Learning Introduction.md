**Machine learning** is a very big concept in programming. It allows us to use tons of possibly useless [[#Data type|data]] and make it more valuable, useful. It does that by using sophisticated [[algorithms]] to distinguish patterns in data and eventually predict the answer based on this data. That is really valuable asset if we want to automate our applications or try to predict answer to sophisticated problems that are data based.

-------------------------------------------------------
# Types of ML
To work with data and create machine learning models, we have to know basic classification of ML algorithms types we can encounter:

###  Supervised Learning 
Most common type of ML, where we know specifically what the inputs are and what the predicted outputs can be. Data in this category is labeled just like columns and rows in spreadsheet, which also defines a model.

### Unsupervised Learning
In this case, we deal with unlabeled data as our input and we are not really sure what output we can expect. There are no true categories when it comes to predicting one, so we cannot tell the machine if it's right or wrong. We just let the machine create and organize those categories.

### Reinforced learning
It's all about teaching machine through trials and error. We let machine make prediction on some particular data set and then reward the machine for making good decision, or punish it for making a poor one.

-------------------------------------------------------

# Framework
Every ML project need have some sort of foundation on which we can build further. Some sort of a plan. That's what the framework is. It consists of 6 layers:


### Problem definition
We need to answer on the following question: ***"What problem are we trying to solve?"***.

Maybe the problem can be solved in a more classical way, without the need of using ML? In this case, we should absolutely choose to solve it using less advanced programming tools.

We also need to know, what is the type of problem we are encountering. Is this a [[#Supervised Learning]], [[#Unsupervised Learning]] or maybe [[#Reinforced learning]] problem?


### Data type
We need to answer on the following question: ***"What type of data we deal with?"***. Two main data categories are:

- **Structured Data**
- **Unstructured Data**

**Structured Data** is something you expect to see in excel file, such as rows and columns with their own labels. We can say that it's highly organized, have typically the same format and is somewhat consistent.

**Unstructured Data** is everything such us audio files, video messeges, phone calls, images etc. We can't really orginize it into logical categories.

We also differentiate between **static** and **streaming** data. The first one doesn't change at all, but the second one does.


### Evaluation
We need to answer on the following question: ***"What defines success for us?"***. Depending on our scenario we can have various goals. Maybe our model need to be extremely fast and doesn't have to be very accurate. Or maybe we need to have really high accuracy no matter what. That's what evalution is.


### Features
We need to answer on the following question: ***"What do we already know about the [[#Data type|data]]?"***. Feature are referring more specificaly to different forms of data within structured or unstructured data.

Features can be for example different categories of data that we will be using to predict the answer we are looking for. Those categories are named **feature variables**. We are using them to predict a **target variable**.

There are also **numerical features** which are straight-up numbers and patterns they possess.

We can base on those two types of features to create our own, **derived features**.

> [!NOTE] Unstructured data features
> Note that unstructered data also have features, they are just less obvious for us.


### Modelling
We need to answer on the following question: ***"What kind of model should we use?"***.  We can distinguish 3 parts of modelling:

- [[#Choosing and training a model]]
- [[#Tuning a model]]
- [[#Testing a model]]

#### Spliting Data
But before we can proceed to those operations, we need to **split** our data into 3 sets: 

- **Training** set (70% - 80% of data)
- **Validation** set (10% - 15% of data)
- **Test** set (10% - 15% of data)

It's crucial to correctly [[#Evaluation|evaluate]] how well our model is doing. To ensure that the answer will be reliable, we have to strictly separate our data into 3 sets that have to be disjunct so that our model will be tested on data that it has never before encountered.

#### Choosing and training a model
It's important to use proper tools for different [[#Problem definition|problems]] we may encounter. On one hand, tools such as *CatBoost*, *XGBoost* or random forest algorithm can be helpful for structured data. On the other hand, concepts such as deep learning and transfer learning can be used to deal with unstructured data.

To start training our model, we have to use feature variables to predict target variables (when we are dealing with [[#Supervised Learning]]), or we have to use different methods depending of our [[#Types of ML|type of problem]].

Time optimization is also a thing to consider while training a model. Sometimes little increase in accuracy is not worth disproportionately longer runtime.

Remember that all the training takes place only on [[#Spliting Data|training set]].

#### Tuning a model
Machine learing models have hyperparameters you can adjust. It all depends on algorihtm we decide to use. By changing those parameters we can enhance results of our model. Tuning can take place on [[#Spliting Data|training set]] or [[#Spliting Data|validation set]].

#### Testing a model
One of the most important parts of ML framework. Testing a model can tell us a lot about its real capabilities. We analyze accuracy obtained on training set and test set and compare those two values. They should be as close to each other as possible. If our test set has significantly less accuracy than our training set we are dealing with **underfitting** model. If our test set has significantly more accuracy than our training set we are dealing with **overfitting**. 