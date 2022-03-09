# Survey about the audience
- How many of you have worked with sql, table, joins

# Insights can be derived

### a) joins and aggregation
- join `sales_order_header` with `sales_order_details`, then aggregate, partition by and sum/RANK/dense-rank
- get insights: which city makes more profit, the least profit days, which category sells more quantity

### b) joins and group by
- join `sales_order_header` with `sales_order_details`
so we can get the customer state/city, with product category/sub-category they purchased
- get insights: such as customer segmentation

### c) join and possible forecast/trend
- join `sales_order_header`, `sales_target` and `sales_order_details`
so we can get target(assume Profit/loss) and actual sales; 
- get insights: check whether the target was met or not, potential forecast what could happen in near future at CATEGORY level

# Other insight could be derived if we had dataset:
- inventory
  `demand planning`, and `forecasting`
- consumer details
  `target communication` using their contact information
  
# Performance consideration
consider materializing the joins and save to disk