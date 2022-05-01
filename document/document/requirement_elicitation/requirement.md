### Functional requirements:
The specified functional requirements for the topic POS are presented in this section. The
broad needs for the entire system are presented first. Following needs have been delineated
to the extent feasible based on their relevance to the users of system users, namely clients,
clerks, cooks, and supervisors.

GENERAL REQUIREMENTS:
- The system should allow non-direct contact between Clerks and Customers
- The system should be implemented using Web technology and QR code, so customers will not have to install apps
- The system should be usable from a mobile device, a tablet device or a normal computer/ laptop
- The system should be extendable to use in multiple restaurants in the future
- The current transactions is about 300 orders per day

CUSTOMER

- The customers shall be able to engage the menu of restaurants by scanning the QR code placed on their tables or logging in with their own accounts.
- Customers will be able to begin placing an order by picking any of the available items.
- Customers will be able to change the quantity of an item after they have selected it.
- Customers will be able to change the quantities, requests, and removal of products while on the menu page
- The customers shall be able to submit their orders.
- The customers shall be able to go back to the menu anytime to continue picking items.
- The customers shall be alerted via the notification of system in case an item is not available
- Customers will be able to request assistance via the web at any time (for special recommendations, cleaning, etc.).
- The customers shall be able to search for the item on the menu page.
- Customers will be able to select payment options (internet banking, credit card, or cash) before placing orders on the confirmation page.
- If the customers choose for the internet banking method, they shall be able to select their bankcard type then confirm their payment.
- The customers shall be able to send feedback on quality of the foods,attitude of staff ,... right on the website after finishing the meals.

CLERK: 
- The clerks shall be able to log in and log out their own account on their tablets
- If an order is placed, the clerks will be notified via their tablets.
- The clerks shall be alerted if the item ordered from the kitchen is ready.
- The clerks shall be alerted if the item ordered is not available.
- The clerks will be able to use their tablets to record an item that they successfully deliver to the table.
- Clerks who process contact payments (credit cards and cash) will use their tablets to keep track  of them.

CHEF:
- The chef shall be able to confirm an order of customer through the display
- If an item is not available through the display, the chef will be able to inform the consumer.
- Through the display, the chef will be able to signal when a order of customer item is ready to be served.

### Non-functional Requirements:
This part presents the identified non-functional requirements for Restaurant POS 2.0. The subcategories of non-functional requirements given are safety, security and performance
SAFETY:
- When problems occrur ( such as system crash or power failure), the system must restore the previous condition.
- When tablets fail to send messages or when assigned clerks are disconnected from the tablet, the system will flag them.
- The system must be able to display a menu to take orders at all time.
- To monitor the condition of tablet, the system sends periodic 12 30-second sustaining signals between the tablet and the server.

SECURITY:
- At any given time, a clerk will be limited to logging onto only one tablet.
- The WPA2-PSK password for wireless communication must have at least 80 bits of bit strength and be changed at least once a month.
- A clerk password for tablet login must have at least 64 bits of bit strength and be changed every three months.
- When customers scan QR code to access to the website, they do not need to login.
- Any other users must have username and password to log in.

PERFORMANCE
- The server must be able to handle at least an arbitrary number of simultaneous connections.
- The server must be able to process an unlimited number of orders at the same time.
- The server must be able to support a maximum of 300 orders one in a day.

![](https://www.linkpicture.com/q/3_1284.png)
