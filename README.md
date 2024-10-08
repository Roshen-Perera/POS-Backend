# POS Backend API

This backend API is implemented using he Jakarata EE for the existing front-end of the POS system. The API includes various features, including Servlet, JSON, and JNDI, to provide basic CRUD operations, using layered design pattern. The database management system used in this API is  MySQL via JND.

## Components

### Basic CRUD Operations

The API supports Create, Read, Update, and Delete operations for managing POS system data.

### Use of Design Patterns

The design patterns Singleton, Factory are implemented to enhance the maintainability and lower the amount of boilerplate of the code.

### Database Integration with JNDI

The API seamlessly integrates with a SQL database using Java Naming and Directory Interface (JNDI) for efficient data storage and retrieval.

### Logging Mechanism

The logging mechanism is used place to log and store relevant operations of the API. This ensures effective monitoring and troubleshooting.

## Requests Collection

### Base URL

The base URL for the API is:

http://localhost:8081/POS_BackEnd

### POST Register User
http://localhost:8081/POS_BackEnd/user
```json
{
    "name": "roshen",
    "email": "roshen@gmail.com",
    "password": "123"
}
```

### POST Login User

http://localhost:8081/POS_BackEnd/login?name=roshen&password=123

### POST Save Customer

http://localhost:8081/POS_BackEnd/customer

```json
{
    "id": "S001",
    "name": "Tony Stark",
    "address": "NYC",
    "phone": "0760199035"
}
```

### DELETE Delete Customer

http://localhost:8081/POS_BackEnd/customer?id=S001

### PUT Update Customer

http://localhost:8081/POS_BackEnd/customer
```json
{
    "id": "S001",
    "name": "Peter Parker",
    "address": "NYC",
    "phone": "0760199035"
}
```

### GET Get Customer
http://localhost:8081/POS_BackEnd/customer

### GET Get Customer by ID
http://localhost:8081/POS_BackEnd/customer?id=S001

### POST Save Product
http://localhost:8081/POS_BackEnd/product
```json
{
        "id": "P001",
        "name": "Munchee",
        "type": "Biscuit",
        "qty": 500,
        "price": 450
}
```

### DELETE Delete Product
http://localhost:8081/POS_BackEnd/product?id=O001

### PUT Update Product
http://localhost:8081/POS_BackEnd/product
```json
{
        "id": "P001",
        "name": "Munchee",
        "type": "Biscuit",
        "qty": 1000,
        "price": 440
}
```

### GET Get Product
http://localhost:8081/POS_BackEnd/product

### GET Get Product by ID
http://localhost:8081/POS_BackEnd/product?id=P001

### POST Save Order
http://localhost:8081/POS_BackEnd/orders
```json
{
    "orderId": "O005",
    "customerId": "S001",
    "customerName":"Tony Stark",
    "productId": "P001",
    "productName": "Munchee",
    "productType": "Biscuit",
    "productQTYNeeded": 20,
    "productPrice": 400,
    "productTotal": 2000
}
```

### DELETE Remove Order
http://localhost:8081/POS_BackEnd/orders?id=O001