## Ineuron Internship Machine Learning project

Application url:
[Insurance Premium Predictor](https://premiumprediction-app.herokuapp.com/)

# Insurance Premium Prediction:
 
To give people an estimate of how much they need based on their individual health situation. After that, customers can work with any health insurance carrier and its plans and perks while keeping the projected cost from our study in mind. This can assist a person in concentrating on the health side of an insurance policy rather than the ineffective part.

**_ Data source _**: https://www.kaggle.com/noordeen/insurance-premium-prediction

### Dataset description

1. Age: Person's age in years
2. Sex: Gender of the person or insurance holder(Female or Male)
3. BMI: Body mass index. The ideal range according to height and weight is 18.5 to 24.9
4. Children: Number of dependents
5. Smoker: Whether the insurance holder smokes or not
6. Region: Residential area of the person
7. Expenses: Individual medical costs billed by health insurance

## Approach: 
1. Loading the dataset using Pandas and performed basic checks like the size of the data, data type of each column and having any missing values. Also checked the uniq values of categorical columns.
2. Performed Exploratory data analysis:
- To get even more better insights visualized independent feature with the target feature
- - the distribution of the target feature, expenses which was in Normal distribution with a very little right skewness.
4. Data Transformation:
- To standardise numerical columns i use standard scaler technique and to create dummy variables for categorical columns used onehotencoding.
3. Experimenting with various ML algorithms
- Like LinearRegression, DecissionTreeRegressor, GradienBoostingRegressor and RandomForestRegressor ,performed hyper parameter tuning using the GridSearchCV and found the best hyperparameters for each model. Then, picked the top most features as per the feature importance by an each model. Models, evaluated on both the training and testing data and recorded the performance metrics. Based on the performance metrics of both the linear and the tree based models, random forest regressor performed the best among all.
4. Deployment: Deployed the Randomforest regressor model using Flask, which works in the backend part while for the frontend used HTML5.

### Software and account Requirement.

1. [Github Account](https://github.com)
2. [Heroku Account](https://dashboard.heroku.com/login
3. [VS Code IDE](https://code.visualstudio.com/download)
4. [GIT cli](https://git-scm.com/downloads)
5. [GIT Documentation](https://git-scm.com/docs/gittutorial)


Creating conda environment
```
conda create -p pvenv python==3.7 -y
```
```
conda activate pvenv/
```
OR 
```
conda activate pvenv
```

```
pip install -r requirements.txt
```

To Add files to git
```
git add .
```

OR
```
git add <file_name>
```

> Note: To ignore file or folder from git we can write name of file/folder in .gitignore file

To check the git status 
```
git status
```
To check all version maintained by git
```
git log
```

To create version/commit all changes by git
```
git commit -m "message"
```

To send version/changes to github
```
git push origin main
```

To check remote url 
```
git remote -v
```

To setup CI/CD pipeline in heroku we need 3 information
1. HEROKU_EMAIL = pallabisahoo1234@gmail.com
2. HEROKU_API_KEY = <>
3. HEROKU_APP_NAME = premiumprediction-app

BUILD DOCKER IMAGE
```
docker build -t <image_name>:<tagname> .
```
> Note: Image name for docker must be lowercase


To list docker image
```
docker images
```

Run docker image
```
docker run -p 5000:5000 -e PORT=5000 f8c749e73678
```

To check running container in docker
```
docker ps
```

Tos stop docker conatiner
```
docker stop <container_id>
```


```
python setup.py install
```


Install ipykernel

```
pip install ipykernel
```