# H1B Job Links Platform

A comprehensive platform for accessing curated H1B job opportunities with role-based filtering and subscription management.

## 🚀 Features

- **Paid Access Only**: Subscription-based access to curated job links
- **Role-Based Filtering**: 40+ job roles with dedicated link collections
- **User Authentication**: Secure login/registration system
- **Link Tracking**: Monitor user access and engagement
- **Excel Import**: Bulk import job links from Excel files
- **Modern UI**: Clean, responsive design with Tailwind CSS

## 🏗️ Architecture

### Backend (Node.js + TypeScript)
- Express.js REST API
- SQLite database with TypeScript models
- JWT authentication
- Role-based access control
- Excel import functionality

### Frontend (React + TypeScript)
- React 18 with TypeScript
- Tailwind CSS for styling
- React Router for navigation
- Axios for API communication
- Context API for state management

## 📦 Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Quick Start

1. **Clone and setup**:
   ```bash
   git clone <repository-url>
   cd h1b-job-links-platform
   ```

2. **Start Backend**:
   ```bash
   chmod +x start-backend.sh
   ./start-backend.sh
   ```
   Backend will run on http://localhost:3001

3. **Start Frontend** (in a new terminal):
   ```bash
   chmod +x start-frontend.sh
   ./start-frontend.sh
   ```
   Frontend will run on http://localhost:3000

## 🔐 Default Accounts

For testing, the system creates these sample accounts:

- **Premium User**: `demo@example.com` / `password123`
- **Basic User**: `test@example.com` / `password123`

## 📊 Sample Data

The system includes sample job links for:
- Data Analyst (Google, Microsoft)
- Business Analyst (Amazon, Facebook)
- Software Engineer (Netflix, Apple)
- Java Developer (Spotify, Uber)
- Python Developer (Stripe, Airbnb)

## 🛠️ API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile
- `POST /api/auth/upgrade-subscription` - Upgrade subscription

### Jobs
- `GET /api/jobs/roles` - Get all job roles with counts
- `GET /api/jobs/roles/:roleId/links` - Get links for specific role
- `GET /api/jobs/search` - Search links
- `POST /api/jobs/links/:linkId/access` - Log link access
- `GET /api/jobs/dashboard` - Dashboard statistics

### Admin
- `POST /api/admin/import-excel` - Import job links from Excel

## 📁 Project Structure

```
h1b-job-links-platform/
├── backend/
│   ├── src/
│   │   ├── controllers/     # API controllers
│   │   ├── middleware/      # Auth middleware
│   │   ├── models/          # Database models
│   │   ├── routes/          # API routes
│   │   ├── scripts/         # Utility scripts
│   │   ├── utils/           # Helper utilities
│   │   └── index.ts         # Main server file
│   ├── data/                # SQLite database
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── contexts/        # React contexts
│   │   ├── pages/           # Page components
│   │   └── App.tsx          # Main app component
│   └── package.json
├── start-backend.sh         # Backend startup script
├── start-frontend.sh        # Frontend startup script
└── README.md
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the backend directory:

```env
PORT=3001
NODE_ENV=development
JWT_SECRET=your-super-secret-jwt-key
FRONTEND_URL=http://localhost:3000
DB_PATH=./data/job_links.db
```

### Frontend Configuration

The frontend automatically connects to `http://localhost:3001/api` by default.

## 📈 Business Model

- **Paid Access Only**: No free tier, all users must have active subscriptions
- **Subscription Types**: Basic and Premium
- **Link Curation**: Hand-picked job opportunities from various sources
- **Role-Based Organization**: Links organized by 40+ job roles
- **Usage Tracking**: Monitor user engagement and popular roles

## 🚀 Deployment

### Backend Deployment
1. Build the TypeScript: `npm run build`
2. Set production environment variables
3. Deploy to your preferred hosting platform (Heroku, AWS, etc.)

### Frontend Deployment
1. Build the React app: `npm run build`
2. Deploy the `build` folder to your hosting platform
3. Update API URLs for production

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the ISC License.

## 🆘 Support

For support or questions, please contact the development team.

---

**Built with ❤️ for H1B job seekers**
