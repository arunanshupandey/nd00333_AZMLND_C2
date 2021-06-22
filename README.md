# Operationalizing ML Experiments

*Overview of the project:* This project guides us to operationalize the Machine Learning pipelines. Starting with Bank Marketing datasets, an auto ml pipeline was confidered. We deployed a classification model to predict wether a person will subscribe to the services of the bank given demographic details. In the later sections, we were given a notebook where we used SDK to create, publish and make a consumption ready pipeline. 


## Architectural Diagram

The following steps were tested/ taken for submission of the project:
![image](https://user-images.githubusercontent.com/25560357/122880533-b8bde400-d357-11eb-9aed-301cbf5cdfdb.png)

1. Authentication (Was not required as it was Udacity Lab)
2. Automated ML Experiment with the banking dataset
3. Deploy the best model found
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline
8. Documentation


## 2. Automated ML Experiment with banking data sets

2.1 Registered Data Sets in ML Studio showing bank marketing dataset as available.

![image](https://user-images.githubusercontent.com/25560357/122881104-63ce9d80-d358-11eb-82d7-0dc95e37a4c1.png)


2.2 Experiment shown as complete

![image](https://user-images.githubusercontent.com/25560357/122881140-6e893280-d358-11eb-8eb5-536ab9122c08.png)


2.3 Screenshot of best model after the experiment. On the righ hand side, you can see the best model suggested is Voting Ensemble. 

![image](https://user-images.githubusercontent.com/25560357/122881227-8d87c480-d358-11eb-8aa8-2bddb9a452b7.png)

## 3. Deploy the best model found
As you can see the REST endpoints are visible and Application Insights are not enabled.
![image](https://user-images.githubusercontent.com/25560357/122881388-bc9e3600-d358-11eb-8ec7-810758391af6.png)

## 4. Enable logging
Enabled Application insights. The screenshot below shows the Application insights as True and related URL
![image](https://user-images.githubusercontent.com/25560357/122881728-156dce80-d359-11eb-9c2a-9132280403e4.png)

Finally the Enabled URL
![image](https://user-images.githubusercontent.com/25560357/122881764-21f22700-d359-11eb-9311-3def6437690e.png)


## 5. Swagger Documentation
Enabling Swagger and Python Servers : 

Executing Swagger.sh on LAB VM 
![image](https://user-images.githubusercontent.com/25560357/122881918-477f3080-d359-11eb-8a6f-5f81351a4420.png)

Python Server Up and Running : 
![image](https://user-images.githubusercontent.com/25560357/122881950-4fd76b80-d359-11eb-9bec-f42b80d2e103.png)

Swagger UI with application request and responses
![image](https://user-images.githubusercontent.com/25560357/122881993-5c5bc400-d359-11eb-8865-8f309e63ea92.png)

![image](https://user-images.githubusercontent.com/25560357/122882005-6087e180-d359-11eb-8ff5-fd82d6c701f5.png)


## 6. Consume model endpoints

I followed the steps provided in the documentation however the code "endpoint.py" was always giving 502 error. On further debugging, I copied the code given in the "consume" section of the endpoint and changed the "data" based on swagger documentation ( from the step #5 ). The endpoint_2.py is executed successfully providing the result as given in the screnshot below. 
My assumption is that the format ( order ) of the data payload is playing a part in the model and hence we are getting a failure with endpoint.py code. 

![image](https://user-images.githubusercontent.com/25560357/122882098-7a292900-d359-11eb-8b8e-48a9bc8805e7.png)


## 7. Create and publish a pipeline
Once the Notebook run is successful, it will publish the pipeline. 

![image](https://user-images.githubusercontent.com/25560357/122882534-ea37af00-d359-11eb-9492-4021c34d82a4.png)

A detailed screenshot : 
![image](https://user-images.githubusercontent.com/25560357/122882601-fde31580-d359-11eb-8f16-7177a636d0d2.png)

Screenshot showing the REST endpoint as published pipeline
![image](https://user-images.githubusercontent.com/25560357/122882674-10f5e580-d35a-11eb-9293-1f59c0e0b44d.png)

Screenshot from the notebook describing the model flow through run details

![image](https://user-images.githubusercontent.com/25560357/122882735-1e12d480-d35a-11eb-9b6f-267d50238eac.png)


## Screen Recording
Please find the link for the screencast.

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
