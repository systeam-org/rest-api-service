# systeam-backend-api
The repository for backend APIs for SysteamBiz shipment solution.

- University Name: San Jose State University (http://www.sjsu.edu)
- Course: Cloud Technologies
- Professor: Sanjay Garje (https://www.linkedin.com/in/sanjaygarje)
- Students:
  - Praveen Kumar Thakur (https://www.linkedin.com/in/praveen-kumar-thakur-aa38301a)
  - Amit Vijapure (https://www.linkedin.com/in/amitvijapure)
  - Dhwani Shanghvi (https://www.linkedin.com/in/dhwani-sanghvi)
  - Jignesh Madhani (https://www.linkedin.com/in/jdmadhani)
  
### Project Introduction

  **In this project, we are going to provide two portals i.e. Customer portal and Vendor portal.**

  - **Customer Portal:** On this portal, customer can provide shipping details such as date, total weight, dimensions, source and destination pin codes. And using these details, system will provide best possible price. After that customer can confirm the order. Customer can also see the list of orders which they have placed.  

  - **Vendor Portal:** On this portal, vendors can provide shipping rates for a given source, destination and weight. Vendor can also see the list of orders.

### Architecture Diagram:
  ![Architecture Diagram](Architecture-Diagram.png)

### Sample Demo Screenshots
  - Get Estimate
  ![Get Estimate](images/get_estimate.png)
  ![Get Estimate with Map](images/get_estimate_map.png)

  - Place Order
  ![Place Order](images/place_order.png)
  
  - Order List
  ![Order List](images/order_list.png)
  
  - Least shipment price
  ![Least shipment price](images/least_prices.png)
  
  - Update Price
  ![Update Price](images/update_price.png)
  
  - Chatbot
  ![Chatbot](images/chatbot.png)
  
### Pre-requisites Set-up
  - AWS S3
  - AWS Cloudfront
  - AWS Route53
  - Global Table Configuration for DynamoDB Tables
  
### List of required software to download locally
  - Python v3.7  
  - Docker Desktop
  - AWS SAM cli
  - Java Runtime v1.8 (Needed to run DynamoDB locally)
  - DynamoDBLocal.jar (http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Tools.DynamoDBLocal.html)
   
### How to set up and run project locally?
  - **Running DynamoDB locally:**
    - To run DynamoDB locally run download jar from: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.DownloadingAndRunning.html
    - Run following command:     
      *java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb*
  
  - **Run the lambda function locally:**
    - Start Docker Desktop    
    - Run following command from git root directory:     
      *sam local start-api*
