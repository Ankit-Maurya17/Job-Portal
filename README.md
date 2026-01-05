Job-Portal

# Job Listing Portal

A dynamic full-stack web application that connects job seekers with employers efficiently. Built with React.js, Node.js, Express, and MongoDB.

## 🚀 Features

### For Job Seekers
- **User Registration & Login** - Secure authentication with JWT tokens
- **Browse Jobs** - Search and filter jobs by type, location, salary, and experience level
- **Job Details** - View comprehensive job information including responsibilities, qualifications, and benefits
- **Apply for Jobs** - Submit applications with resume and cover letter
- **Application Tracking** - Monitor application status in real-time
- **Profile Management** - Update personal information, skills, and experience

### For Employers
- **Post Jobs** - Create detailed job listings with all necessary information
- **Manage Listings** - Edit or delete job postings
- **View Applications** - Review applications from job seekers
- **Update Application Status** - Mark applications as reviewed, shortlisted, accepted, or rejected
- **Company Profile** - Showcase company information

### General Features
- **Secure Authentication** - Password hashing with bcrypt and JWT-based authorization
- **Real-time Notifications** - Stay updated on application statuses
- **Responsive Design** - Modern UI that works on all devices
- **Advanced Search** - Filter jobs with multiple criteria
- **Role-based Access Control** - Different features for job seekers and employers

## 🛠️ Tech Stack

### Frontend
- React.js 18
- React Router DOM 6
- Axios for API calls
- Lucide React for icons
- CSS3 for styling

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Bcrypt.js for password hashing
- Express Validator for input validation

## 📋 Prerequisites

Before running this application, make sure you have the following installed:
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn package manager

## 🔧 Installation & Setup

### 1. Clone or Download the Project
```bash
cd "New folder"
```

### 2. Backend Setup

Navigate to the backend directory:
```bash
cd "backend side"
```

Install dependencies:
```bash
npm install
```

Create a `.env` file in the backend directory:
```bash
cp .env.example .env
```

Edit the `.env` file with your configuration:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/job-portal
JWT_SECRET=your_super_secret_jwt_key_change_this
JWT_EXPIRE=7d
NODE_ENV=development
```

### ⚠️ IMPORTANT: Database Configuration

**Your data will now be saved permanently!** 

This project uses **persistent MongoDB** instead of in-memory storage. Follow one of these options:

#### Option A: MongoDB Atlas (Recommended - Free & Easy)
1. Read `backend side/QUICK_START_DATABASE.md` for 5-minute setup
2. No installation needed, completely free
3. Data accessible from anywhere

#### Option B: Local MongoDB
1. Read `backend side/DATABASE_SETUP.md` for installation guide
2. Install MongoDB on your computer
3. Faster for development

**📋 Quick Setup Checklist:** See `backend side/SETUP_CHECKLIST.md`

### 3. Frontend Setup

Navigate to the frontend directory:
```bash
cd "../frontend side"
```

Install dependencies:
```bash
npm install
```

### 4. Database Setup

**✅ Database is now configured for permanent storage!**

Your profiles, job posts, and applications will be saved permanently. See the database setup guides mentioned above for detailed instructions.

Quick verification:
```bash
# Start the backend server
npm run dev

# You should see:
# ✅ MongoDB Connected Successfully
# 💾 Database: job-portal
```

**📚 Detailed Guides:**
- `QUICK_START_DATABASE.md` - 5-minute MongoDB Atlas setup (Hindi + English)
- `DATABASE_SETUP.md` - Complete setup guide with troubleshooting
- `SETUP_CHECKLIST.md` - Step-by-step checklist
- `ARCHITECTURE_CHANGE.md` - Technical architecture details

## 🚀 Running the Application

### Start the Backend Server

From the `backend side` directory:
```bash
npm start
```

Or for development with auto-restart:
```bash
npm run dev
```

The backend server will start on `http://localhost:5000`

### Start the Frontend Application

From the `frontend side` directory:
```bash
npm start
```

The React app will start on `http://localhost:3000`

## 📱 Usage

### For Job Seekers

