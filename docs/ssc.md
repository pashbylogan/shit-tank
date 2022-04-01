# SSC
- Revenue: $43.5M [source](https://www.datanyze.com/companies/sanitary-service/33817681)
- Employees: 220
- 45,000-50,000 Customers [source](http://www.ssc-inc.com/uploads/SSC_25thAnniversary_CurbsideRecycling_Snapshot_Electronic_061814_1.pdf)
- "SSC operates four trash trucks, five recycling trucks and one compost truck." [source](http://whatcomwatch.org/index.php/article/whatcoms-recyclers-face-uncertainty/)
- "Drivers need to get in and out of their vehicles between 600 and 1,000 times a day" [source](https://www.bellinghamherald.com/news/local/article257791303.html#storylink=cpy)

## Derived Business Stats
```python

customers = 45_000
employees = 220
revenue = 43_000_000
revenue_per_customer = revenue/customers # ~ $950
revenue_per_customer_per_month = revenue_per_customer/12
print(revenue_per_customer_per_month) # ~$80

customers_per_route_low = 600
customers_per_route_high = 1000

# less efficient drivers
routes = customers / customers_per_route_low
print(routes) # 75
routes_per_day = routes / 5
print(routes_per_day) # 15 (drivers?)
# 9000 customers a day?

# very efficient drivers
routes = customers / customers_per_route_high
print(routes) # 45
routes_per_day = routes / 5
print(routes_per_day) # 9 (drivers?)

# operating costs?
salary_average = 40000
payroll = employees * salary_average
print(payroll) # ~ $8_800_000

```

## Idea: Notifications For Route Pickup

```python

customers = 45_000
salary_per_hour = 20
annual_salary = salary_per_hour * 2_000
price_per_message = 0.0075 # twilio (vonage = 0.0064)
annual_cost_ceiling = 52 * customers * price_per_message
print(annual_cost_ceiling) # $17_500 / year

hours_needed_to_save = annual_cost_ceiling / salary_per_hour
print(hours_needed_to_save) # ~1_000 hours needed to save



```

# Web Service

## Calendar

```python
customers = 45_000
geocoding_request_per_month = 3_000
geocoding_cost_per_month = 15

// cache the entire ssc db
// geocoding_request_per_month = 45_000
// geocoding_cost_per_month = 225

```

