**Background Information:**

3-1-1 connects Baltimore citizens, businesses & visitors with a vast array of city services, programs and information.  Either by a live agent-assisted phone call or through the self-service web or mobile portal, 3-1-1 allows customers to report a problem, request a service, check the status of a previously submitted service request, and obtain information regarding City programs or events. Constituents may call 3-1-1 to file non-emergency police reports.

<img width="170" alt="image" src="https://user-images.githubusercontent.com/91503635/172508351-4f033f43-de43-4408-9d81-ecbbbe3e1b26.png">
fig: The Official logo of 3-1-1 service in Baltimore City


**Severity of the Issue:**
I was always interested in working on open datasets and when I found out about 3-1-1 services in Baltimore, I did further research and found the different aspects of 3-1-1 services. 311 is how citizens in a community can help bring awareness non-emergency issues and make sure authorities are aware that they exist. It is very difficult for authorities to know about the minor services that are needed to be done in any field. 3-1-1 is as important as 9-1-1 in terms of non-emergency complaints or issues. 

**Overview:** 
Firstly, I would like to find the statistics of the data and later try to find better attributes for model building. Also, I would like to find the outcome of service request based on which agency does the request belongs. For example electricity issues come under BGE, unattended vehicles in driveway comes under Transport agency. 


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

I am planning to use Method Received(how did the customer created the service request), Agency(Type of Agency the service request belongs to) and try to predict the Outcome of service request. 

Models we are going to use:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Neural Networks

**Evaluation Metrics to be used:** 
I am planning to evaluate the metrics such as f1-score, recall, accuracy, precision and ROC-AUC curves. I am planning to improve the performance of the model after determining the best evaluation metric obtained. 

**Outcomes:** 

-	My main motive is to get a firm understanding on effective ways to handle real world data such as open datasets and all. 
-	To apply various Machine Learning models to classify the outcome.
-	To perform meaningful Exploratory Data Analysis and stating the outcomes.
-	Analyzing and visualizing the data.
-	Applying various Classification techniques
-	Usage of various evaluation metrics to determine the performance of the model. 
