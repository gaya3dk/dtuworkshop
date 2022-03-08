# Dataset discovery

## sales_order_header
Data discovery result: there are `Order Id` being null; PK is `Order Id`
```text
Order ID:string
Order Date:string
CustomerName:string
State:string
City:string
```

Sample:
```text
+--------+----------+------------+-------+---------+
|Order ID|Order Date|CustomerName|  State|     City|
+--------+----------+------------+-------+---------+
| B-25601|01-04-2018|      Bharat|Gujarat|Ahmedabad|
+--------+----------+------------+-------+---------+
```

## sales_order_detail
Data discovery result: aggregated away `product id` (if there are any). Composite Key is `Order Id`,`Category`,`sub-category`
```text
Order ID:string
Amount:double
Profit:double
Quantity:integer
Category:string
Sub-Category:string
```
Sample (Order Id ='B-25601')
```text
+--------+------+-------+--------+-----------+----------------+
|Order ID|Amount| Profit|Quantity|   Category|    Sub-Category|
+--------+------+-------+--------+-----------+----------------+
| B-25601|1275.0|-1148.0|       7|  Furniture|       Bookcases|
| B-25601|  66.0|  -12.0|       5|   Clothing|           Stole|
| B-25601|   8.0|   -2.0|       3|   Clothing|     Hankerchief|
| B-25601|  80.0|  -56.0|       4|Electronics|Electronic Games|
+--------+------+-------+--------+-----------+----------------+
```

## sales_target
```text
Month of Order Date:string
Category:string
Target:double
```
Sample:
```text
+-------------------+---------+-------+
|Month of Order Date| Category| Target|
+-------------------+---------+-------+
|             Apr-18|Furniture|10400.0|
|             May-18|Furniture|10500.0|
|             Jun-18|Furniture|10600.0|
|             Jul-18|Furniture|10800.0|
```