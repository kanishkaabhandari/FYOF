# 🚀 FYOF API Documentation

## Base URL: `http://localhost:5000/api`

---

## 🛒 **CART APIs**

### **Get User Cart**
```http
GET /cart/:userId
```
**Response:**
```json
{
  "userId": "string",
  "outletId": { "_id": "string", "name": "string" },
  "items": [
    {
      "itemId": "string",
      "itemName": "string", 
      "price": number,
      "quantity": number
    }
  ],
  "total": number
}
```

### **Add Item to Cart**
```http
POST /cart/add
Content-Type: application/json

{
  "userId": "string",
  "outletId": "string", 
  "item": {
    "itemId": "string",
    "itemName": "string",
    "price": number,
    "quantity": number
  }
}
```

### **Update Item Quantity**
```http
PUT /cart/update
Content-Type: application/json

{
  "userId": "string",
  "itemId": "string",
  "quantity": number
}
```

### **Remove Item from Cart**
```http
DELETE /cart/remove
Content-Type: application/json

{
  "userId": "string",
  "itemId": "string"
}
```

### **Clear Cart**
```http
DELETE /cart/clear/:userId
```

---

## 📦 **ORDER APIs**

### **Checkout (Create Order)**
```http
POST /orders/checkout
Content-Type: application/json

{
  "userId": "string",
  "paymentMethod": "card|upi|wallet|cash",
  "deliveryAddress": "string"
}
```

**Response:**
```json
{
  "success": true,
  "message": "Order placed successfully",
  "order": {
    "_id": "string",
    "customerId": "string",
    "outletId": "string", 
    "items": [...],
    "totalAmount": number,
    "status": "pending",
    "paymentStatus": "pending",
    "estimatedTime": number
  },
  "paymentRequired": boolean
}
```

### **Process Payment**
```http
POST /orders/payment/:orderId
Content-Type: application/json

{
  "paymentMethod": "card|upi|wallet",
  "paymentData": {
    // For card:
    "cardNumber": "string",
    "expiryDate": "MM/YY", 
    "cvv": "string"
    
    // For UPI:
    "upiId": "string"
    
    // For wallet:
    "walletType": "Paytm|PhonePe|GooglePay"
  }
}
```

**Response:**
```json
{
  "success": true,
  "message": "Payment successful",
  "transactionId": "string",
  "order": {...}
}
```

### **Get User Orders**
```http
GET /orders/user/:userId?status=pending&limit=10&page=1
```

### **Get Vendor Orders**
```http
GET /orders/vendor/:vendorId?status=pending&limit=10&page=1
```

### **Update Order Status**
```http
PUT /orders/status/:orderId
Content-Type: application/json

{
  "status": "pending|confirmed|processing|completed|cancelled",
  "vendorId": "string"
}
```

### **Get Single Order**
```http
GET /orders/:orderId
```

### **Get Payment Methods**
```http
GET /orders/payment-methods
```

**Response:**
```json
{
  "success": true,
  "paymentMethods": [
    {
      "id": "card",
      "name": "Credit/Debit Card",
      "description": "Pay using your credit or debit card",
      "icon": "credit-card",
      "enabled": true
    }
  ]
}
```

### **Create Razorpay Order**
```http
POST /orders/create-razorpay-order/:orderId
```

### **Process Refund**
```http
POST /orders/refund/:orderId
Content-Type: application/json

{
  "reason": "string",
  "amount": number (optional)
}
```

---

## 👤 **AUTH APIs**

### **Login**
```http
POST /auth/login
Content-Type: application/json

{
  "email": "string",
  "password": "string"
}
```

**Response:**
```json
{
  "token": "jwt_token",
  "user": {
    "_id": "string",
    "name": "string", 
    "email": "string",
    "role": "user|vendor"
  }
}
```

### **Register**
```http
POST /auth/register
Content-Type: application/json

{
  "name": "string",
  "email": "string", 
  "password": "string",
  "role": "user|vendor"
}
```

---

## 🏪 **OUTLET APIs**

### **Get All Outlets**
```http
GET /outlets
```

**Response:**
```json
[
  {
    "_id": "string",
    "name": "string",
    "description": "string",
    "cuisine": ["string"],
    "rating": number,
    "location": {
      "address": "string",
      "city": "string"
    },
    "menu": [
      {
        "itemName": "string",
        "description": "string", 
        "price": number,
        "category": "string",
        "isAvailable": boolean
      }
    ],
    "vendor": {
      "name": "string",
      "email": "string"
    }
  }
]
```

---

## 🧪 **TEST CREDENTIALS**

### **Customers:**
```
📧 sarah@example.com | 🔒 password123
📧 rahul@example.com | 🔒 password123  
📧 priya@example.com | 🔒 password123
📧 amit@example.com | 🔒 password123
📧 neha@example.com | 🔒 password123
```

### **Vendors:**
```
📧 rajesh@restaurant.com | 🔒 password123
📧 sunita@cafe.com | 🔒 password123
📧 mohammed@streetfood.com | 🔒 password123
📧 lakshmi@southindian.com | 🔒 password123
📧 vikram@punjabi.com | 🔒 password123
```

---

## 🔧 **ERROR RESPONSES**

### **Standard Error Format:**
```json
{
  "error": "Error message",
  "success": false
}
```

### **Common HTTP Status Codes:**
- `200` - Success
- `400` - Bad Request (validation error)
- `401` - Unauthorized
- `403` - Forbidden
- `404` - Not Found
- `500` - Internal Server Error

---

## 💡 **USAGE EXAMPLES**

### **Complete Order Flow:**
```javascript
// 1. Add items to cart
await fetch('/api/cart/add', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    userId: 'user_id',
    outletId: 'outlet_id',
    item: { itemId: 'item_id', itemName: 'Pizza', price: 200, quantity: 1 }
  })
});

// 2. Checkout
const order = await fetch('/api/orders/checkout', {
  method: 'POST', 
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    userId: 'user_id',
    paymentMethod: 'card',
    deliveryAddress: '123 Street'
  })
});

// 3. Process payment
const payment = await fetch(`/api/orders/payment/${orderId}`, {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    paymentMethod: 'card',
    paymentData: {
      cardNumber: '4111111111111111',
      expiryDate: '12/26', 
      cvv: '123'
    }
  })
});
```

---

## 🚀 **READY FOR PRODUCTION**

All APIs are fully functional and tested. The system supports:
- ✅ Complete cart management
- ✅ Multiple payment methods  
- ✅ Order tracking and management
- ✅ User authentication
- ✅ Vendor management
- ✅ Real-time updates
- ✅ Error handling
- ✅ Data validation
