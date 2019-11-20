**Mongo DB**

*1. What are the different collections in the Northwind database?*
```
> show collections
categories
customers
employee-territories
northwind
order-details
orders
products
regions
shippers
suppliers
territories
```
*2. How many documents are in the "categories" collection?*
```
> db.categories.count()
8
```
*3. How many documents are in the "orders" collection?*
```
> db.orders.count()
830
```
*4. How many orders were handled by the person with EmployeeID number 8?*
```
> db.orders.count( {EmployeeID: 8} )
104
```
*5. What is the last name of the employee who has the EmployeeID number 1?*
```
> db.employees.find( { EmployeeID: 1 }, { _id: 0, LastName: 1 } )
{ "LastName" : "Davolio" }
```
*6. What are the EmployeeID numbers on orders which have an OrderID less than 10300?*
```
> db.orders.distinct( "EmployeeID", { "OrderID": { $lt: 10300 } } )
[ 3, 4, 6, 5, 9, 1, 8, 2, 7 ]
```
*7. What are the Company Names of the suppliers?*
```
> db.suppliers.distinct( "CompanyName" )
[
	"New Orleans Cajun Delights",
	"Cooperativa de Quesos 'Las Cabras'",
	"Tokyo Traders",
	"Exotic Liquids",
	"Grandma Kelly's Homestead",
	"Pavlova",
	"Specialty Biscuits",
	"Mayumi's",
	"Refrescos Americanas LTDA",
	"PB Knäckebröd AB",
	"Plutzer Lebensmittelgroßmärkte AG",
	"Heli Süßwaren GmbH & Co. KG",
	"Nord-Ost-Fisch Handelsgesellschaft mbH",
	"Formaggi Fortini s.r.l.",
	"Norske Meierier",
	"Bigfoot Breweries",
	"Svensk Sjöföda AB",
	"Aux joyeux ecclésiastiques",
	"New England Seafood Cannery",
	"Leka Trading",
	"Zaanse Snoepfabriek",
	"Karkki Oy",
	"Lyngbysild",
	"G'day",
	"Ma Maison",
	"Pasta Buttini s.r.l.",
	"Escargots Nouveaux",
	"Gai pâturage",
	"Forêts d'érables"
]
```
*8. How many suppliers are there?*
```
> db.suppliers.count()
29
```
*9. What is the supplier ID and phone number for the supplier in Boston, Mass.? Be sure NOT to include the ID of the document...*
```
> db.suppliers.find( {City: "Boston"}, {_id: 0, SupplierID: 1, Phone: 1} )
{ "SupplierID" : 19, "Phone" : "(617) 555-3267" }
```
*10. What employee is responsible for the largest number of orders, and for how many orders is that employee responsible?*
```
>  db.orders.aggregate( [ { $group : { _id : "$EmployeeID", count : { $sum : 1 } } }, { $sort : { count : -1 } }, { $limit : 1 } ] )
{ "_id" : 4, "count" : 156 }
```
*11. How many territories have the RegionID value of "2"?  What are their territory descriptions? Be sure NOT to include the ID of the document, and ONLY show the territory descriptions.*

*12. What is the phone number of the shipper with the company name "United Package"? Be sure NOT to include the ID of the document in the output, ONLY the phone number.*


BONUS:

*13. How many documents are in the "order-details" collection?  How many in the "employee-territories" collection?*

*14. How many orders were shipped to Albuquerque, NM?  What are the order numbers? Be sure NOT to include the ID of the document in the output, ONLY the Order ID numbers.*

------------
       
**Neo4j**

*1. What are the different collections in the Northwind database?*

*2. How many documents are in the "categories" label set?*

*3. How many documents are in the "orders" label set?*

*4. How many orders were handled by the person with EmployeeID number 8?*

*5. What is the last name of the employee who has the EmployeeID number 1?*

*6. What are the EmployeeID numbers on orders which have an OrderID less than 10300?*

*7. What are the Company Names of the suppliers?*

*8. How many suppliers are there?*

*9. What is the supplier ID and phone number for the supplier in Boston, Mass.?*

*10. What employee is responsible for the largest number of orders, and for how many orders is that employee responsible?*

*11. How many territories have the RegionID value of "2"?  What are their territory descriptions? You can use two queries.  Be sure to ONLY show the territory descriptions for that query.*

*12. What is the phone number of the shipper with the company name "United Package"? Be sure to ONLY include the phone number in the result.*


BONUS:

*13. How many relationships are in the "order-details" edges set?  How many in the "employee-territories" edges set?*

*14. How many orders were shipped to Albuquerque, NM?  What are the order numbers?*
            
