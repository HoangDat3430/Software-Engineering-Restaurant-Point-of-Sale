# POS SYSTEM (Software Engineering Assignment)
**Task 1:** Requirement Elictation 
**Task 2:** Activity, Sequence and Class Diagram 
**Task 3:** Architecture design 
**Task 4:** Implementation

## Members
- Hoàng Mạnh Đạt (1952313)
- Nguyễn Bình Minh (1952846)
- Phạm Hữu Thiên (1852755)
- Trần Trung Hiếu (1952684)
- Lê Bá Thành (1852739)

## Task 1
### Task 1.1
#### Context of Project
Restaurant POS 2.0 is a system where customer interacts with restaurant clerks.POS systems providing method for customers to do many things. Restaurant clerks and
chefs are able to deliver dishes with minimum interacts with the customer in the Covid-19 pandemic

#### Relevant Stakeholders
- Customer
- Chef
- Clerk
- Manager

#### Expected Jobs
– The system should allow non-direct contact between Clerks and Customers.
– The system should be implemented using Web technology and QR code, so customers will not have to install apps.
– The system should be usable from a mobile device, a tablet device or a normal computer/laptop.
– The system should be extendable to use in multiple restaurants in the future.
– The current transactions is about 300 orders per day.

#### Scope of Project
– The Restaurant POS 2.0 system is used in various kind of restaurant, coffee shop, etc. to give method for customer to having a table reservation, ordering food, making payment, etc. . . manager to manage the sales, clerk to check the orders.
– These activities are operated in a website, no apps need to be installed to use this systems.
– The user interface has the restaurants’ menu, ways to communicate with restaurant’s clerks.

### Task 1.2
The following section presents the complete set of functional and nonfunctional requirements for the subject Restaurant POS 2.0.
• Functional requirements concentrate on the relationships between the overall system and the users: supervisors, customers, clerks and chefs.
• The non-functional requirements revolve around the interface, safety, security, qualification, operation, maintenance and performance.

#### Functional requirements:
The specified functional requirements for the topic POS are presented in this section. The
broad needs for the entire system are presented first. Following needs have been delineated
to the extent feasible based on their relevance to the users of system users, namely clients,
clerks, cooks, and supervisors

#### Non-functional requirements:
This part presents the identified non-functional requirements for Restaurant POS 2.0. The
subcategories of non-functional requirements given are safety, security and performance

#### Use-case diagram for the whole system

![](https://i.imgur.com/Lmcp1yR.png)


### Task 1.3

## Task 2
### Task 2.1 Activity Diagram

![](https://i.imgur.com/tYAA2F9.png)

### Task 2.2 Sequence diagram

![](https://i.imgur.com/8lwAGJX.png)



### Task 2.3 Class diagram

![](https://i.imgur.com/PEcTBOT.png)


## Task 3
Architecture design  
The team needs to perform the following tasks:

- Task 3.1. Describe an architectural approach you will use to implement the desired system
- Task 3.2. Draw an implementation diagram for Major (not all) functional requirements

### Task 3.1 An architectural approach

The technology is built to be very scalable and may be used in a wide range of restaurants around the world.
• The restaurant owns the domain name "storeabc.com," which users use to access the website.
– For the two primary sorts of users, there are two sub-domains: ”staff. storeabc.com” for employees and ”www. storeabc.com” for customers.
Assignment 1 for Software Engineering - Academic year 2021 - 2022 Page 12/14 Ho Chi Minh City University of Technology Faculty of Computer Science and Engineering
– Laptops and mobile phones are examples of user devices. Client devices’ browsers send queries to the URL and AWS Rout 53, a domain name service redirect, and
receive responses from AWS CloudFront, a CDN server, which receives and renders resources.
• Server that hosts the CDN
– The CDN server will host the resource on AWS S3, which is available in 27 regions. The precise host region will be picked based on the restaurant’s location to maximize resource delivery time.
– This server’s resources comprise html, javascript, and pictures, which are used to respond to requests from users’ browsers.
– All incoming requests will be sent to https requests.
– The response to all outbound requests will be https.
– When a user interacts with a website in their browser, the browser renders static
response files from the CDN server and sends REST API queries to API Gateway.
• AWS Lambda running on Nodejs 14.6 is the compute unit.
– The back-end service is created using a serverless architecture and includes four core services: viewing meals, making payments, placing orders, and confirming meals.
– These services will make a request to a DynamoDB database cluster to get the data they require, then process it and send the results to the client.
– The put order service uses AWS SQS (simple queue service) to keep track of orders that are waiting to be processed. Confirm-Meal Service is triggered when items in
SQS are put in or taken out.
• AWS DynamoDB is used to host the database cluster.
– This strategy places the partition key on the Domain Name. Our entire system is capable of supporting a big number of restaurants while maintaining excellent availability.
Only the IP from the compute server will be accepted for inbound and outgoing traffic

![](https://i.imgur.com/3cSmaqv.png)


### Task 3.2 An implementation diagram
![](https://i.imgur.com/9oX3Nfv.png)

## Task 4

- Task 4.1: Setting up. The team creates an online repository (github, bitbucket, etc) for version control.
- Task 4.2: Adding documents, materials and folders for Requirement, System modelling and Architectural design. Use the selected version control system to report the changes to these files/ folders
- Task 4.3: Implement a Minimum Viable Product (MVP) for the menu screen in Figure 2 and demonstrate the result. MVP means that do the least to be able to demonstrate. That means at this stage, no need for a database to store all menu items, customers, etc. Data can be hard coded in code files.
