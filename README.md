# *Real-Life Example: How REST APIs Power Everyday Applications*

#Real-Life Example

Imagine you're ordering pizza through an online delivery app. The app's backend uses a REST API to interact with its database. Here’s how it might work:

1. *Scenario: You want to view the menu.*

   * API Call:
     The app sends a GET request to the backend:

     >GET https://pizzaapp.com/menu
     

   * Response:
     The backend sends back the menu in JSON format:

     ```json
     {
          "menu": [
          {
              "id": 1,
              "name": "Margherita",
              "price": 5
          },
          {
              "id": 2,
              "name": "Pepperoni",
              "price": 6
          }
        ]
     }

---------------------------------------------------------------------------------------------------------------------------------------------

2. *Scenario: You want to order a Pepperoni pizza.*

   * API Call:
     The app sends a POST request to the backend:

     >POST https://pizzaapp.com/orders

      ```json
      Body:
      {
      "item_id": 2,
      "quantity": 1
      }
     

   * Response:
    The backend confirms the order with a status code 201 Created and a response:

     ```json
       {
        "order_id": 123,
        "status": "confirmed"
       }

---------------------------------------------------------------------------------------------------------------------------------------------

3. *Scenario: You want to check your order status.*
   
  * API Call:
     The app sends a GET request:

     >GET https://pizzaapp.com/orders/123

   * Response:
    
     ```json
       {
        "order_id": 123,
        "status": "preparing"
       }


---------------------------------------------------------------------------------------------------------------------------------------------

4. *Scenario: You decide to cancel the order.*

   * API Call:
     The app sends a DELETE request:

     >DELETE https://pizzaapp.com/orders/123

   * Response:
    
     ```json
       {
         "message": "Order canceled successfully."
       }
---------------------------------------------------------------------------------------------------------------------------------------------
