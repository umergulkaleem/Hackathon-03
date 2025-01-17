 Furniture Store E-Commerce Website  

This project is a simple e-commerce website for buying furniture online. It lets users browse products, place orders, and write reviews.  


## System Overview  

### Frontend  
- **Technology**: Next.js  
- **What it does**:  
  - Shows a list of furniture items.  
  - Lets users add reviews and view them.  
  - Handles cart and checkout.  

### Backend  
- **Technology**: Sanity CMS  
- **What it does**:  
  - Stores product details, orders, and reviews.  
  - Manages user data and comments.  

### Third-Party APIs  
- **Payment**: Processes payments securely.  
- **Delivery Tracking**: Tracks shipments.  


## APIs  

### Products  
- **GET** `/products` – Fetch all products.  
  ```json
  {
    "id": 1,
    "name": "Sofa",
    "price": 15000,
    "image": "Sofa.svg"
  }
  

### Comments  
- **GET** `/comments` – Get comments for a product.  
  ```json
  {
    "userId": 101,
    "productId": 1,
    "message": "Durable Product",
    "time": "10:02 pm, 16/1/2025"
  }


### Orders  
- **POST** `/orders` – Create a new order.  
  ```json
  {
    "orderId": 5101,
    "productId": 1,
    "quantity": 2
  }
  ```


## Workflow  

1. **User Login**:  
   - Verify new or returning users using **Sanity CMS**.  

2. **Products**:  
   - Display products from **Sanity CMS**.  

3. **Place Order**:  
   - Users add items to the cart and checkout.  

4. **Payment**:  
   - Process payment through a third-party API.  

5. **Track Shipment**:  
   - Use a third-party API to track delivery.  

6. **Write Review**:  
   - Users leave reviews; data is stored in **Sanity CMS**.  


## Data Structure  

### Products  
| Field | Type   | Description         |  
|-------|--------|---------------------|  
| id    | String | Unique product ID   |  
| name  | String | Product name        |  
| price | Number | Product price       |  


