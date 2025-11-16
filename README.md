# Grocery-store inventory
# Tools used
This analysis was conducted entirely with microsoft excel. Within microsoft excel, power query was applied for cleaning data and power pivot was used for used for analysing and modelling. 
# Data cleaning
This was conducted using power query; here improper texts were transformed aptly, every field carried their various and correct data type.
# Analysis
Proper analysis of the data set aided correct answers to the various questions asked; The first question was on the average stock quantity/product category: This was found by creating a new measure formula =AVERAGE(Grocery_Inventory_new_v1[Stock_Quantity]).

For the third question which is on finding the product with the longest shelf life, multiple calculated columns where added to help us achieve the required objective. firstly, a calculated column(Recent date) was included to reveal the latest dates for each product, formula used: =CALCULATE(MAX(Grocery_Inventory_new_v1[Date_Received]),
FILTER(Grocery_Inventory_new_v1, Grocery_Inventory_new_v1[Product_Name] = EARLIEST(Grocery_Inventory_new_v1[Product_Name]))). 

For shelf life; =Grocery_Inventory_new_v1[recent date received]-Grocery_Inventory_new_v1[Expiration_Date] was used.

Finally, the formula;
=IF(Grocery_Inventory_new_v1[recent date received]=Grocery_Inventory_new_v1[Date_Received],Grocery_Inventory_new_v1[Shelf time],0) gave the required answer.

For question five, the neccessary fields we subjected to data forecasting, this displayed appropriate trends which was vital in predicting seasonal demands for te various product categories.

Questions
1. What is the average stock quantity available per product category? The average stock quantity available per product category are;
   Bakery(56), Beverages(50), Diary(58), Fruits & vegetables(55), Grains & pulse(50), Oils & fats(53), Seafood(62). 

2. Which suppliers contribute the most to total product inventory? KATZ contributes the most to total product inventory.

3. Which products have the longest shelf life before expiration, and how does that impact sales? SALMONS has the longest shelf life, having 
   a positive impact on sales as there is a reduced risk of stockout.

4. Which products are most likely to run out of stock based on last reorder levels? Considering last reorder levels the following products
   will most likely run out of stock: Banana, Lettuce, Vanilla Biscuit, All-Purpose Flour, Powered Sugar, Garlic, Herbal Tea.

5. Can we predict seasonal demand for different product categories based on sales volume trends?
 >BAKERY: There is an upward trend in sales volume from the 12th month, implying that demand will also increase overtime.

 >BEVERAGES: There's a slight increase in sales volume from the 12th month, implyimg that demand will slightly increase overtime.

 >DIARY: From the 12th month there is a sharp decline in sales volume but a likelihood of increase overtime, implying that
   demand will greatly decrease from the 12th month but there is a possibility of increased demand overtime.
 
 >FRUITS & VEGETABLES: There's a slight decline in sales volume from the 12th month but a likelihood of increase overtime,
   implying that demand will slightly drop from the 12th month but possibly increase overtime.

 >GRAINS AND PULSES: There's a slight decline in sales volume from the 12th month and an equal increase overtime, implying
   that demand will slightly drop from the 12th month and also possibly increase overtime.
 
 >OILS & FATS: There is a sharp upward trend in sales volume from the 12th month, implying that demand will increase
   continuously from the 12th month.

 >SEAFOOD: From the 12th month there is a sharp upward trend in sales volume and a also decline overtime, implying that
   demand will greatly increase from the 12th month and there is a possibility of decreased demand overtime. 
   
6. What are the optimal reorder levels for high-demand products to prevent stockouts?

 

