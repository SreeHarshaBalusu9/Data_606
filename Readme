This repository is part of my Capstone Project DATA_606 
Instructor: Dr. Chaojie Wang


**Background Information:**

3-1-1 connects Baltimore citizens, businesses & visitors with a vast array of city services, programs and information.  Either by a live agent-assisted phone call or through the self-service web or mobile portal, 3-1-1 allows customers to report a problem, request a service, check the status of a previously submitted service request, and obtain information regarding City programs or events. Constituents may call 3-1-1 to file non-emergency police reports.

**The Official logo of 3-1-1 services in Baltimore City**
<img width="170" alt="image" src="https://user-images.githubusercontent.com/91503635/172508351-4f033f43-de43-4408-9d81-ecbbbe3e1b26.png">



**Severity of the Issue:**
I was always interested in working on open datasets and when I found out about 3-1-1 services in Baltimore, I did further research and found the different aspects of 3-1-1 services. 311 is how citizens in a community can help bring awareness non-emergency issues and make sure authorities are aware that they exist. It is very difficult for authorities to know about the minor services that are needed to be done in any field. 3-1-1 is as important as 9-1-1 in terms of non-emergency complaints or issues. 

**Overview:** 
Firstly, I would like to find the statistics of the data and later try to find better attributes for model building. Also, I would like to find the outcome of service request based on which agency does the request belongs. For example electricity issues come under BGE, unattended vehicles in driveway comes under Transport agency. 

The outcome is the response from the service agency whether they completed the work and closed the service request or shifted to other related agency. There are like 44 categories of outcomes out of which which like 12 of them are occurring most frequently.

Considering only those 12 outcomes and the rest of them as "other" I had an idea of performing Encoding to convert the categorical variables into numeric variables.


**Data Source:** https://data.baltimorecity.gov/datasets/311-customer-service-requests-2019/explore 

**Unit of analysis:** Method received, Agency 

**Records to be Analyzed:** Around 450,000 

**Output Variable:** Outcome of Service Request


**Dataset Description:** 

Srrecordid: Service Record id

Srrequestnum: Service Request Number

Srtype: The type of service requested by customer

Methodreceived: Hoe the service is received either by API, Phone or Internal

Created Date: Date of the service creation

Srstatus: Present Status of the Service

DueDate: Due Date of the Service

CloseDate: Date of Closing of the particular service

Agency: Agency to which the service belongs

LastActivity: Latest activity on the request received

LastActivityDate: Date of Last Activity on the request

Outcome: Outcome of the service

Address: Address of the service

Zipcode: Zipcode of the service

Neighborhood: Neighborhood of the service area

CounsilDistrict: Council District of the Service request area

PoliceDistrict: PoliceDistrict of the Service request area

PolicePost: PolicePost to which the service request area belongs to

Latitude: Latitude of the address

Longitude: Longitude of the address

Geolocation: Geolocation of the service address

**Data Cleaning:** Some unwanted columns such as longitude, latitude are dropped as they have nothing to do with modelling and all.

Also, the rows which contains Null values are removed as they do not make any difference in further steps such as EDA and Model Building. 

The column “Policepost” contains most of its values as Null values and so the column is dropped.

Later Exploratory Data Analysis is performed on the final data followed by Model building and Model Evaluation.


**Exploratory Data Analysis:**
The pie chart which is plotted for method received shows that most of the service requests are received by Phone followed by API, System and Internal when compared to the others. 

Out of the 19 kinds of agencies present, only 10 of the agencies have a meaningfull value of requests when compared to the rest of the other agencies.

Some agencies such as Liquor Board, Public work,  BCIT, Mayor’s Office, Police department, General Services, City Council, Public Schools have almost negligible values when compared to other agencies. So, we can get better modelling results if we drop the agencies with less values. 

There are 306 kinds of service types out of which only some have a reasonable value.

The major outcome of the service request are:
- Work Completed
- Sr closed by agency specific work management request
- Work could not be completed
- SR assessed and no cause for action determined
- Work referred to another agency.

Only the outcomes with highest values are considered for model evaluation as the remaining has negligible values 

Most of the SrStatus values are “Closed” which means that the service request has been addressed and closed by specific agency.


**Model Building:**

Initially Label Encoding is performed to convert the columns outcome, method_received and agency into numeric values.

The data is then split into training and testing sets in the ratio of 67:33, respectively. 

A pipeline is built using Pipeline object from sklearn.pipeline. 

Machine Learning Pipeline includes raw data input, features, outputs, the machine learning model and model parameters, and prediction outputs.


**Model Evaluation:**

Different Regression algorithms like Decision Tree Classifier and Random Forest Classifier are fit in the pipeline as part of model building.

Grid search is performed in order to search for the best parameters using GridSearchCV() from sklearn.model_selection and the results from GridSearchCV() are analyzed.

The Decision tree Regressor accuracy score is 68%.

The accuracy score of Random Forest Regressor is found to be 73%. 
