<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/Customer%20Churn.png" width="1250" height ="650">
</p>

# Customer-Churn-Analysis

## The purpose of this project is to provide an end-to-end Business Analysis Solution to minimize Customer Attrition for a Telecom service provider.

#### The project aims to determine the factors associated with Customer churn along with quantification and categorization of the churn risk associated with any user in the subscriber base and to find out the most popular churn segments.   


## Demo-Preview

The end goal is to create a business solution report satisfying all the demands of the client (as per the specified acceptance criteria) mentioned in the business request document. Here's a glimpse of the final report.

![](https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/Project_Demo.gif)
<p align="center">
  <em>Business Solution Report</em>
</p

[(Back to top)](#table-of-contents)


## Table of contents

- [Demo-Preview](#demo-preview)
- [Installation](#installation)
- [Background](#background)
- [Business case](#business-case)
- [Requirement Gathering and Documentation](#requirement-gathering-and-documentation)
- [Data Summary and Exploratory Analysis](#data-summary-and-exploratory-analysis)
- [Dashboarding](#dashboarding)
- [Conclusion](#conclusion)


## Installation
  
Apart from the pre-installed Microsoft Office Suite, Power BI Desktop is used which is an open source Data Visualization software created by Microsoft as part of the Microsoft Business Intelligence Toolkit.
  
As per your system specifications. [Download Power BI from here.](https://powerbi.microsoft.com/en-us/downloads/)
  
[Step by step installation guide.](https://www.youtube.com/watch?v=T_qnV-HTb-M)


[(Back to top)](#table-of-contents)


## Background

Customer churn or customer attrition is the phenomenon where customers of a business no longer purchase or interact with the business. A high churn means that higher number of customers no longer want to purchase goods and services from the business.
  
It is an integral parameter for the organization since acquiring a new customer could cost almost 7 times more than retaining an existing customer.
  
The ability to be able to predict that a certain customer is at a very high risk of churning, while there is still some time to do something significant about it, itself represents a great additional potential revenue source for any business.
  
> Apart from the usual reasons of poor service and monetary issue, there are many different types of churn which requires in-depth business understanding before any analysis can be done.
> [For more details about Customer churn specifically related to Telecom industry, go through my blog.](https://inblog.in/Customer-Churn-Analysis-5PyOaWdwDF)

[(Back to top)](#table-of-contents)


## Business case

A telecom company wants to overhaul their business strategy. In order to do so the sales manager has requested these specific details: 
1. **Summarizing the profile of a churner compared to the entire database.**

2. **Churn risk associated with each customer.**

3. **Major factors leading to churn.**

4. **Critical Segment of Churning customers.**

5. **Interactive dashboard for each customer displaying  the necessary details.**

[(Back to top)](#table-of-contents)



## Requirement Gathering and Documentation

As a business analyst the first step would be to gather all the requirements necessary for the analysis and document it. 

Documentation is the most critical part of a project development as it is the foundation of all further project deliverables describing what inputs and outputs are associated with each process function. 

I have created a Business Requirement documentation for our business case as shown below. (PS: Names are changed due to confidentiality issues).

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/BRD-Churn.png" width="1050" title ="Business Requirement Document">
  <em>Business Requirement Document</em>
</p>

[(Back to top)](#table-of-contents)


## Data Summary and Exploratory Analysis

Data Acquisition plays a crucial role in the final result of our analysis. As a business analyst, it is of paramount importance that we know what we need. Based on the business case and the business requirement we filter out the required data.

The provided dataset consists of the information below:

- Demographic information about customers including gender, age, marital status.

- Customer account information including the number of months staying with the company, paperless billing, payment method, monthly charges, and total charges.

- Customer usage behavior, such as streaming TV, streaming movie.

- Services that the customer signed up for: phone service, multiples, internet service, online security, online backup, device protection, and tech support.

- Customer churn where the customer left within the last month.


After data acquisition, the raw data needs to be cleaned and transformed before we can try and draw any insights from it. We can use multiple platforms to do so, but I have implemented the process using Power BI.

The steps involved in Data Pre Processing are:

1. **Handling Missing Values**: Based on the number of missing values, we can choose different strategies to deal with them.

2. **Data Validation**: We need to check the data types of each column and make sure they are compatible with our business understanding.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/data_load.png" width="1050" title="Data Connected to Power BI">
  <em>Data Connected to Power BI</em>
</p>

Once the data source is connected we have to perform these cleaning and transformation steps in Power Query Editor. Based on the raw file I have created two different tables,

1. **Complete Subscriber database.**

2. **Complete Churner Database.**

This is because one of the customer's demand is to compare the profiles of a churners with the total subscribers.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/query_editor.png" width="1050" title="Complete Subscriber base and churned subscriber base">
  <em>Complete Subscriber base and churned subscriber base</em>
</p>

1. **Handling Missing Values**: 
  In our dataset we have only 11 rows with missing values out 7043, so deleting those rows won't have any significant impact on our result. The blank rows are removed by choosing the remove empty option in data filtering.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/missing_value.png" width="1050" title="Missing Value Treatment">
  <em>Missing Value Treatment</em>
</p>

Now after analyzing the dataset we can see that all the data fields are in correct format. Once the Data transformation steps are completed we will Load the cleaned data in our model using the close and apply  option in Power Query Editor so that we can create a schema diagram.

In order to analyze the churning risk of a subscriber we need to create models to predict whether a subscriber will churn or not based on its accuracy. This can be done using Machine Learning techniques. Here, I have used Logistic recognition to do the modeling. Logistic regression models need to be scripted in programming languages like R or Python. But Power BI will help us in creating models as well. Power BI can use Python scripts to create prediction tables and probability score associated with it.

This can be done by the following steps:

1. Get Data 

2. Choose Python Script 

3. Paste the script required for modelling

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/pythonscript1.png" width="1050" title="Python Scripting">
  <em>Python Scripting</em>
</p>

After running above script, dataset will be loaded . 

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/pythonresult1.png" width="1050" title="Loaded dataset">
  <em>Loaded dataset</em>
</p>

The Python scripting can easily be done using pre-written code snippets by adjusting the parameters and variables according to our use case and understanding the concept of Logistic regression.

Final Code that we will run :

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/python_script2.png" width="1050" title="Python Script for risk prediction">
  <em>Python Script for risk prediction</em>
</p>

After running above script you will get below output :

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/python%20result2.png" width="1050" title="Prediction Data Loaded using Python">
  <em>Prediction Data Loaded using Python</em>
</p>

We can then use Power Query Editor to merge the variables from cleaned initial data and the prediction values and then can create new variables to show the Prediction Probabilities.

In order to get the Risk Category we use conditional column as

- **IF Probability of churn less than 40% then non risky,**

- **between 40% to 60% : Low Risky,**

- **60% to 80%: Risky,**

- **Greater than 80%: High risky**

The final table looks like this

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/prdicted_data.png" width="1050" title="Predicted Data ">
  <em>Predicted Data </em>
</p>

### Data Modeling:

Once the dataset is loaded in Power BI Desktop, we have to create the schema diagram using the star schema mechanism. The Customer ID field of both the Transformed and Predicted table are connected on a one to one relationship as shown below.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/schema_diagram.png" width="1050" title="Schema Diagram">
  <em>Schema Diagram</em>
</p>

Once the data modelling is done we have to create certain calculated column which would allow us to better depict the Customer ID in the Customer profile reporting. Here the first 4 characters of Customer ID is extracted and a new column is created for better visual representation.

``` 
ID = LEFT('Telco-Churn-Analysis-Predictions'[customerID], 4)
```

We will start the exploratory analysis and dashboarding together in Power BI.

[(Back to top)](#table-of-contents)


## Dashboarding

As per the client's demands and based on the acceptance criteria we have created six separate dashboard namely 

- **Home**

- **Summary**

- **Churn Reasons**

- **Churn Factors**

- **Customer Details**

- **Ask a question** 

> These dashboard together form the Customer Churn Analysis Report.

The background image as well as the layout customization plays a vital role in increasing the aesthetic appeal of any dashboard or visual. Power BI has certain limitation in this regard and hence we use a graphic designing tool called **Snappa**.

### 1. Home:

The Home Page depicts all the dashboard names as well as buttons devised for easier page navigation. This helps the end user to get to the specific dashboard and get the required information.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/homedb.png" width="1050" title="Home Dashboard ">
  <em>Home Dashboard </em>
</p>

### 2. Summary:

The Summary dashboard contains the visuals showing the relationship of all the acquired user data with its effect on churning. Here, we perform the actual exploratory data analysis to get an idea of some peculiar features of a churner when compared with the entire subscriber base.

We have created a subdivision in our dashboard comparing certain characteristics of churners and all the subscribers. We have performed univariate and bivariate analysis to extract the insights from the subscriber data. The salient features of the dashboard are:

1. Card Visual to depict total number of subscriber and the churner. **The data shows that roughly 27% of the subscriber base have churned.**

2. **Demographic** comparison of all subscribers and churners are made like Gender division of all subscriber and churner,  Senior citizen categorization, Partner categorization as well as the tenure of a subscriber and churner with the organization using Donut Chart, Funnel Chart and Bar chart. From the visualization, we can conclude that:

   2.1. **Gender has no impact on churning.**

   2.2: Subscribers in the **tenure bucket of 0-20 i.e. NEW customers are churning much more as** compared to long term customer.

   2.3: Subscribers who **do not have partners are 40% more likely to churn** as compared to partnered subscriber.

   2.4: Higher percentage (around **11% more) of Senior citizen are in the churner base** then in the subscriber base.

3. In the **Phone Service  and usage data** we can infer that:

   3.1 Subscribers with **no online security are 30 % more likely to churn.**

   3.2: Subscribers **without any tech support assistance are 32% more likely to churn.**

   3.3: Subscribers on **fiber optics are 25 % more likely to churn as well.**

4. In the **Contract and Payment data** we can infer that:

   4.1 Subscribers on **monthly plan form 90% of all the churners** and are very highly likely to churn as compared to just 55% of all subscriber.

   4.2: Subscribers paying through **electronic cheques are 24% more likely to churn.**

   4.3: **Churner's average monthly revenue is $10 more than monthly ARPU.**


<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/summarydb.png" width="1050" title="Churn Summary Dashboard">
  <em>Churn Summary Dashboard</em>
</p>

### 3. Churn Reasons:

The Churn Reason dashboard contains the categories of a churner and the revenue details associated with them. This dashboard satisfies the client's demands of categorizing churners based on their likelihood of churn. We have created a custom categories based on the churn probabilities of each customer and then binned them in Non Risky, Less risky, Risky and High Risky customers. The visual depicts:

1. Total no of **Risky customer is 2057.**

2. **Average risk score**(percentage probability of churning) is **26.57**.

3. **Revenue at risk** because of these customer is **$2.42 Million**.

4. Of all the risky subscribers, **692 are highly risky** and requires immediate attention followed by **1365 risky**.

5. Out of the total **$2.42 million at risk**, **Risky subscribers** contribute around **$2.12 million**.

>These are very important and business driving insights which will help the client to focus on the most critical subscriber base and also develop strategies to minimize their at-risk revenue.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/reasondb.png" width="1050" title="Churn Reason and Categorization">
  <em>Churn Reason and Categorization</em>
</p>

### 4. Churn Factors:

The most important aspect of a business analysis project is to find the root cause of the client's problem. In our project, we have to determine the churn factors. Normally, determining the actual factors responsible for churn is a tedious data science challenge. However Power BI takes care of this issue for us and we can find out the churn factors using the  **Key Influencer**  visual.

**Key Influencers**  visual is a AI driven visual that helps to find and establish the factors that drive a metric based on their relative importance. It helps to understand the elements which influence the specified target variables. We use the churn field as the  _'analyze by'_ and all the other fields in _'explain by'_ option  which explains the churn (Yes/No) based on the subscriner data. In the visual below it can be observed that

1.Being in  **Monthly Contract**  **increases**  the  likelihood  of  **churning**  by  **6.3 times.**

2.  **No Online Security increases** the likelihood of  **churning** by  **3.63 times.**

3. **No tech Support**  increases the likelihood of  **churning**  by  **3.51 times.**

... and many more such factors can be observed.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/factordb.png" width="1050" title="Most Importand factors related to churn and the corresponding likelihood score">
  <em>Most Importand factors related to churn and the corresponding likelihood score</em>
</p>


Another very important visual offered by Power BI for AI driven solution is the  **Top Segment**  visual. The top segment visual creates certain  **segments of customer**  i.e. **customer clusters satisfying a set of criteria.**

It also shows the **churn likelihood**  of customers in **these segemnt**  when compared with the **entire churner base.**

In our dashboard, Power BI has created five such segment.

1. The first Segment consist of people whose:

-   **Contract** is  **Monthly**.
-   **Internet Service**  runs on **Fiber optic**.
-   **Tenure bin**  is from  **0-20 months**.
-   **Total Charges** is  **less**  than  **$347.65**  or  **greater** than  **$3273.55**
-   **Subscriber** in  these  **segment is 75.6% likely to churn**  which is **49% more**  than average  churn rate.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/segmentdb.png" width="1050" title="Potential Churner characterstic: Segment 1">
  <em>Potential Churner characterstic: Segment 1</em>
</p>

2. The second Segment consist of people whose:

-   **Contract** is  **Monthly**.
-   **Internet Service**  runs on **Fiber optic**.
-   **Tenure bin**  is from  **0-20 months**.
-   **Total Charges** is  **greater** than  **$347.65**  or  **less**  than  **$3273.55**
-   **Subscriber** in  these **segment is 59.7% likely to churn** which is **33% more** than average  churn rate.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/segment2db.png" width="1050" title="Potential Churner characterstic: Segment 2">
  <em>Potential Churner characterstic: Segment 2</em>
</p>

3. The third Segment consist of people whose:

-   **Contract** is  **Monthly**.
-   **Internet Service**  runs on **not Fiber optic**.
-   **No online security**.
-   **Total Charges** is  **less**  than  **$347.65**  or  **greater**  than  **$3273.55**
-   **Subscriber** in  these **segment is 51.3% likely to churn** which is **25% more** than average  churn rate.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/segment3db.png" width="1050" title="Potential Churner characterstic: Segment 3">
  <em>Potential Churner characterstic: Segment 3</em>
</p>

4. The fourth Segment consist of people whose:

-   **Contract** is  **Monthly**.
-   **Internet Service**  runs on **Fiber optic**.
-   **Tenure bin**  is  **not** from  **0-20 months**.
-   **Payment Method** is  **Electronic check**
-   **Subscriber** in  these **segment is 46.2% likely to churn** which is **20% more** than average  churn rate.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/segment4db.png" width="1050" title="Potential Churner characterstic: Segment 4">
  <em>Potential Churner characterstic: Segment 4</em>
</p>

5. The fifth Segment consist of people whose:

-   **Contract** is  **Monthly**.
-   **Internet Service**  runs on **Fiber optic**.
-   **Tenure bin**  is  **not** from  **0-20 months**.
-   **Payment Method** is  **not Electronic check**
-   **Subscriber** in  these **segment is 31.2% likely to churn** which is **5% more** than average  churn rate.


<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/segment5db.png" width="1050" title="Potential Churner characterstic: Segment 5">
  <em>Potential Churner characterstic: Segment 5</em>
</p>

>These visuals makes it tremendously easy for the client to target their different business strategies at diffent sections of subscriber resulting in the least amount of churn and most return on investment.


### 5. Customer Details:

The Customer Details dashboard acts as a Customer Profile portal with all the necessary details of the customer like:

-   **Personal Details:** ID, name, gender and age
-   **Phone Service Details:**  Device Protection, Online security, Internet Service etc
-   **Contract details:** Contract type and payment method
-   **Other details:**  Senior Citizen check and tenure in the company

The dashboard also contains the  **Risk Category**,  **Total revenue**  and  **Churn index**(percentage probability of churning)

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/profiledb.png" width="1050" title="Customer Profile">
  <em>Customer Profile</em>
</p>

>The visual gives a perfect snapshot of the customer details with filters based on ID. This will be very useful for a Incident Management team as well as service evaluation teams.


### 6.Ask a question:

The '_Ask a question_' visual comes in handy during a business evaluation meeting or a strategy development meetings. This visual gives the details of churner based on any independant data field involving any number of calculations.

Since not every visual can be depicted in a limited-size dashboard, the '_Ask a question_' visual develops the necessary graph as and when it is needed.

<p align="center">
  <img src="https://github.com/ankitkash101/Customer-Churn-Analysis/blob/main/aqadb.png" width="1050" title="Ask a Question visual">
  <em>Ask a Question visual</em>
</p>

>Once the final report is prepared, we publish the dashboard to Power BI service and schedule automated data refresh based on the client's specification.


[(Back to top)](#table-of-contents)



## Conclusion

All the tasks mentioned in the BRD has been completed as per the specified acceptance criteria. The project is then evaluated and continuously monitored for any future changes. This concludes a Business Analysis project of Customer Churn Prediction analysis.



[(Back to top)](#table-of-contents)






