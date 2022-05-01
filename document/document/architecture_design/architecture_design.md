# Task 3: 
## 3.1 An architectural approach

The technology is built to be very scalable and may be used in a wide range of restaurants around
the world.

• The restaurant owns the domain name "storeabc.com," which users use to access
the website.

- For the two primary sorts of users, there are two sub-domains: ”staff. storeabc.com”
for employees and ”www. storeabc.com” for customers.
– Laptops and mobile phones are examples of user devices. Client devices’ browsers
send queries to the URL and AWS Rout 53, a domain name service redirect, and
receive responses from AWS CloudFront, a CDN server, which receives and renders
resources.

• Server that hosts the CDN
- The CDN server will host the resource on AWS S3, which is available in 27 regions.
The precise host region will be picked based on the restaurant’s location to maximize
resource delivery time.
- This server’s resources comprise html, javascript, and pictures, which are used to
respond to requests from users’ browsers.
- All incoming requests will be sent to https requests.
- The response to all outbound requests will be https.
- When a user interacts with a website in their browser, the browser renders static
response files from the CDN server and sends REST API queries to API Gateway.

• AWS Lambda running on Nodejs 14.6 is the compute unit.
- The back-end service is created using a serverless architecture and includes four core
services: viewing meals, making payments, placing orders, and confirming meals.
- These services will make a request to a DynamoDB database cluster to get the data
they require, then process it and send the results to the client.
– The put order service uses AWS SQS (simple queue service) to keep track of orders
that are waiting to be processed. Confirm-Meal Service is triggered when items in
SQS are put in or taken out.

• AWS DynamoDB is used to host the database cluster.
- This strategy places the partition key on the Domain Name. Our entire system is capable of supporting a big number of restaurants while maintaining excellent availability.
Only the IP from the compute server will be accepted for inbound and outgoing traffic.
[![](https://www.linkpicture.com/q/1_7.png)](https://www.linkpicture.com/view.php?img=LPic626e54cb03ccc1042050397)

## 3.2 An implementation diagram
![](https://www.linkpicture.com/q/2_5.png)

