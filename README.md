# MyIndianBaazaar 🛒

A modern, full-stack e-commerce platform built with React, TypeScript, and Express.js. MyIndianBaazaar provides a complete online shopping experience with features like product management, user authentication, cart functionality, order processing, and review systems.

## 🚀 Features

### Customer Features
- **Product Browsing**: Browse products by categories with advanced filtering
- **Product Details**: Detailed product pages with image zoom, specifications, and reviews
- **Shopping Cart**: Add/remove items, quantity management, and persistent cart
- **User Authentication**: Secure login/registration with JWT tokens
- **Order Management**: Place orders, track order status, and view order history
- **Review System**: Rate and review products with verified purchase badges
- **Responsive Design**: Mobile-first design that works on all devices

### Admin Features
- **Admin Dashboard**: Comprehensive dashboard with sales analytics
- **Product Management**: Create, update, and delete products
- **Order Management**: View and update order statuses
- **Customer Management**: View customer information and order history
- **Inventory Management**: Track stock levels and manage product availability

### Technical Features
- **Real-time Notifications**: Toast notifications for user actions
- **Image Optimization**: Responsive images with zoom functionality
- **SEO Friendly**: Proper meta tags and structured data
- **API Integration**: RESTful API with proper error handling
- **Database Integration**: PostgreSQL with Sequelize ORM

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks and functional components
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and development server
- **React Router 6** - Client-side routing
- **TailwindCSS 3** - Utility-first CSS framework
- **Radix UI** - Headless UI components
- **React Hook Form** - Form management with validation
- **Zod** - Schema validation
- **Lucide React** - Beautiful icons

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **TypeScript** - Type-safe server development
- **PostgreSQL** - Relational database
- **Sequelize** - ORM for database operations
- **JWT** - JSON Web Tokens for authentication
- **bcrypt** - Password hashing
- **CORS** - Cross-origin resource sharing

### Development Tools
- **Vite** - Build tool and dev server
- **Vitest** - Unit testing framework
- **ESLint** - Code linting
- **Prettier** - Code formatting
- **PostCSS** - CSS processing

## 📦 Installation

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/MyIndianBaazaar.git
   cd MyIndianBaazaar
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   ```bash
   cp .env.example .env
   ```
   
   Update the `.env` file with your configuration:
   ```env
   # Database Configuration
   DB_USER=postgres
   DB_HOST=localhost
   DB_NAME=myindianbaazaar
   DB_PASSWORD=your_password
   DB_PORT=5432
   
   # JWT Configuration
   JWT_SECRET=your_jwt_secret
   JWT_EXPIRY=7d
   
   # Server Configuration
   PORT=8080
   NODE_ENV=development
   ```

4. **Database Setup**
   ```bash
   # Create database
   createdb myindianbaazaar
   
   # Run migrations (if available)
   npm run migrate
   
   # Seed database (if available)
   npm run seed
   ```

5. **Start the application**
   ```bash
   # Development mode
   npm run dev
   
   # Production build
   npm run build
   npm start
   ```

## 🚀 Development

### Available Scripts

```bash
# Development
npm run dev          # Start development server
npm run build        # Build for production
npm start           # Start production server

# Database
npm run migrate     # Run database migrations
npm run seed        # Seed database with sample data

# Code Quality
npm run typecheck   # TypeScript type checking
npm run format.fix  # Format code with Prettier
npm test           # Run tests
```

### Project Structure

```
MyIndianBaazaar/
├── client/                 # React frontend
│   ├── pages/             # Route components
│   ├── components/        # Reusable React components
│   ├── lib/              # Utility functions and API client
│   ├── hooks/            # Custom React hooks
│   └── main.tsx          # Application entry point
├── server/                # Express backend
│   ├── controllers/      # Route handlers
│   ├── models/           # Database models
│   ├── utils/            # Server utilities
│   └── index.ts          # Server entry point
├── shared/                # Shared types and interfaces
└── public/               # Static assets
```

## 📱 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile
- `PUT /api/auth/profile` - Update user profile

### Product Endpoints
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `POST /api/products` - Create product (Admin only)
- `PUT /api/products/:id` - Update product (Admin only)
- `DELETE /api/products/:id` - Delete product (Admin only)

### Order Endpoints
- `POST /api/orders` - Create new order
- `GET /api/orders` - Get user orders
- `GET /api/orders/:id` - Get order by ID
- `PATCH /api/orders/:id/status` - Update order status (Admin only)

### Review Endpoints
- `POST /api/reviews` - Create product review
- `GET /api/products/:id/reviews` - Get product reviews

## 🔒 Authentication

The application uses JWT-based authentication with the following features:
- Secure password hashing with bcrypt
- Token-based authentication
- Protected routes for authenticated users
- Role-based access control (Admin/Customer)

## 🎨 UI Components

The application uses a custom UI component library built with Radix UI and TailwindCSS:
- **Layout Components**: Header, Footer, Sidebar
- **Form Components**: Input, Button, Select, Textarea
- **Display Components**: Card, Badge, Avatar, Toast
- **Navigation Components**: Breadcrumb, Pagination

## 🚀 Deployment

### Production Build
```bash
npm run build
npm start
```

### Docker Deployment
```bash
# Build Docker image
docker build -t myindianbaazaar .

# Run container
docker run -p 8080:8080 myindianbaazaar
```

### Environment Variables
Ensure all required environment variables are set in production:
- Database connection details
- JWT secret
- Payment gateway credentials (if applicable)

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👥 Team

- **Developer**: Anish Singh Rawat
- **Email**: anishsinghrawat5@gmail.com

## 🐛 Known Issues

- Review system requires purchase verification
- Image optimization can be improved
- Need to implement payment gateway integration

## 🔄 Future Enhancements

- [ ] Payment gateway integration (Razorpay/Stripe)
- [ ] Real-time chat support
- [ ] Advanced search and filtering
- [ ] Wishlist functionality
- [ ] Product recommendations
- [ ] Multi-language support
- [ ] Progressive Web App (PWA)
- [ ] Email notifications
- [ ] Social media integration

## 📞 Support

For support, email anishsinghrawat5@gmail.com or create an issue in the GitHub repository.

---

**Made with ❤️ in India**