1. **Register**: Click "Sign Up" and select "Job Seeker" role
2. **Complete Profile**: Add your skills, experience, and resume
3. **Browse Jobs**: Use filters to find relevant positions
4. **Apply**: Submit applications with cover letters
5. **Track Applications**: Monitor status in "My Applications"

### For Employers

1. **Register**: Click "Sign Up" and select "Employer" role
2. **Add Company Info**: Complete your company profile
3. **Post Jobs**: Click "Post Job" and fill in details
4. **Manage Applications**: Review and update application statuses
5. **Update Jobs**: Edit or close job postings as needed

## 🔐 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/updateprofile` - Update user profile
- `PUT /api/auth/updatepassword` - Update password

### Jobs
- `GET /api/jobs` - Get all jobs (with filters)
- `GET /api/jobs/:id` - Get single job
- `POST /api/jobs` - Create job (Employer only)
- `PUT /api/jobs/:id` - Update job (Employer only)
- `DELETE /api/jobs/:id` - Delete job (Employer only)
- `GET /api/jobs/employer/myjobs` - Get employer's jobs

### Applications
- `POST /api/applications` - Create application (Job seeker only)
- `GET /api/applications/myapplications` - Get user's applications
- `GET /api/applications/job/:jobId` - Get job applications (Employer only)
- `GET /api/applications/:id` - Get single application
- `PUT /api/applications/:id/status` - Update application status (Employer only)

## 📁 Project Structure

```
New folder/
├── backend side/
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── jobController.js
│   │   └── applicationController.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Job.js
│   │   └── Application.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── jobs.js
│   │   └── applications.js
│   ├── middleware/
│   │   └── auth.js
│   ├── server.js
│   ├── package.json
│   └── .env
│
└── frontend side/
    ├── public/
    │   └── index.html
    ├── src/
    │   ├── components/
    │   │   ├── Navbar.js
    │   │   └── PrivateRoute.js
    │   ├── context/
    │   │   └── AuthContext.js
    │   ├── pages/
    │   │   ├── Home.js
    │   │   ├── Login.js
    │   │   ├── Register.js
    │   │   ├── Dashboard.js
    │   │   ├── Jobs.js
    │   │   ├── JobDetails.js
    │   │   ├── CreateJob.js
    │   │   ├── MyApplications.js
    │   │   └── Profile.js
    │   ├── utils/
    │   │   └── api.js
    │   ├── App.js
    │   ├── App.css
    │   ├── index.js
    │   └── index.css
    └── package.json
```

## 🔒 Security Features

- Password hashing with bcrypt (10 salt rounds)
- JWT token-based authentication
- Protected routes with middleware
- Role-based access control
- Input validation with express-validator
- Secure HTTP headers
- Environment variables for sensitive data

## 🎨 UI/UX Features

- Modern gradient design
- Responsive layout for all screen sizes
- Intuitive navigation
- Real-time form validation
- Loading states and error handling
- Smooth animations and transitions
- Accessible design patterns

## 🐛 Troubleshooting

### MongoDB Connection Issues
- Ensure MongoDB is running
- Check connection string in `.env`
- Verify network access if using MongoDB Atlas

### Port Already in Use
- Change `PORT` in backend `.env` file
- Or kill the process using the port

### CORS Issues
- Backend CORS is configured to allow all origins in development
- For production, update CORS settings in `server.js`

### Dependencies Issues
```bash
# Delete node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

## 📝 Environment Variables

### Backend (.env)
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/job-portal
JWT_SECRET=your_secret_key_here
JWT_EXPIRE=7d
NODE_ENV=development
```

## 🤝 Contributing

This is a project for learning purposes. Feel free to fork and modify as needed.

## 📄 License

This project is open source and available for educational purposes.

## 👥 Support

For issues or questions, please create an issue in the project repository.

## 🎯 Future Enhancements

- File upload for resumes
- Email notifications
- Advanced analytics dashboard
- Chat feature between employers and applicants
- Job recommendations based on profile
- Social media integration
- Payment integration for premium features

---

**Built with ❤️ using React.js, Node.js, Express, and MongoDB**
