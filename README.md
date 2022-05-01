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
– The system should allow non-direct contact between Clerks and Customers.<br>
– The system should be implemented using Web technology and QR code, so customers will not have to install apps.<br>
– The system should be usable from a mobile device, a tablet device or a normal computer/laptop.<br>
– The system should be extendable to use in multiple restaurants in the future.<br>
– The current transactions is about 300 orders per day.<br>

#### Scope of Project
– The Restaurant POS 2.0 system is used in various kind of restaurant, coffee shop, etc. to give method for customer to having a table reservation, ordering food, making payment, etc. . . manager to manage the sales, clerk to check the orders.<br>
– These activities are operated in a website, no apps need to be installed to use this systems.<br>
– The user interface has the restaurants’ menu, ways to communicate with restaurant’s clerks.<br>

### Task 1.2
The following section presents the complete set of functional and nonfunctional requirements for the subject Restaurant POS 2.0.<br>
• Functional requirements concentrate on the relationships between the overall system and the users: supervisors, customers, clerks and chefs.<br>
• The non-functional requirements revolve around the interface, safety, security, qualification, operation, maintenance and performance.<br>

#### Functional requirements:
The specified functional requirements for the topic POS are presented in this section. The
broad needs for the entire system are presented first. Following needs have been delineated
to the extent feasible based on their relevance to the users of system users, namely clients,
clerks, cooks, and supervisors
### GENERAL REQUIREMENTS: 
G01 The system should allow non-direct contact between Clerks and Customers.<br>
G02 The system should be implemented using Web technology and QR code, so customers will not have to install apps.<br>
G03 The system should be usable from a mobile device, a tablet device or a normal computer/ laptop.<br>
G04 The system should be extendable to use in multiple restaurants in the future.<br>
G05 The current transactions is about 300 orders per day.<br>
### CUSTOMER:
C01 The customers shall be able to engage the menu of restaurants by scanning the QR code placed on their tables or logging in with their own accounts.<br>
C02 Customers will be able to begin placing an order by picking any of the available items.<br>
C03 Customers will be able to change the quantity of an item after they have selected it.<br>
C04 Customers will be able to change the quantities, requests, and removal of products while on the menu page<br>
C05 The customers shall be able to submit their orders.<br>
C06 The customers shall be able to go back to the menu anytime to continue picking items.<br>
C07 The customers shall be alerted via the notification of system in case an item is not available<br>
C08 Customers will be able to request assistance via the web at any time (for special recommendations, cleaning, etc.).<br>
C09 The customers shall be able to search for the item on the menu page.<br>
C10 Customers will be able to select payment options (internet banking, credit card, or cash) before placing orders on the confirmation page.<br>
C11 If the customers choose for the internet banking method, they shall be able to select their bankcard type then confirm their payment.<br>
C12 The customers shall be able to send feedback on quality of the foods,attitude of staff ,... right on the website after finishing the meals.<br>
### CLERK:
K01 The clerks shall be able to log in and log out their own account on their tablets<br>
K02 If an order is placed, the clerks will be notified via their tablets.<br>
K03 The clerks shall be alerted if the item ordered from the kitchen is ready.<br>
K04 The clerks shall be alerted if the item ordered is not available.<br>
K05 The clerks will be able to use their tablets to record an item that they successfully deliver to the table.<br>
K06 Clerks who process contact payments (credit cards and cash) will use their tablets to keep track of them.<br>
### CHEF: 
H01 The chef shall be able to confirm an order of customer through the display<br>
H02 If an item is not available through the display, the chef will be able to inform the consumer.<br>
H03 Through the display, the chef will be able to signal when a order of customer item is ready to be served.<br>

#### Non-functional requirements:
This part presents the identified non-functional requirements for Restaurant POS 2.0. The subcategories of non-functional requirements given are safety, security and performance<br>
### SAFETY:
S01 When problems occrur ( such as system crash or power failure), the system must restore the previous condition.<br>
S02 When tablets fail to send messages or when assigned clerks are disconnected from the tablet, the system will flag them.<br>
S03 The system must be able to display a menu to take orders at all time.<br>
S04 To monitor the condition of tablet, the system sends periodic 30-second sustaining signals between the tablet and the<br>
server.<br>
### SECURITY:
E01 At any given time, a clerk will be limited to logging onto only one tablet.<br>
E02 The WPA2-PSK password for wireless communication must have at least 80 bits of bit strength and be changed at least once a month.<br>
E03 A clerk password for tablet login must have at least 64 bits of bit strength and be changed every three months.<br>
E04 When customers scan QR code to access to the website, they do not need to login.<br>
E05 Any other users must have username and password to log in.<br>
### PERFORMANCE:
P01 The server must be able to handle at least an arbitrary number of simultaneous connections.<br>
P02 The server must be able to process an unlimited number of orders at the same time.<br>
P03 The server must be able to support a maximum of 300 orders one in a day.<br>

