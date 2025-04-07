# GigGatek Development Guide

This document provides detailed information for developers working on the GigGatek platform.

## Development Environment Setup

### Prerequisites

- Node.js (v16.x or higher)
- MySQL (v8.0 or higher)
- Git
- npm or yarn

### Initial Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/khryptorgraphics/giggatek-ecommerce.git
   cd giggatek-ecommerce
   ```

2. Install dependencies for both client and server:
   ```bash
   # Install server dependencies
   cd server
   npm install

   # Install client dependencies
   cd ../client
   npm install
   ```

3. Set up environment variables:
   ```bash
   # Server environment
   cd ../server
   cp .env.example .env
   # Edit .env with your local configuration

   # Client environment
   cd ../client
   cp .env.example .env
   # Edit .env with your local configuration
   ```

4. Initialize the database:
   ```bash
   cd ../server
   npm run db:setup
   ```

### Running the Application

#### Development Mode

Start the backend server:
```bash
cd server
npm run dev
```

Start the frontend development server:
```bash
cd client
npm start
```

The backend API will be available at `http://localhost:5000` and the frontend at `http://localhost:3000`.

## Code Standards

### Frontend

- Use functional components with hooks
- Follow the React file structure outlined in the project
- Use CSS modules for component-specific styles
- Follow the Airbnb JavaScript Style Guide
- Write meaningful component and function names
- Add JSDoc comments for all functions and components

### Backend

- Use ES6+ features
- Follow the MVC pattern
- Implement proper error handling
- Use async/await for asynchronous operations
- Add input validation for all API endpoints
- Document all API endpoints
- Write unit tests for all controllers and services

## Database Management

### Migrations

Create a new migration:
```bash
npm run migrate:create -- --name=migration-name
```

Run migrations:
```bash
npm run migrate:up
```

Rollback migrations:
```bash
npm run migrate:down
```

### Seeding

Seed the database with initial data:
```bash
npm run db:seed
```

## Testing

### Running Tests

Backend tests:
```bash
cd server
npm test
```

Frontend tests:
```bash
cd client
npm test
```

### Writing Tests

- Use Jest for both frontend and backend tests
- Follow the AAA pattern (Arrange, Act, Assert)
- Mock external dependencies
- Test both success and failure cases
- Aim for high test coverage

## Branching Strategy

We follow the Gitflow workflow:

- `main`: Production-ready code
- `develop`: Main development branch
- `feature/*`: New features
- `bugfix/*`: Bug fixes
- `release/*`: Release preparation
- `hotfix/*`: Urgent fixes for production

## Pull Request Process

1. Create a branch from `develop` for your work
2. Make your changes, following the code standards
3. Write or update tests
4. Ensure all tests pass
5. Update documentation if necessary
6. Submit a pull request to `develop`
7. Request a code review
8. Address any feedback

## Deployment

### Staging Deployment

The staging environment is automatically updated when changes are merged into the `develop` branch.

### Production Deployment

1. Create a release branch from `develop`
2. Perform final testing
3. Version bump and update changelog
4. Merge into `main`
5. Tag the release
6. Deploy to production

## Documentation

### API Documentation

The API documentation is generated using Swagger. To access it:

1. Start the server
2. Visit `http://localhost:5000/api-docs`

To update the API documentation, modify the JSDoc comments in the controller files.

### Component Documentation

Frontend components are documented using Storybook. To access it:

1. Run `npm run storybook` in the client directory
2. Visit `http://localhost:6006`

## Troubleshooting

### Common Issues

#### Database Connection Errors
- Check your MySQL service is running
- Verify your .env database credentials
- Ensure your database exists

#### Node.js Version Issues
- Use nvm to manage Node.js versions
- Run `nvm use` in the project root to use the recommended version

#### Port Conflicts
- Check if ports 3000 or 5000 are already in use
- Modify the port in .env files if needed

## Additional Resources

- [Sequelize Documentation](https://sequelize.org/master/)
- [React Documentation](https://reactjs.org/docs/getting-started.html)
- [Express Documentation](https://expressjs.com/)
- [MySQL Documentation](https://dev.mysql.com/doc/)