# Quick Start Guide - Job Listing Portal

## 🚀 Get Started in 5 Minutes

### Step 1: Install Dependencies

**Backend:**
```bash
cd "backend side"
npm install
```

**Frontend:**
```bash
cd "../frontend side"
npm install
```

### Step 2: Setup Environment

The `.env` file is already created in the backend directory. You can use it as is for local development, or update the MongoDB URI if needed.

### Step 3: Start MongoDB

**Windows:**
- Open Command Prompt as Administrator
- Run: `mongod`

**Mac/Linux:**
```bash
sudo systemctl start mongod
```

**Or use MongoDB Atlas (Cloud):**
1. Go to https://www.mongodb.com/cloud/atlas
2. Create free account and cluster
3. Get connection string
4. Update `MONGODB_URI` in `backend side/.env`

### Step 4: Run the Application

**Terminal 1 - Backend:**
```bash
cd "backend side"
npm start
```
Backend runs on: http://localhost:5000

**Terminal 2 - Frontend:**
```bash
cd "frontend side"
npm start
```
Frontend runs on: http://localhost:3000

### Step 5: Test the Application

1. **Open browser**: http://localhost:3000
2. **Register as Job Seeker**:
   - Click "Sign Up"
   - Fill form with role "Job Seeker"
   - Login with credentials

3. **Register as Employer** (in incognito/private window):
   - Click "Sign Up"
   - Fill form with role "Employer"
   - Login with credentials

4. **Test Features**:
   - **Employer**: Post a job, view dashboard
   - **Job Seeker**: Browse jobs, apply, track applications

## 📝 Test Credentials (After Registration)

Create your own test accounts:

**Job Seeker:**
- Email: jobseeker@test.com
- Password: test123
- Role: Job Seeker

**Employer:**
- Email: employer@test.com
- Password: test123
- Role: Employer

## ⚡ Common Commands

### Backend
```bash
npm start          # Start server
npm run dev        # Start with nodemon (auto-restart)
```

### Frontend
```bash
npm start          # Start React app
npm run build      # Build for production
```

## 🔍 Verify Installation

### Check Backend
```bash
curl http://localhost:5000/api/health
```
Should return: `{"status":"OK","message":"Server is running"}`

### Check Frontend
Open browser to http://localhost:3000
You should see the home page with "Find Your Dream Job Today"

## 🐛 Troubleshooting

### Backend won't start
- Check if MongoDB is running
- Verify port 5000 is not in use
- Check `.env` file exists

### Frontend won't start
- Check if port 3000 is available
- Clear npm cache: `npm cache clean --force`
- Delete node_modules and reinstall

### Can't connect to MongoDB
- Ensure MongoDB service is running
- Check MongoDB URI in `.env`
- Try: `mongodb://127.0.0.1:27017/job-portal`

### CORS errors
- Ensure backend is running on port 5000
- Check frontend API URL in `src/utils/api.js`

## 📚 Next Steps

1. ✅ Complete your user profile
2. ✅ Explore all features
3. ✅ Post jobs (as employer)
4. ✅ Apply to jobs (as job seeker)
5. ✅ Track applications

## 🎯 Key Features to Test

### Authentication
- [x] User registration
- [x] User login
- [x] Profile update
- [x] Password security

### Job Management
- [x] Create job posting
- [x] Edit job posting
- [x] Delete job posting
- [x] Search and filter jobs

### Applications
- [x] Submit application
- [x] Track application status
- [x] View applications (employer)
- [x] Update application status

## 💡 Tips

1. **Use two browsers** - One for job seeker, one for employer
2. **Check console** - For any errors or API responses
3. **MongoDB Compass** - Use GUI tool to view database
4. **Postman** - Test API endpoints directly

## 📞 Need Help?

- Check the main README.md for detailed documentation
- Review error messages in browser console
- Check backend terminal for server errors
- Verify all dependencies are installed

---

**Happy Coding! 🎉**
