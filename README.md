# R_selflearning

Repository for the Udemy course. Please support this project by joining this on-line course:

https://www.udemy.com/course/self-learning-trading-robot/?referralCode=B95FC127BA32DA5298F4

Note: this course is the part of the series of step-by-step tutorials allowing to build more comprehensive Automated Trading System based on Decision Support System approach. Check out other courses of the series. 

# Synchronize or Deploy

## Setup Environmental Variables

Add these User Environmental Variables:

PATH_T2 - path to Development Terminal MT4, folder *\MQL4\Files
PATH_T1, PATH_T3, etc - paths to the Terminals where all other terminals are located
PATH_DSS_Repo - path to the folder where this repository is stored on the local computer

## Goal

Create model-based self-testing artificially intelligent trading system.

## Motivation

There are probably just 3 possible types of mechanical trading systems:

* Human Idea[captured from the screen pattern] -> Indicator[parameters] + fix trading rules + Fresh Data = trading decision
* Past Data + Algorithm[based on some idea] -> Model[hyperparameters] + Fresh Data = trading decision [via predicted probability]
* Combination of the two above -> Fix trading rules + fresh data + filter based on the model = trading decision

The *first* approach relies on finding suitable parameters via optimization [bruteforcing many trades scenarios to find the best] and testing to confirm. This is typically done using MT4 terminal with optimization module

The *second* approach, developed in this course, relies on the model that would be trained to recognize the dominant pattern to generate trading decision. Approach will involve use of neural network model on `h2o` frame. The CPU is not 'bruteforcing' trades execution but follows the algorithm rules trying to find best parameters of the deep learning model. Technically use of NN models is more efficient as modern algorithms can use all CPU cores. As apposed to MT4 platform that can only use 1 CPU. At the same time training NN is more challenging due to reproducibility, overfitting issues, etc.

The *third* approach will use combination of the classic 'rule-based' system and will also use the 'model' as a filter. For example, a probability of winning the trade will be used to enter the trade once the rule-based system suggest an entry

## Main Features

Repository contains scripts capable to:

* collect financial data: (prices and indicators)
* transform data for modelling
* perform deep learning
* test deep learning model
* use model and fresh data to generate new predictions

Particularity of this project is that data and modelling is coming from 28 forex currency pairs. Data used for modelling is being collected to increase dataset. 

## Advantages

More efficient trading generation tool:

* Both reduced time and energy spent to perform modelling and test,
* Fully automated learning and testing,
* Model hyperparameter tuning using testing objective

## Challenges

Trading decisions are moved to the separate *Decision Support System* fully coded in R. This will imply the following:

* Reproducibility of the modelling, hyperparameter search may be computationally intensive and complex
* Required to do backtest of the strategy
* Non instant communication with MT4 due to usage of simplified file-based interface
* Black box system

## Courious how to apply?

This content is a result of a lot of dedication and time.
Please support this project by joining these courses using referral links published
here: https://vladdsm.github.io/myblog_attempt/topics/topics-my-promotions.html

## Disclaimer

Use on your own risk