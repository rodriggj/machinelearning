# End-To-End Machine Learning Project

## Objective
> Work through an example project end to end, pretending to be a recently hired data scientist at a real estate company. 

+ [Steps](https://github.com/rodriggj/machinelearning/tree/proj01#steps)
    + [High Level Steps](https://github.com/rodriggj/machinelearning/tree/proj01#high-level-steps)
    + [Low Level Steps](https://github.com/rodriggj/machinelearning/tree/proj01#lower-level-steps)
+ [Reference Materials](https://github.com/rodriggj/machinelearning/tree/proj01#references)

---------

## Steps

### High level steps: 

#### 1. Look at the big picture
- [ ] 1.1 - Define the objective in business terms. 
- [ ] 1.2 - How will the solution be used?
- [ ] 1.3 - What are the current solutions/workarounds (if any)?
- [ ] 1.4 - How would you frame the problem (supervised, unsupervised, reinforced learning, online/offline, etc)
- [ ] 1.5 - How should performance be measured?
- [ ] 1.6 - Is the performance aligned with the business objective? 
- [ ] 1.7 - What would be the minimum performance needed to reach the business objective? 
- [ ] 1.8 - What are comparable problems? Can you reuse experience or tools? 
- [ ] 1.9 - Is human expertise available? 
- [ ] 1.10 - How would you solve the problem manually? 
- [ ] 1.11 - List the assumptions you (or others) have made so far.
- [ ] 1.12 - Verify assumptions if possible. 

#### 2. Get the data
- [ ] 2.1 - List the data you need and how much you need. 
- [ ] 2.2 - Find and document where you can get the data. 
- [ ] 2.3 - Check how much space it will take. 
- [ ] 2.4 - Check legal obligations, and get authorization if necessary
- [ ] 2.5 - Get access authorizations
- [ ] 2.6 - [Create a workspace](https://github.com/rodriggj/machinelearning/tree/proj01#26---create-a-workspace) 
- [ ] 2.7 - [Download the Data](https://github.com/rodriggj/machinelearning/tree/proj01#27---download-the-data)
- [ ] 2.8 - [Convert the data to a format you can easily manipulate (without changing the data integrity)](https://github.com/rodriggj/machinelearning/tree/proj01#28---210-take-a-preliminary-look-at-the-data)
- [ ] 2.9 - Ensure sensitive information is deleted or protected (e.g. anonymized)
- [ ] 2.10 - Check the size and type of data (time series, sample, geographical, etc.)
- [ ] 2.11 - [Sample a test set, put it aside, and never look at it (no data snooping)](https://github.com/rodriggj/machinelearning/tree/proj01#211---sample-a-test-set-put-it-aside-and-never-look-at-it-no-data-snooping)

#### 3. Discover and visualize the data to gain insights
- [ ] [3.1 - Create a copy of the data for exploration](https://github.com/rodriggj/machinelearning/tree/proj01#31---create-a-copy-of-the-data-for-exploration)
- [ ] 3.2 - Create a Jupyter notebook to keep a record of your exploration
- [ ] 3.3 - Study each attribute and its characteristics
- [ ] 3.4 - For supervised learning tasks, identify the target attribute
- [ ] 3.5 - Visualize the data
- [ ] 3.6 - Study the correlations between attributes
- [ ] 3.7 - Study how you would solve the problem manually 
- [ ] 3.8 - Identify the promising transformations you may want to apply
- [ ] 3.9 - Identify the extra data that would be useful 
- [ ] 3.10 - Document what you learned

#### 4. Prepare the data for Machine Learning algorithms
5. Select a model and train it
6. Fine-tune your model 
7. Present your solution 
8. Launch, monitor, and maintain your system

<small>[Back to Top](https://github.com/rodriggj/machinelearning/tree/proj01#high-level-steps)</small>
------- 

### Lower Level Steps

#### 2.6 - Create a Workspace

1. Install [python](https://www.python.org) if you haven't already. 

2. Create a path to your virtual environment
```s
export ML_PATH="$HOME/Desktop/Dev/machinelearning"
mkdir -p $ML_PATH
```

3. Create an isolated environment to contain you ML code and datasets with [virtualenv](https://virtualenv.pypa.io/en/latest/). Open a terminal session and run the following command: 
```s
python3 -m pip install -U virtualenv
cd ML_PATH
python3 -m virtualenv proj01
```

Now anytime you want to activate to this _virtualenv_ execute the following commands: 
```s
cd ML_PATH
source proj01/bin/activate   #on Linux or Mac
.\proj01\Scripts\activate    #on Windows
```

To exit, (aka deactivate) the _virtualenv_, execute the following command while in the active virtual env: 
```s
deactivate
```

4. Now that the _virtualenv_ is established, we need to install dependencies. For now we will install the following dependencies with our package manager program _pip_. 
+ jupyter
+ matplotlib
+ numpy
+ pandas
+ scipy
+ scikil-learn

To do this, in your _virtualenv_ `proj01`, type the following command: 
```s
python3 -m pip install -U jupyter matplotlib numpy pandas scipy scikit-learn 
```

5. Now you can fire up your Jupyter Notebook application which is where we will create our workspace that we will be using for our ML analysis. In your _virtualenv_ type the following command: 
```s
jupyter notebook
```

You should be redirected to a browser where you will see the Jupyter notebook application, and your proj01 env. If you didn't get a browser window, then Open a Brower and type `http://localhost:8888/`. 

6. From this screen, Click "New", and select "Python 3". You will re-directed to a new Workspace in Jupyter Notebook. You can rename the notebook to "Median Housing Prices" for future reference. 

<small>[Back to the Top](https://github.com/rodriggj/machinelearning/tree/proj01#2-get-the-data)</small>
---------

#### 2.7 - Download the Data
1. Typically we would connect to some data source and execute some queries to retrieve data. This would involve having the correct permissions, and access to the data source which we can't really mimic. For the purpose of this demo we will simply download a .csv file containing Census Data that we will use for our Median pricing analysis. 

2. Navigate to the following URL and download the .tgz file, fo the $ML_PATH directory. 

```s
https://github.com/ageron/handson-ml2/blob/master/datasets/housing/housing.tgz
```

3. Unzip this file, to uncover the `housing.csv` file. 

4. In the jupyter notebook, enter the following code to open and import the `housing.csv` file with the pandas library: 

```python
import pandas as pd
pd.read_csv("./housing.csv")
```

Which should render a data table in your notebook.

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207964415-848be661-d721-40e6-971b-5dde8ef46d9f.png">
</p>

<small>[Back to the Top](https://github.com/rodriggj/machinelearning/tree/proj01#2-get-the-data)</small>
---------- 

#### 2.8 - Convert the data to a format you can easily manipulate

1. Assigning the data read from the file to a variable will allow you to call additional methods utilizing the _pandas_ library. For example `head()` and `info()`. See diagrams below. 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207964801-390b42fc-2ae3-4fa4-a848-57ae3e180887.png">
</p>

> By leveraging _head()_ method you can see the top 5 rows of the DataFrame. Here you can see that there are 10 different attributes in the dataset. 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207964938-ef2f6a69-50a7-478b-8527-15ddd14c08ca.png">
</p>

> By leveraging _info()_ method, pandas library will render quick descriptions of the data, in particular the total number of rows, each attribute type, and the number of nonnull values. 

2. If we start to examine this output we can begin to define additional tasks needed to "rationalize" our data. For example note in the _info()_ display there are 20,433 values in the `total_bedrooms` feature. This means that 207 districts (our total was 20640) are missing this feature in the data set. You can also see that all the data attribues are numeric except for the `ocean_proximity` feature which is of type _object_. 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207967601-f4836d4e-fa63-4c45-b006-f140645fb2d7.png">
</p>

Another observation is that we can see that the `ocean_proximity` attribute has repetive values, suggesting it may be "categorical". If we wanted to validate this assumption we can use the pandas library _value_counts()_ method, and return the categories and count of values in each respective category. 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207968358-c564edef-8e21-479b-86f1-f9e1285d3260.png">
</p>

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207968942-01aa9321-be74-4397-b071-2f3ebe84713b.png">
</p>

3. We can explore the other "numeric" fields as well. For example lets look at the _describe()_ method which will show a summary of the numerical attributes in the housing data set. 

```s
housing.describe()
```
Here we see a returned table with some statistical data regarding the data set. 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207969304-302b59b0-8b6c-4a34-bda3-7268b6559bf0.png">
</p>

> **NOTE:** Null values are ignored when calculating these statistics. See the `total_bedroom` count is 20433 and all the statistical categories are still provided. 

> **NOTE:** The `std` row, shows the _standard deviation_ of the observed values to show the amount of dispersion in the attribute. 

> **NOTE:** The _quartile_ views. The 25%, median, 75% values show the median for the data captured in each _quartile_. So for > 25% of the observations the `housing_median_age` is 18 years old. 

4. Finally, one last way to quickly evaluate the downloaded data is to plot the data visually. This can quickly be done with a histogram of each of the attributes. You can execute a histogram on a single or all attributes in the data set. For this example we will use the _hist()_ method in the `matlab` library and list all attributes. 

```s
%matplotlib inline   # only neede in a Jupyter notebook
import matplotlib.pyplot as plt
housing.hist(bins=50, figsize=(20,15))
plt.show()
```

Will reveal output as follows in the Jupyter notebook: 

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207971016-e40814a4-1ccf-43a5-84b0-0bc1bbe3c371.png">
</p>

There are several things to notice about these histograms: 
1. The `median_income` attribute is not expressed in USD ($). After checking with the team you are told that the $ were _scaled_ and _capped_ at 15. For higher median incomes the value is at 15 and for lower median incomes the value is a 0.5. The numbers represent 10s of thousands (e.g. 3 means ~$30,000).

2. The `housing_median_age` & the `median_house_value` were also capped. The later may be a big problem when building your model, because the algorithm will assume that no value ever exceeds this limit (which is not true). 

3. These attributes have different scales. 

4. Finally, you notice that several of these histograms are `tail heavy`. Meaning there is a large amount of data outside of a "bell curve" which will make prediction accuracy difficult to predict "patterns". Some feature engineering or transformations of data may be necessary.

<small>[Back to the Top](https://github.com/rodriggj/machinelearning/tree/proj01#2-get-the-data)</small>
---------

#### 2.11 - Sample a test set, put it aside, and never look at it (no data snooping)

We want to avoid sampling bias, and create models that over-fit our data. Therefore we want to early on, take a portion of our sample data and set it aside as a `test-set`. The logic behind the amount of data you choose for test set varies, but an 80/20 rule typically applies. 

1. First we will create a function that will take our total sample size and divide it by some ratio we enter, to set aside a `training_set` and a `test_set`. 

```python
import numpy as np
def split_train_test(data, test_ratio): 
    shuffled_indices = np.random.permutation(len(data))
    test_set_size = int(len(data) * test_ratio)
    test_indices = shuffled_indices[:test_set_size]
    train_indices = shuffled_indices[test_set_size:]
    return data.iloc[train_indices], data.iloc[test_indices]
```

Now in our notebook execute the function with an implemention like this: 

```python
train_set, test_set = split_train_test(housing, 0.2)
```

Now validate that the split occured correctly. First test the `train_set` 
```python
len(train_set)
```

Next validate the quantity of the the `test_set` sample size
```python
len(test_set)
```

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207978151-965c7a03-1f01-4722-9c8a-8fc07b5a4d75.png">
</p>

2. While the function works there are several problems with this method of creating a sample test set: 
    1. We want the training data to be consistent so that we can train our model. We also want our test set to be consistent to ensure our performance metrics are valid as we "tune" our model. If we keep regenerating new "training" & "test" samples then we won't be able to consistently train or tune our model. 

    With the current function the next time you run the function new "training" & "test" sets will be created. We don't want this. 

    2. The function uses a purely random sampling method to isolate the "test" and "training" sets. This may cause issues with training our model b/c we are not assured that the randomly selected samples are represented of the total population. When a marketing company decides to do a random sample interview of a product they could simply open the phone book and start calling all the "A" names till they got to say 1000 samples. But there is a high likely hood that all the "A" named people are not a representative total of all the population in the phone book. We would want some dispersion to assume representation of the total. 

    3. Right now there is no "index" of each record in the dataset. We could use the "row" in the .csv file or some combination of attributes to create a unique identifier. But it is relevant to mention that random sampling without a means to id what was sampled in one run to the next is probably going to become a problem. 

To address these issues there are a few options: 
+ One option it so save the `test set` in the first run to another file and when necessary load this data.
+ Another option is to set the random number generator's `seed` (e.g. np.random.seed(42)^14) before calling _np.random.permutation()_ so that it always generates the same shuffled indicies. 

> Both of these solutions will break next time you fetch an updated dataset. 

+ A common solution is to use each instances' identifier to decide whether or not it should go in the test set. (assuming a unique id is available or can be created). For example you could compute a _hash_ of each instances' id and put that instance in the test set if it has a lower than or equal to 20% of the maximum hash value. 

```python
from zlib import crc32

def test_set_check(identifier, test_ratio):
    return crc32(np.int64(identifier)) & 0xffffffff < test_ratio * 2**32

def split_train_test(data, test_ratio, id_column): 
    ids = data(id_columns) 
    in_test_set = ids.apply(lambda id_: test_set_check(id_, test_ratio))
    return data.loc[~in_test_set], data.loc[in_test_set]
```
> Unfortunately the housing dataset does not have a identifier column. The simpliest solution is to use the row index as the ID. 

```python
housing_with_id = housing.reset_index()   # adds and index column
train_set, test_set = split_train_test_by_id(housing_with_id, 0.2, "index")
```

> If you use this method you need to make sure that new data gets `appended` to the end of the dataset and that no row ever gets deleted. 

+ Sci-Kit Learn provides a few methods for splitting datasets into mulitple subsets. The simpliest method is `train_test_split()` which does pretty much the same as our current split function with a few additional features: 
    1. there is a `random_state` parameter that allows you to set a random generator seed. 
    2. You can pass multiple datasets with an **identical number of rows** and it will split them on the same indices

```python
from sklearn.model_selections import train_test_split
train_set, test_set = train_test_split(housing, test_size = 0.2, random_state = 42)
```

3. Typically, instead of random sample sizes for your test set, `strata` are used to develop what is called `stratified sampling`. `strata` are homogenous subgroups within a population that are representative of the overall population total. The right number of instances are chosen within each `stratum` to gaurantee that the test set is prpresentative of the overall total. (e.g Census mapping of the united states would include strata such as men, women, homeless, employed, etc.)

In our scenario experts are used to define _median income_ as a very important attribute to predict _median housing prices_. You want to ensure that the test set is representative of the various categories (strata) of incomes in the whole dataset. Since the _median income_ is a continous numerical attribute, you need to create in _income category_ attribute. 

If you look at the _median income_ histogram, and decide we can use the this as a means to define strata. 

```s
housing["income_cat"] = pd.cut(housing["median_income"], bins=[0, 1.5, 3.0, 4.5, 6., np.inf], labels=[1,2,3,4,5])
```

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207984979-789e3c30-f875-4cf8-909d-7525246aa823.png">
</p>

4. So now we can use the _Scikit-Learn_ `StratifiedShuffleSplit` class to generate a test sample from the strata defined, with an appropriate number of instances within each strata to reserver in your test set. To do this type the following code: 

```python
from sklearn.model_selection import StratifiedShuffleSplit

split = StratifiedShuffleSplit(n_splits=1, test_size=0.2, random_state=42)
for train_index, test_index, in split.split(housing, housing["income_cat"]): 
    strat_train_set = housing.loc[train_index]
    strat_test_set = housing.loc[test_index]
```

<p align="center">
<img width="350" alt="image" src="https://user-images.githubusercontent.com/8760590/207987240-1c56ffd3-67a1-4834-93ba-fc2e6ee3505d.png">
</p>

5. It is now safe to say that our test data and our training data are similar such that a model built from the training set should have similar "generalization" when applied to our test set. 

<small>[Back to the Top](https://github.com/rodriggj/machinelearning/tree/proj01#2-get-the-data)</small>
---------

#### 3.1 - Create a copy of the data for exploration

1. Run the following command to create a copy of our training data

```python
housing = strat_train_set.copy()
```

<small>[Back to the Top](https://github.com/rodriggj/machinelearning/tree/proj01#3-discover-and-visualize-the-data-to-gain-insights)</small>
---------

#### 3.5 - Visualize the data

1. 
---------


## References

### Data Sets (Real World)
+ #### Popular open data repositories
- [ ] [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
- [ ] [Kaggle datasets](https://www.kaggle.com/datasets)
- [ ] [Amazon AWS datasets](https://registry.opendata.aws/)

+ #### Meta portals
- [ ] [Data Portals](http://dataportals.org/)
- [ ] [OpenDataMonitor](https://opendatamonitor.eu/frontend/web/index.php?r=dashboard%2Findex)
- [ ] [Quandl](https://data.nasdaq.com/)

+ #### Other pages listing many popular open data repositories
- [ ] [Wikipedia's list of ML Datasets](https://en.wikipedia.org/wiki/List_of_datasets_for_machine-learning_research)
- [ ] [Quora.com](https://www.quora.com/Where-can-I-find-large-datasets-open-to-the-public)
- [ ] [Subreddit](https://www.reddit.com/r/datasets/)

### Commands

housing = {variable}

#### Pandas
- import pandas as pd
- pd.read_csv("<path/file.csv>")
- housing = pd.read_csv("<path/file.csv>")
- housing.head()
- housing.info()
- housing.describe()

#### matlab
- housing.hist()
