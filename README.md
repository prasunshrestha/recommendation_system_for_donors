# Social-good-recommender-system
This project is to build a recommender system for donors of DonorChoose.org platform to increase repeat donations


PROJECT OVERVIEW
DonorsChoose.org (DCo) is a fund-raising platform that empowers public school teachers across the nation to request funding support for educational needs through its online platform. Since DCo’s establishment in 2000, 4.6 million donors and partners have funded more than 1.7 million projects. There is a need to increase repeat donation, through targeted marketing to donors with higher likelihood of re-contribution. Thus, we will work on DonorsChoose.org data challenge to build a recommendation system that profiles donors with higher probability of repeating donations and suggest projects that are likely to be supported by the prior donors. And this recommendation system can be expanded to any other fundraising platform beyond DCo.
In addition, we can also leverage DCo’s data to address their additional challenges. Teachers have many projects in parallel that require fundings. A classifier that could predict the likelihood of a project being funded will benefit the teachers, as they then can propose the projects which are most likely to be funded. As a result, our project will also build a classifier to predict the probability of a project's funding success.


DATA DESCRIPTION
The data is available at Kaggle’s website, which is where DCo hosted their data challenge as well. It includes all the projects from January 2013 to May 2018, with a total number of 4.6 million observations. Available are six data files: (1) Projects.csv, (2) Schools.csv, (3) Teachers.csv, (4) Resources.csv, (5) Donations.csv, and (6) Donors.csv. Each file includes pertinent details - for example, Projects.csv includes project type, cost, short description, and project’s funding status.

PROJECT GOALS
Increase recurring donations among prior donors via donor profiling and the recommendation system.
Build a classifier that will predict the likelihood of a project being funded.
DELIVERABLES
A detailed profiling of donors and projects based on the past data by clustering. The clustering will be used for User-item mapping in the recommendation system
Visualizations for understanding the projects, stakeholders and donations made till date
A recommender system suggesting projects with funding needs to prior donors of DCo (fund-raising platform).
A classifier to predict the likelihood of a project getting funded.
The deliverables will be modular and standardized so that any fundraising platform can use the application with few modifications like feature engineering and use it with minimal effort.


HYPOTHESIS
Donors are more likely to donate to projects that match their geographic region, such as zip code or urban/rural.
Projects of educational supplies type, such as stationeries, are more likely to get donor support than other types.
If a donor makes a recurring donation, s/he is more likely to donate to a similar project.

TECHNICAL APPROACHES
The dataset contains both temporal (5 years) and spatial data (donors and teachers located across cities in the US). Our train, test, validation splits, and k-fold cross validations will take the temporal and spatial nature of the data into consideration. 
We intend to use unsupervised learning algorithms, such as k-means clustering and collaborative filtering, to cluster different types of donors. The different unsupervised learning algorithms will then be compared for performance. The cluster will also help us understand a donor’s likely project preferences, which we could leverage to market targeted projects to them.
We will use collaborative filtering as we are building the recommendation system for existing donors. Both memory based and model based approaches will be tried to get the best model. User-item interaction (donor-project) will be the primary method for recommendation systems. User-user and item-item methods will also be tried out.
We will build a classification algorithm, such as logistic regression, decision tree, and SVM, to predict whether a project will be funded. We have historical data that shows us whether a project is funded or not. Thus, we can apply supervised learning models to discern the patterns and build a classifier.


PROJECT RISKS:
Our domain knowledge is limited, and we do not have access to the organizational expertise
The dataset is large (~4 GB); thus, any model could be computationally expensive, perhaps infeasible in our single machine
MITIGATION STRATEGIES:
We will use the publicly available information to understand the organization and its needs. Should we have questions, we will reach out to them. Additionally, we could plan and use PySpark if computation becomes a bottleneck. We have access to Pittsburgh Supercomputer Center (PSC) as part of our Big Data class

