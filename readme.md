# End-To-End Machine Learning Project

## Objective
> Work through an example project end to end, pretending to be a recently hired data scientist at a real estate company. 

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
- [ ] 2.7 - Get the data
- [ ] 2.8 - Convert the data to a format you can easily manipulate (without changing the data integrity)
- [ ] 2.9 - Ensure sensitive information is deleted or protected (e.g. anonymized)
- [ ] 2.10 - Check the size and type of data (time series, sample, geographical, etc.) 
- [ ] 2.11 - Sample a test set, put it aside, and never look at it (no data snooping)

3. Discover and visualize the data to gain insights
4. Prepare the data for Machine Learning algorithms
5. Select a model and train it
6. Fine-tune your model 
7. Present your solution 
8. Launch, monitor, and maintain your system

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