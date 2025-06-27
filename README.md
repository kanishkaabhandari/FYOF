# 🍽️ **FYOF - Find Your Own Food**
## 🚀 **Advanced OS Algorithm Implementation with Interactive Visualizations**

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://fyof-os-project.netlify.app)
[![Backend API](https://img.shields.io/badge/Backend-API-blue)](https://fyof-backend-production.railway.app)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black)](https://github.com/aayush992/Food_management)

A comprehensive food ordering platform that demonstrates practical implementation of **Operating System algorithms** in a real-world web application. This project showcases advanced algorithm visualization, performance analysis, and modern web development practices with **interactive maps, charts, and real-time data visualization**.

## 🎯 **Project Objectives**

- **Primary Goal:** Implement and visualize OS algorithms in a practical food delivery application
- **Educational Goal:** Demonstrate understanding of Operating System concepts through interactive visualizations
- **Technical Goal:** Build a production-ready full-stack web application with modern technologies
- **Innovation Goal:** Create interactive algorithm demonstrations with real-time performance analysis

## 🧮 **OS Algorithms Implemented**

### **1. 🗺️ Dijkstra's Shortest Path Algorithm**
- **Purpose:** Calculate optimal delivery routes in real-time
- **Implementation:** Interactive map visualization with route calculation
- **Complexity:** O((V + E) log V) where V = vertices, E = edges
- **Features:** Traffic-aware routing, animated path visualization, performance metrics
- **Visualization:** Interactive map with 10 Dehradun locations, animated route drawing

### **2. ⏰ CPU Scheduling Algorithms (5 Implementations)**
- **FCFS (First Come First Serve):** Simple queue-based order processing
- **SJF (Shortest Job First):** Optimize for shortest cooking times
- **Priority Scheduling:** VIP customer and order priority handling
- **Round Robin:** Fair time-sharing for order processing with quantum
- **SRTF (Shortest Remaining Time First):** Dynamic optimization for order completion
- **Visualization:** Gantt charts, performance comparison, efficiency analysis

### **3. 📊 Performance Analysis & Metrics**
- **Real-time Algorithm Comparison:** Live performance metrics and efficiency analysis
- **24-Hour Trend Analysis:** Food availability patterns and peak time detection
- **System Resource Monitoring:** CPU, memory, and network utilization tracking
- **Interactive Heatmaps:** 24-hour availability visualization with color-coded data

## 🎨 **Interactive Visualizations**

### **📈 Charts & Graphs:**
- **Bar Charts:** Algorithm performance comparison
- **Pie Charts:** Efficiency distribution analysis
- **Line Charts:** 24-hour performance trends
- **Radar Charts:** Multi-dimensional route analysis
- **Gantt Charts:** Order processing timeline
- **Heatmaps:** Availability patterns with interactive cells

### **🗺️ Interactive Maps:**
- **Real-time Route Calculation:** Dijkstra's algorithm visualization
- **Animated Path Drawing:** Step-by-step route animation
- **Performance Metrics:** Distance, time, efficiency tracking
- **Traffic-Aware Routing:** Alternative route calculation

### For Restaurant Owners
- **Restaurant Management**
  - Complete dashboard for operations
  - Menu management system
  - Order processing and tracking
  - Analytics and reporting
  - Staff management
  - Inventory tracking

- **Business Tools**
  - Performance analytics
  - Customer feedback management
  - Revenue tracking
  - Restaurant profile management
  - Marketing tools integration

## 💻 **Technical Stack**

### **🖥️ Backend:**
- **Node.js** with Express.js framework
- **MongoDB** with Mongoose ODM
- **JWT** authentication and authorization
- **RESTful APIs** for all operations
- **Socket.io** for real-time features
- **Algorithm APIs** for OS implementations

### **🌐 Frontend:**
- **HTML5, CSS3, JavaScript** (Vanilla JS)
- **Chart.js** for interactive visualizations
- **Responsive Design** for all devices
- **Interactive Maps** for route visualization
- **Real-time Updates** via WebSocket
- **Modern UI/UX** with animations

### **🗄️ Database:**
- **MongoDB Atlas** (Cloud database)
- **Collections:** Users, Outlets, Orders, Payments, Carts
- **Relationships:** Properly normalized schema
- **Indexing:** Optimized for performance

### **🚀 Deployment:**
- **Backend:** Railway.app (Production hosting)
- **Frontend:** Netlify.com (Static hosting)
- **Database:** MongoDB Atlas (Cloud)
- **CI/CD:** Automatic deployments

## Project Structure

```
fyof- frontend/
├── Core Pages
│   ├── index.html          # Landing page
│   ├── about.html          # About platform
│   ├── contact.html        # Contact information
│   └── service.html        # Services overview
│
├── User Interface
│   ├── login.html          # Authentication
│   ├── register-outlet.html # Restaurant registration
│   ├── user-dashboard.html # User control panel
│   └── profile.html        # User profile management
│
├── Restaurant Features
│   ├── menu.html          # Menu display
│   ├── booking.html       # Reservation system
│   ├── orders.html        # Order management
│   └── analytics.html     # Business analytics
│
├── Customer Features
│   ├── cart.html          # Shopping cart
│   ├── delivery.html      # Delivery tracking
│   └── reviews.html       # Rating system
│
├── Styling
│   ├── styles.css         # Global styles
│   ├── dashboard.css      # Dashboard styles
│   ├── login.css         # Authentication styles
│   └── index.css         # Landing page styles
│
├── JavaScript
│   ├── login.js          # Authentication logic
│   └── dashboard.js      # Dashboard functionality
│
└── images/               # Image assets
```

## Technologies Used

- **Frontend**
  - HTML5 for structure
  - CSS3 for styling
    - Responsive design
    - Mobile-first approach
    - Custom animations
  - JavaScript (ES6+)
    - DOM manipulation
    - AJAX for API calls
    - Local Storage for data persistence
  - Bootstrap for UI components

## 🌐 **Live Demo**

### **🚀 Access the Live Application:**
- **Frontend:** [https://fyof-os-project.netlify.app](https://fyof-os-project.netlify.app)
- **Backend API:** [https://fyof-backend-production.railway.app](https://fyof-backend-production.railway.app)

### **📊 Algorithm Demonstrations:**
- **Charts Dashboard:** [/charts-visualization.html](https://fyof-os-project.netlify.app/charts-visualization.html)
- **Dijkstra Map:** [/dijkstra-map.html](https://fyof-os-project.netlify.app/dijkstra-map.html)
- **Algorithm Testing:** [/algorithms-working.html](https://fyof-os-project.netlify.app/algorithms-working.html)
- **Database Viewer:** [/database-viewer.html](https://fyof-os-project.netlify.app/database-viewer.html)

## 🚀 **Getting Started**

### **🌐 Option 1: Use Live Demo (Recommended)**
Simply visit the live demo links above to explore all features immediately.

### **💻 Option 2: Local Development**

1. **Clone the repository:**
   ```bash
   git clone https://github.com/aayush992/Food_management.git
   cd Food_management
   ```

2. **Backend Setup:**
   ```bash
   cd fyof-backend
   npm install
   cp .env.example .env
   # Update .env with your MongoDB connection string
   npm start
   ```

3. **Frontend Setup:**
   ```bash
   cd fyof_frontend
   # Update js/config.js with your backend URL
   # Open index.html in browser or use live server
   ```

### **🗄️ Database Setup:**
- **Local:** MongoDB installed locally
- **Cloud:** MongoDB Atlas (recommended for production)
- **Seed Data:** Run `node seedEverything.js` in backend directory

## Key Features in Detail

### User Management
- Secure authentication system
- User role management (Customer/Restaurant Owner)
- Profile customization
- Settings management

### Order System
- Intuitive cart management
- Real-time order tracking
- Multiple payment integration readiness
- Order history and reordering capability

### Restaurant Management
- Complete dashboard for restaurant owners
- Menu management system
- Order processing workflow
- Table booking system
- Analytics and reporting tools

### Communication
- Integrated messaging system
- Review and rating platform
- Customer feedback management
- Support ticket system

## Contributing

1. Fork the repositorym
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## Contact

Aayush Saini - [GitHub](https://github.com/aayush992)

## 📈 **Performance & Features**

### **🎯 Algorithm Performance:**
- **Dijkstra's Algorithm:** < 5ms execution time
- **Scheduling Algorithms:** Real-time comparison of 5 algorithms
- **Database Queries:** < 100ms response time
- **Chart Rendering:** < 2 seconds for complex visualizations
- **Map Interactions:** Smooth 60fps animations

### **🌟 Unique Features:**
- **Interactive Algorithm Visualization:** See OS concepts in action
- **Real-time Performance Metrics:** Live algorithm comparison
- **Educational Value:** Perfect for learning OS concepts
- **Production Ready:** Deployed on professional platforms
- **Mobile Responsive:** Works on all devices
- **Cross-browser Compatible:** Tested on major browsers

## 🚀 **Deployment Information**

### **🌐 Hosting Platforms:**
- **Frontend:** Netlify.com (Static hosting with CDN)
- **Backend:** Railway.app (Node.js hosting)
- **Database:** MongoDB Atlas (Cloud database)
- **Domain:** Custom domain with HTTPS

### **🔧 CI/CD Pipeline:**
- **Automatic Deployments:** GitHub integration
- **Environment Management:** Separate dev/prod configs
- **Performance Monitoring:** Real-time metrics
- **Error Tracking:** Comprehensive logging

## 🎓 **Educational Value**

### **📚 OS Concepts Demonstrated:**
- **Graph Algorithms:** Dijkstra's shortest path implementation
- **CPU Scheduling:** 5 different scheduling strategies
- **Performance Analysis:** Algorithm efficiency comparison
- **System Optimization:** Real-world application of OS concepts
- **Data Structures:** Practical use of graphs, queues, heaps

### **🏆 Learning Outcomes:**
- Understanding of algorithm complexity and optimization
- Practical application of theoretical OS concepts
- Experience with modern web development technologies
- Knowledge of deployment and production practices
- Skills in data visualization and user experience design

## 🔮 **Future Enhancements**

- **Mobile Application:** React Native implementation
- **Advanced Analytics:** Machine learning integration
- **Real-time Collaboration:** Multi-user algorithm visualization
- **API Documentation:** Comprehensive Swagger documentation
- **Performance Optimization:** Further algorithm improvements
- **Internationalization:** Multi-language support

## Mermaid Flowchart

```mermaid
flowchart TD
  %% User Entry
  User["User"]

  %% Frontend Pages
  subgraph Frontend
    A1["index.html (Landing)"]
    A2["about.html"]
    A3["contact.html"]
    A4["service.html"]
    A5["login.html"]
    A6["register-outlet.html"]
    A7["user-dashboard.html"]
    A8["profile.html"]
    A9["menu.html"]
    A10["booking.html"]
    A11["orders.html"]
    A12["analytics.html"]
    A13["cart.html"]
    A14["delivery.html"]
    A15["reviews.html"]
    A16["messages.html"]
    A17["settings.html"]
    A18["new-index.html"]
    style A1 fill:#f9f,stroke:#333,stroke-width:1px
  end

  %% CSS/JS
  subgraph Assets
    B1["styles.css"]
    B2["dashboard.css"]
    B3["login.css"]
    B4["index.css"]
    B5["login.js"]
    B6["dashboard.js"]
    B7["js/auth.js"]
  end

  %% Backend
  subgraph Backend
    C1["server.js"]
    C2["routes/auth.js"]
    C3["routes/cart.js"]
    C4["routes/orderProcessing.js"]
    C5["routes/outlet.js"]
    C6["controllers/*"]
    C7["models/User.js"]
    C8["models/Cart.js"]
    C9["models/Order.js"]
    C10["models/Outlet.js"]
    C11["middleware/auth.js"]
    C12["algorithms/*"]
    C13["services/OrderProcessingService.js"]
  end

  %% User Navigation
  User --> A1
  User --> A2
  User --> A3
  User --> A4
  User --> A5
  User --> A6
  User --> A7
  User --> A8
  User --> A9
  User --> A10
  User --> A11
  User --> A12
  User --> A13
  User --> A14
  User --> A15
  User --> A16
  User --> A17
  User --> A18

  %% Pages use CSS/JS
  A1 --> B1
  A1 --> B4
  A5 --> B3
  A5 --> B5
  A7 --> B2
  A7 --> B6
  A5 --> B7
  %% (Add more as needed for other pages)

  %% Pages to Backend
  A5 -->|Login API| C2
  A6 -->|Register Outlet API| C5
  A7 -->|Dashboard Data| C4
  A8 -->|Profile Data| C2
  A9 -->|Menu Data| C5
  A10 -->|Booking API| C5
  A11 -->|Order API| C4
  A12 -->|Analytics API| C4
  A13 -->|Cart API| C3
  A14 -->|Delivery API| C4
  A15 -->|Review API| C4
  A16 -->|Messages API| C2
  A17 -->|Settings API| C2

  %% Backend Flow
  C1 --> C2
  C1 --> C3
  C1 --> C4
  C1 --> C5

  C2 --> C6
  C3 --> C6
  C4 --> C6
  C5 --> C6

  C6 --> C7
  C6 --> C8
  C6 --> C9
  C6 --> C10

  C2 --> C11
  C4 --> C12
  C4 --> C13

  %% Data flow to/from database/models
  C7 -.->|User Data| C1
  C8 -.->|Cart Data| C1
  C9 -.->|Order Data| C1
  C10 -.->|Outlet Data| C1