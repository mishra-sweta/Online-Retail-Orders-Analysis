# Online-Retail-Orders-Analysis
SQL solution for order management functionality in an online retail store, utilizing a provided database of orders and customer information

## Queries

1. Write a query to display customer full name with their title (Mr/Ms), both first name and last name are in upper case, customer email id, customer creation date and display customer’s category after applying below categorization rules:
i.IF customer creation date Year <2005 Then Category A
ii.IF customer creation date Year >=2005 and <2011 Then Category B
iiiIF customer creation date Year>= 2011 Then Category C

Hint: Use CASE statement, no permanent change in table required. [NOTE: TABLES to be used - ONLINE_CUSTOMER TABLE]


2. Write a query to display the following information for the products, which have not been sold: product_id, product_desc, product_quantity_avail, product_price, inventory values (product_quantity_avail*product_price), New_Price after applying discount as per below criteria. Sort the output with respect to decreasing value of Inventory_Value.
i) IF Product Price > 20,000 then apply 20% discount
ii) IF Product Price > 10,000 then apply 15% discount
iii) IF Product Price =< 10,000 then apply 10% discount 

Hint: Use CASE statement, no permanent change in table required. [NOTE: TABLES to be used - PRODUCT, ORDER_ITEMS TABLE]


3. Write a query to display Product_class_code, Product_class_description, Count of Product type in each product class, Inventory Value (product_quantity_avail*product_price). Information should be displayed for only those product_class_code which have more than 1,00,000. Inventory Value. Sort the output with respect to decreasing value of Inventory_Value. [NOTE: TABLES to be used - PRODUCT, PRODUCT_CLASS]


4. Write a query to display customer_id, full name, customer_email, customer_phone and country of customers who have cancelled all the orders placed by them 

(USE SUB-QUERY) [NOTE: TABLES to be used - ONLINE_CUSTOMER, ADDRESSS, OREDER_HEADER]


5. Write a query to display Shipper name, City to which it is catering, num of customer catered by the shipper in the city and number of consignments delivered to that city for Shipper DHL 

[NOTE: TABLES to be used - SHIPPER, ONLINE_CUSTOMER, ADDRESSS, ORDER_HEADER]


6. Write a query to display product_id, product_desc, product_quantity_avail, quantity sold and show inventory Status of products as below as per below condition:
i.For Electronics and Computer categories, if sales till date is Zero then show 'No Sales in past, give discount to reduce inventory', if inventory quantity is less than 10% of quantity sold, show 'Low inventory, need to add inventory', if inventory quantity is less than 50% of quantity sold, show 'Medium inventory, need to add some inventory', if inventory quantity is more or equal to 50% of quantity sold, show 'Sufficient inventory'

ii.For Mobiles and Watches categories, if sales till date is Zero then show 'No Sales in past, give discount to reduce inventory', if inventory quantity is less than 20% of quantity sold, show 'Low inventory, need to add inventory', if inventory quantity is less than 60% of quantity sold, show 'Medium inventory, need to add some inventory', if inventory quantity is more or equal to 60% of quantity sold, show 'Sufficient inventory'

iii.Rest of the categories, if sales till date is Zero then show 'No Sales in past, give discount to reduce inventory', if inventory quantity is less than 30% of quantity sold, show 'Low inventory, need to add inventory', if inventory quantity is less than 70% of quantity sold, show 'Medium inventory, need to add some inventory', if inventory quantity is more or equal to 70% of quantity sold, show 'Sufficient inventory'

(USE SUB-QUERY) [NOTE: TABLES to be used - PRODUCT, PRODUCT_CLASS, ORDER_ITEMS]


7. Write a query to display order_id and volume of the biggest order (in terms of volume) that can fit in carton id 10 

[NOTE: TABLES to be used - CARTON, ORDER_ITEMS, PRODUCT]

8. Write a query to display customer id, customer full name, total quantity and total value (quantity*price) shipped where mode of payment is Cash and customer last name starts with 'G' 

[NOTE: TABLES to be used - ONLINE_CUSTOMER, ORDER_ITEMS, PRODUCT, ORDER_HEADER]


9. Write a query to display product_id, product_desc and total quantity of products which are sold together with product id 201 and are not shipped to city Bangalore and New Delhi. Display the output in descending order with respect to the tot_qty. 

(USE SUB-QUERY) [NOTE: TABLES to be used – ORDER_ITEMS, PRODUCT, ORDER_HEADER, ONLINE_CUSTOMER, ADDRESS]

10. Write a query to display the order_id,customer_id and customer fullname, total quantity of products shipped for order ids which are even and shipped to address where pincode is not starting with "5" 

[NOTE: TABLES to be used – ONLINE_CUSTOMER, ORDER_HEADER, ORDER_ITEMS, ADDRESS]
