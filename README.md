# nutrient-api
nutrient-api

Simple project to test different API technologies and database.


## Description of the data contained 
This is USDA foundation foods, meaning basic minimally processed foods. A foundation food might be things like Beans, there are many companies that sell beans but the foundation food for "Beans" will take a look
at what beans are typically made of across the board. here are the fields explained:

1. nutrients (calories, macros and sub categories are all concidered nutrients)
    - rank: How nutritionally relevant the nutrient is, low number = more relevant
    - amount: quantity in unit
    - unit: the unit to measure the quantity

2. input foods: these are the actual foods that you and I can buy used to make the measurements for the overal foundation food.

Note: some nutrients are listed as 0 quantity, this is because there exists regualtions that force them to be measured even if they might not be present in a sample. 

The rest should be self explanatory.

## Requirements

User Must:

1. Search for a food by Id
2. Search for a food by name
3. Search for a food by macro nutrient(s) value
4. Be able to add a quanity as an optional parameter
5. Get the important info first, ajusted for serving size:
    - calories
    - default serving size 
    - Fats
    - Carbs
    - Protein

User Should:

1. Get more detailed information about the food
    - full nutrient breakdown
2. Get results for multiple foods with total nutrients calculated

User Can:

1. Match the USDA food data with an actual product (open food facts?)

User Won't:

1. Upload data
2. Modify data
3. Delete data
    

## Goals

The main goal with this project is to test a variety of technologies to acheive the same results, this will lead to an interesting tech stack. 

## Tech stack

### V1 REST
- DB: MongoDB
- Server: Node + Express (JS)
- Gateway: Nginx
- Deployment: k3s

### V2 REST
- DB: SQL
- Server: Flask (Python)
- Gateway: Nginx
- Deployment: k3s

### V3 REST
- DB: PostgresSQL
- Server: Django + DRF (Python)
- Gateway: Nginx
- Deployment: k3s

### V3 GraphQL
- DB: PostgresSQL
- Server: ?
- Gateway: Nginx
- Deployment: k3s