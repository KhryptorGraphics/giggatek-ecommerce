# GigGatek - Advanced Ecommerce Platform for Refurbished Hardware

GigGatek is a sophisticated ecommerce platform specialized in selling and renting refurbished computer hardware. Built with modern technologies and best practices, it offers both direct sales and a unique rent-to-own service, making cutting-edge technology accessible to more customers.

![GigGatek Logo](https://via.placeholder.com/800x400?text=GigGatek+Platform)

## 🚀 Key Features

- **Dual Business Model**: Traditional sales and innovative rent-to-own options
- **Advanced Product Categorization**: Intelligent hierarchical system for hardware components
- **Comprehensive Admin Panel**: Feature-rich backend for managing inventory, orders, rentals, and customers  
- **Detailed Product Tracking**: Condition grading, benchmarking, and compatibility tracking
- **Rental Contract Management**: Automated payment scheduling, buyout options, and contract enforcement
- **Customer Dashboard**: Order history, rental agreement management, and personalized recommendations
- **Responsive Design**: Optimized for all devices with modern UI/UX principles
- **Secure Authentication**: Role-based access control with OAuth integrations
- **Advanced Search**: Filter by component specifications, condition ratings, and rental options

## 💻 Technology Stack

### Frontend
- React.js with Hooks and Context API
- Bootstrap for responsive layouts
- Redux for state management
- Axios for API communication
- PWA capabilities

### Backend
- Node.js with Express
- MySQL database with Sequelize ORM
- JWT-based authentication
- RESTful API design
- Winston for logging
- Jest for testing

### DevOps & Infrastructure
- Ubuntu 22.04 server
- Apache2 web server
- PM2 for process management
- Nginx as reverse proxy (optional)
- SSL via Let's Encrypt

## 📋 Prerequisites

- Node.js 16.x or higher
- MySQL 8.0+
- npm 8.x or higher
- Git

## 🔧 Installation & Setup

### Clone the Repository

```bash
git clone https://github.com/khryptorgraphics/giggatek-ecommerce.git
cd giggatek-ecommerce
```

### Backend Setup

```bash
cd server
npm install
cp .env.example .env  # Edit with your credentials
npm run db:setup      # Initialize database
npm run dev           # Start development server
```

### Frontend Setup

```bash
cd client
npm install
cp .env.example .env  # Edit with your settings
npm start             # Launch development server
```

### Production Build

```bash
# Backend
cd server
npm run build

# Frontend
cd client
npm run build
```

## 🏗️ Project Structure

```
giggatek/
├── client/                # Frontend React application  
│   ├── public/            # Static files
│   ├── src/               # Source code
│   │   ├── components/    # UI components
│   │   ├── contexts/      # React contexts
│   │   ├── layouts/       # Page layouts
│   │   ├── pages/         # Page components
│   │   ├── services/      # API services
│   │   ├── styles/        # CSS and style files
│   │   └── utils/         # Utility functions
├── server/                # Backend Node.js application
│   ├── config/            # Server configuration
│   ├── controllers/       # Route controllers
│   ├── middleware/        # Express middleware
│   ├── models/            # Sequelize models
│   ├── routes/            # API routes
│   ├── services/          # Business logic
│   ├── utils/             # Utility functions
│   └── tests/             # Test files
├── docs/                  # Documentation
└── scripts/               # Utility scripts
```

## 📊 Database Schema

The database includes these primary entities:

- **Users**: Customer accounts, authentication, and profiles
- **Products**: Computer hardware with detailed specifications
- **Categories**: Hierarchical product categorization
- **Orders**: Purchase transactions and histories
- **RentalAgreements**: Contracts for rent-to-own arrangements
- **Reviews**: Product ratings and customer feedback

## 🔍 API Documentation

API documentation is available at:

- Development: `http://localhost:5000/api-docs`
- Production: `https://api.giggatek.com/api-docs`

## 🧪 Running Tests

```bash
# Backend tests
cd server
npm test

# Frontend tests
cd client
npm test
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the project's coding standards and includes appropriate tests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

For inquiries, please contact: admin@giggatek.com

---

Built with ❤️ by [KhryptoGraphics](https://github.com/khryptorgraphics)