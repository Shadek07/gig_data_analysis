# gig data analysis

Here I will share experimental results of data collected from Gig platforms such as Instacart, DoorDash, Postmates etc.


## Instacart platform

I started working as gig employee for Instacart as a shopper back in July, 2020. While I was shopping for customers, I decided to collect all possible shopping data so that later on I can do data analysis using visualization, machine learning models. Here, first I will explain the data that I have been collecting since the beginning of my gig career.

* Data format and description
The shopping data is in tabular format where each row corresponds to a “batch” order. A batch is defined by the shopping order of one or more customers from a certain store. Each batch has a certain set of attributes or columns. Now I will describe those attributes.

**date** - the date when I did shopping for the batch. one example date format is: 10/05/2020

**store_name** - the store name where I did shopping for the batch. one example is: Costco

**order_type** - There are two types of order. ‘full service’ or ‘delivery only’. In “full service” order, I have to shop and deliver for a customer. In ‘delivery only’ order, I have to go to the assigned store and pick the order which is already packaged by an instacart store employee.

**batch_accept_time** - the time during the day when I accepted the batch at Instacart Shopper app. One example to show the format is: 2:40 PM

**store_reach_time** - the time when I reached the store and started shopping for customers. Same format as batch_accept_time

**num_orders** - It denotes the number of customers I have to shop for. Usually the range of num_orders is 1-3

**num_items** - the number of total items that all the customers ordered in the batch. If order is ‘full service’, the format is ‘a/b’ where a is the number of unique items, b is the number of total units. A unique item has one or more units. If order is ‘delivery only’, the format is ‘a bags’ where a is the number of bags for all customers in the batch.

**heavy_pay** - ‘yes’ if the order is heavy-weight (around 50 lbs) or ‘n/a’

**shopping_speed** - It is defined as (seconds spent picking and verifying / items picked or replaced)

**checkout_speed** - It is defined as (seconds spent checking out and staging / items picked or replaced)

**drive_distance** - total map distance from store to all the customers locations with having a certain sequence customer’s delivery (for example first deliver to customer A, then to customer B, then C)

**dropoff_time_A** - the time when the batch order was delivered to the first customer. It has same format as batch_accept_time

 **dropoff_time_B** - The time when the 2nd customer’s order was delivered to his/her location. If ‘num_orders’ is 1, then dropoff_time_B is ‘n/a’

**dropoff_time_C** - The time when the 3rd customer’s order was delivered to his/her location. If ‘num_orders’ is <3, then dropoff_time_C is ‘n/a’

**instacart_pay_amount** - The dollar amount that instacart paid to the shopper (me) for the batch. This payment takes into account the amount of effort involved in delivering a batch, and will depend on a number of factors, including the number of items, units, weights, store type, distance. 

**tip_amount** - total tips that all the customers (1-3) in a batch gave

**peak_boost** - any dollar amount that was given to the batch by instacart due to promo offer or high need for shopper during shopper accept time









