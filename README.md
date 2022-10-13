# SLackathon-Payment-Fraud-Detection-cygnus01
#### By K.Poornima
  

### 1.0 Introduction


Digital era marks how much we, collectively as human race, have achieved in technology in various disciplines. From the deepest of the ocean to the greatest expanse of space, we have got it covered. Advancement of mankind has grown tremendously in enhancing connectivity, broadening communication range, storing and retrieving data at larger scale without sacrificing the quality, redefining conventional learning method, flipping through on over-the-top platforms for current entertainment, traveling in sophisticated mode of vehicle and so much more. In short, everything is made comfortable, easy and flexible for us, the consumers. Convenience at the tip of our fingers is not a mere catchy phrase but a reality. 

As much as technology unites, diminishing distance between us, it has its own fair share of disadvantages. Most obvious one is privacy. Freedom comes with a cost to many in this digital epochs. Data is scattered all around and in the period of heightened cybersecurity, we still witness the costly affair of data leakage on millisecond basis. Data leakage leads to a lot of opportunities to create mishaps in the financial world. It is always tied to a strong human component, be it greed or conflict of interest. Without internal inputs, it is indeed cumbersome for the fraudsters to proceed. 
It is easier to transfer money to any part of the world, to anyone by just tapping our mobile phones, instantaneously. Purchasing online using credit card is a breeze too or paying for services through mobile apps. The growth in electronic transactions makes it accessible to external sources albeit the security systems motivated by the increased sophistication of fraud attempts and the rising number of attack strategies.

According to the information published by Statista Research Department, value of fraud loss in the US (2021) through bank transfer/payment alone is 756 million USD [^1] as opposed to other type of frauds such as cryptocurrency, wire transfer, gift/reload cards, cash advance, check, debit card, payment app/service and money order. Besides that, a new study conducted by Juniper Research states that businesses in e-Commerce, airline ticketing, money transfer and banking services, will cumulatively lose over 200 billion USD to online payment fraud between 2020 and 2024 [^2]. Evidently the loss is irrevocable.


### 2.0 What is the exact problem? 


What is payment fraud? It is a criminal act where unauthorized transactions are made using another’s person stolen credentials. Fraudsters can choose to hit any banks, across the globe, at any time to intrude online banking sessions. Their activities include stealing credentials for clients, deploying malware and obviously, transferring funds from accounts of clients illegally. In this challenge, we are going to concentrate on credit card transactions frauds which come in a few forms:

  -	true fraud (where identity of the customer is stolen together with their credentials and the fraudsters proceed to make purchases)
  -	friendly fraud (where the chargeback is initiated after receiving the product or service based on false claims)

A credit card fraud can take place without a physical card, through corrupted credit card application, account takeover (can happen by sim card clone/swap, where the pin number can be changed by the fraudster by using stolen credentials) and most popular method is the practice of credit card skimming. Customers are the weakest links in this chain as they can be easily cheated and of course lack of awareness on cybersecurity make them vulnerable to digital frauds. 


#### 2.1 Why is it happening?

**Vulnerabilities of finance institutions/banks**

As the volume of electronic transactions have increased manifolds, the traditional/manual way of monitoring each transaction do not have the capacity or speed to halt fraudulent activities. By the time, the fraud is detected, it is usually too late to trace back or recall. 

Government’s policy is also exposing banks to more challenges although their main interest is to protect consumer rights in case of any illegal transactions under certain conditions[^3]. For example, European Union’s 2nd Payment Services Directive(PSD2) which was introduced in 2018 urges all the ensuring safe and secure payments. In short, the banks must have anti-fraud software solutions installed as per the EU Payment Services Directive (PSD2). PSD2 allows the customers to authorize a third party payment service providers to transfer payment from their account to the pay for products/services, just more new ways for transactions to happen, refer to image 2.0 below. Another challenge to add to the bucket is how to protect identification of customers/discovery of sensitive information while opening up to third party payment service providers.