#### Use-case diagram for the whole system

![](https://www.linkpicture.com/q/3_1284.png)

### Task 1.3  Use-case diagram and describe
| **Name:**               |   Make Payment                                                                                                                        | 
| ---                     | ---                                                                                                                                   |
| **Description:**        |   With Make Payment, customers might pay their orders                                                                                 | 
| **Preconditions:**      |   Customers need to access to Make Payment page. Customers have already placed orders.                                                | 
| **Normal Flow:**        |   1. Customers access the payment page. <br> 2. Customers view the detailed orders before payment. <br> 3. Customers choose the way for payment (payment methods: Internet Banking, Visa Card and Cash) that are available in the system.<br> 4. Customers show payment for clerks to check.              |
| **Alternative flow:**   |   By Cash <br>  3a. Notify clerk to go to the table of customer <br> Go to step 4 <br> 5a. Clerk confirms the successful transaction <br>    By Visa Card <br> 3a. Notify clerk to go to the table of customer <br> 3b. Swiping cards <br> Go to step 4 <br> By Internet Banking <br> 3a. Customers choose the Internet Banking method to pay <br> 3b. Customers fill banking account information and submit <br> 3c. Customers receive and submit OTP codes. <br> Go to step 4. |
| **Exception flow:**     |    Incorrect banking account information <br> Transaction fail <br> 3b. Ask customers to resubmit or choose other payment methods <br>      4a. Customers retry payment <br> Go to step 3                                                                                                                     |
![](https://www.linkpicture.com/q/4_921.png)

## Task 2
### Task 2.1 Activity Diagram

![](https://www.linkpicture.com/q/5_726.png)

### Task 2.2 Sequence diagram

![](https://www.linkpicture.com/q/6_974.jpg)



### Task 2.3 Class diagram

![](https://www.linkpicture.com/q/7_340.png)


## Task 3 Architecture design  
The team needs to perform the following tasks:<br>

- Task 3.1. Describe an architectural approach you will use to implement the desired system<br>
- Task 3.2. Draw an implementation diagram for Major (not all) functional requirements<br>

### Task 3.1 An architectural approach

The technology is built to be very scalable and may be used in a wide range of restaurants around the world.<br>
• The restaurant owns the domain name "storeabc.com," which users use to access the website.<br>
  – For the two primary sorts of users, there are two sub-domains: ”staff. storeabc.com” for employees and ”www. storeabc.com” for customer. Assignment 1 for Software Engineering - Academic year 2021 - 2022 Page 12/14 Ho Chi Minh City University of Technology Faculty of Computer Science and Engineering<br>
  – Laptops and mobile phones are examples of user devices. Client devices’ browsers send queries to the URL and AWS Rout 53, a domain name service redirect, and
receive responses from AWS CloudFront, a CDN server, which receives and renders resources.<br>
• Server that hosts the CDN<br>
  – The CDN server will host the resource on AWS S3, which is available in 27 regions. The precise host region will be picked based on the restaurant’s location to maximize resource delivery time.<br>
  – This server’s resources comprise html, javascript, and pictures, which are used to respond to requests from users’ browsers.<br>
  – All incoming requests will be sent to https requests.<br>
  – The response to all outbound requests will be https.<br>
  – When a user interacts with a website in their browser, the browser renders static response files from the CDN server and sends REST API queries to API Gateway.<br>
• AWS Lambda running on Nodejs 14.6 is the compute unit.<br>
  – The back-end service is created using a serverless architecture and includes four core services: viewing meals, making payments, placing orders, and confirming meals.<br>
  – These services will make a request to a DynamoDB database cluster to get the data they require, then process it and send the results to the client.<br>
  – The put order service uses AWS SQS (simple queue service) to keep track of orders that are waiting to be processed. Confirm-Meal Service is triggered when items in
SQS are put in or taken out.<br>
• AWS DynamoDB is used to host the database cluster.<br>
  – This strategy places the partition key on the Domain Name. Our entire system is capable of supporting a big number of restaurants while maintaining excellent availability.<br>
Only the IP from the compute server will be accepted for inbound and outgoing traffic<br>

[![](https://www.linkpicture.com/q/1_7.png)](https://www.linkpicture.com/view.php?img=LPic626e54cb03ccc1042050397)


### Task 3.2 An implementation diagram
![](https://www.linkpicture.com/q/2_5.png)

## Task 4

- Task 4.1: Setting up. The team creates an online repository (github, bitbucket, etc) for version control.<br>
- Task 4.2: Adding documents, materials and folders for Requirement, System modelling and Architectural design. Use the selected version control system to report the changes to these files/ folders<br>
- Task 4.3: Implement a Minimum Viable Product (MVP) for the menu screen in Figure 2 and demonstrate the result. MVP means that do the least to be able to demonstrate. That means at this stage, no need for a database to store all menu items, customers, etc. Data can be hard coded in code files.<br>
