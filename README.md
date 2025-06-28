# Project Name 
### GREENEATS is an online food ordering system
# step 1.

1.1 create a dynamodb table (we are creating to tables one for menus the other for orders)

#### Name: MenuItems

Partition key: 

Name → restaurant_id

Type → String

####  to input iteams click explory ( note you can genereate a jeson code and deploy i just tried inserting the code manually)

|FIELD                            |VALUE                            |
|---------------------------------|---------------------------------|
|restaurant_id                    |r001                             |
|item_id                          |i001                             |
|category_name                    |Burgers                          |
|name                             |Veggie Burger                    |
|description                      |Plant-based burger               |
|price                            |	5.99                            |
|image_url                        |	https://example.com/veggie.jpg  |

### CLICK CREATE ITEAM

Confirm Json output like this 

{
  "restaurant_id": "r001",
  "item_id": "i001",
  "category_name": "Burgers",
  "name": "Veggie Burger",
  "description": "Plant-based burger",
  "price": 5.99,
  "image_url": "https://example.com/veggie.jpg"
}

### 1.2 

### Create Order Table

Table name: Orders

Partition key:

Name → order_id

Type → String

### Click create table 

### To input items click explore: create iteams

Json and pes this code 

{
  "order_id": { "S": "ord001" },
  "restaurant_id": { "S": "r001" },
  "table_number": { "S": "12" },
  "status": { "S": "Order Received" },
  "timestamp": { "S": "2025-06-28T10:30:00Z" },
  "items": {
    "L": [
      {
        "M": {
          "item_id": { "S": "i001" },
          "name": { "S": "Veggie Burger" },
          "quantity": { "N": "2" },
          "price": { "N": "5.99" }
        }
      }
    ]
  }
}