![image 2 0](https://user-images.githubusercontent.com/107114510/195568460-53d04f2b-40e9-413f-9128-3292634214ce.png)
<p align="center">Image 2.0 What third-party payment looks like?</p>

The banks, in this case, will expedite the sharing of highly confidential information with the third-party service provides through APIs and they have to be responsible for any unauthorized transactions that take place on customer’s accounts through open APIs.

The digital revolution which the banks are going through is also enabling new types of fraud to emerge. Customer-centric approaches the bank take are also exposing them to the fraudsters, this just gives them a wider and larger arena to attack. 
Existing firewalls are not protecting the banks against external attacks as novel techniques are being developed by the criminals to bypass the security system. Besides that, there isn’t any real protection against sim card fraud (the sim card of customers are cloned or swapped, inhibiting the authorization messages/purchase proof from being sent out).
The banks have to be vigilant at all times, monitoring each transaction, which is not easy, practically.

#### 2.2 Why current approaches in handling frauds are not efficient? 

As a general practice, banks’ first layer of defense mechanism against frauds is rule based anti-fraud systems. A set of pre-defined conditions/rules are employed to investigate suspicious transactions. Some of the criteria could be the location the payment is made, first time the recipient receives (a threshold can be set for above a certain amount based on historical data) and so on. These predefined rules are rigid and do not take into account of new type/pattern of fraud when it happens. Two factors invalidate the rule based system; the arena of online payment has widen enabling the fraudsters to be creative and ever ready to attack. Secondly, the kind of flexibility digital transaction gives to the customers where the payment can be made from anywhere, to anyone, regardless of time and means which makes the rule based system to be not so customer friendly. Again, the conventional method of identifying fraud will not be able to read/analyze the behavior of customer’s nature is it is valid or suspicious.

The ever evolving rate of frauds or fraudsters is overwhelming and financial institutions/banks need the intervention of machine learning/analytics besides stringent cybersecurity systems as their conventional method is not solving the issue. Banks have been taking a different approach, by investing in artificial intelligence. However, mainstream AI based approaches fail to deliver due reasons like training data is not large enough, data imbalance (non-fraud cases are more in number compared to fraud cases where the difference is so significance enough that most models suffer from overfitting (performing well enough in training but poorly with the test data/new data) [^4].

#### 2.3 What we can do differently and why data analytics/machine learning?

A lot of insights can be drawn based on historical data which might consists type, size and location of transaction, was it a first time recipient from a customer’s account, time, day and month, the customer’s device upon which the transaction was triggered, which web browser and much more. Also, if a transaction does not fall in the usually occurring list, it can be further analyzed before blocking it for fraud. It cannot be done manually for each transactions and this is where we can go arms in arms with data analytics/machine learning. Not only, it would be able to learn from a customer’s previous behavior and compare it with the customer’s profile but it can provide a better channel to flag transactions. Once flagged, it will go through more in depth check whether it has exceeded certain threshold before blocking the transaction for good and thus indicating a flag. The highlight of data analytics is premature and spontaneous discovery of out of place transactions or anomalies in real-time by taking into account the already existing fraud detection and trigger alerts when it surpasses the normal set boundary. Unlike the conventional method, where the rules are rigid, in machine learning, the model would be able to learn and identify new fraudulent patterns in frauds without manual intervention. The traditional way of doing things might not time and cost efficient.


### 3.0 The approach


Our challenge is to detect and prevent the fraud by analyzing individual customer’s behavior and the overall context in where and how each transaction takes place is then compared with the customer’s established behavioral profile to detect any anomaly. We need a multi-agent system and therefore we will employ a mixed model with the combination of both supervised learning (the model will train based on features and target output to detect/predict future frauds) and unsupervised learning (the model will detect anomalies through clustering). Image 3.1 shows the first phase of fraud detection system and image 3.2 shows the second phase flow diagram where the payment is sanctioned.

![image 3 1](https://user-images.githubusercontent.com/107114510/195569599-cb901624-8ee5-49ca-bc56-91b7edf09d4a.png)
<p align="center">Image 3.1 – First phase of fraud detection system - Monitor transaction and behavioral analysis</p>


![image 3 2](https://user-images.githubusercontent.com/107114510/195569610-1358b46a-6012-4d67-bab3-bf5fc76eed6c.png)
<p align="center">Image 3.2 – Second phase of fraud detection system – Payment Sanctioning</p>

A scoring method will be enabled in our model and each transaction will be scored against it. The model will include all the available data collected (type, size and location of transaction, was it a first time recipient from a customer’s account, time, day and month, the customer’s device upon which the transaction was triggered, which web browser and so on) and use these to score the transaction. If the transaction is suspected to be an anomaly, it will be flagged.
Detection in real-time is the key to find a proper solution. Figure 3.0 [^5] shows the reaction time in establishing a fraud. There is a latency or time lag between the point which fraud happened and fraud detected. By the time the model realizes a fraud, it is usually too late. More advanced algorithms (for future studies) must be used in order to catch the fraud earlier. Of course, besides the algorithms, the IT infrastructure should be diligent enough to handle incoming threats.

![image 3 3](https://user-images.githubusercontent.com/107114510/195569994-351413fc-a839-48b7-b42d-5e16ec704dbc.png)
<p align="center">Image 3.3 - Key Issue: Reaction Time</p>

In short, we need to develop an anti-fraud system incorporating multiple agents (2 or more) which can effectively detect anomalies and prevent fraudulent activities as early as possible by not compromising customer’s confidential information. Our aim includes reducing false positives as to not cause inconvenience to the customers as well and operational losses. 


### 4.0 General overview on data preprocessing and model building.


![image 4 0](https://user-images.githubusercontent.com/107114510/195570154-40b32444-c80e-484e-9cad-cb448c2a3457.png)
<p align="center">Image 4.0 – Overview on data preprocessing and model building</p>

#### 4.1 The probable challenges in developing the ML Model

Our dataset might have outliers, missing data, skewed data distributions or imbalance target labels. Outliers are points abnormally high or low compared to other points and they can’t be just deleted. It could be a typing error or an IOT device recorded the values wrong and in cases like fraud detection, unusual incidents (outliers) should be further investigated as it can be a fraudulent activity. Not handling outliers will prolong the training time and thus results in less accurate model. 
Skewed data distribution shows the spread of data and if it follows a normal distribution. If not, it should be rectified as well because skewed data can clutter up the power of our predictive model. 

Imbalance target class is very common in fraud detection. Our dataset can have a binary class where 1 stands for fraud and 0 for non-fraud. Usually, the frequency of 1s (fraud transactions) will be lesser compared to 0s (non-fraud transactions) and in this case, our model will be trained primarily on 0 class while ignoring the minority class of 1. There is a high probability of misclassification of the minority class as compared to the majority class. It might even show a high accuracy where:

```math
Accuracy = (TP+FP)/(TP+FP+FN+TN) where 
- TP = True positive
- FP = False positive
- FN = False Negative
- TN = True Negative
```

The metric selected for imbalance target class dataset should be a combination of Recall and Precision, like F1-Score.

Feature elimination/masking either by regularization or dimensionality reduction. We can even venture into IBM Privacy toolkit in order to build a less complex model while removing redundant features which will not be useful in building our model.

**References**

[^1]: "Value of fraud loss in the United States in 2021, by payment method." https://www.statista.com, 30 Sept. 2022, www.statista.com/statistics/958997/fraud-loss-usa-by-payment-method.

[^2]: "ONLINE PAYMENT FRAUD LOSSES TO EXCEED $200 BILLION OVER NEXT 5 YEARS." https://www.juniperresearch.com, 25 Feb. 2020, www.juniperresearch.com/press/online-payment-fraud-losses-to-exceed-200-billion.

[^3]:"Payment Services Directive: frequently asked questions." https://ec.europa.eu/, 12 Jan. 2018, https://ec.europa.eu/commission/presscorner/detail/fr/MEMO_15_5793.

[^4]: "Payment Fraud." https://www.netguardians.ch, accessed on 10 Oct. 2022, www.netguardians.ch/solutions/payment-fraud/.

[^5]: "Fraud Latency." Data Science Warsaw Meetup, 28 Feb. 2017, www.slideshare.net/mrafalo/realtime-fraud-detection-in-credit-card-transactions.

