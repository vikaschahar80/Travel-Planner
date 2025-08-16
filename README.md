# Travel Planner App

A comprehensive full-stack mobile application designed to help users efficiently plan and manage their trips. The app allows users to explore destinations, create detailed itineraries, manage budgets, and collaborate with other travelers. Features a seamless UI, real-time data management, and secure authentication.

## 🚀 Features

### Core Features
- **User Authentication**: Secure Google OAuth login with JWT token management
- **Trip Creation & Management**: Create, edit, and organize multiple trips
- **Itinerary Planning**: Detailed day-by-day activity scheduling
- **Destination Explorer**: Search and add places using Google Places API
- **Budget Management**: Set trip budgets and track expenses
- **Expense Tracking**: Categorize and split expenses among travelers
- **Collaborative Planning**: Invite friends via email to join trips
- **Interactive Maps**: View trip locations and get directions
- **Photo Management**: Upload and organize trip photos
- **Real-time Updates**: Live synchronization across devices

### Advanced Features
- **Google Places Integration**: Rich place details, photos, reviews, and ratings
- **Email Invitations**: Send trip invites with direct join links
- **Multi-user Support**: Multiple travelers per trip with role management
- **Offline Capability**: Basic functionality works without internet
- **Responsive Design**: Optimized for various screen sizes

## 🛠 Tech Stack

### Frontend
- **React Native** (0.74.1) - Cross-platform mobile development
- **React Navigation** (6.1.17) - Navigation and routing
- **React Native Maps** (1.18.0) - Interactive map integration
- **React Native Vector Icons** (10.2.0) - Icon library
- **Axios** (1.7.2) - HTTP client for API calls
- **AsyncStorage** (2.0.0) - Local data persistence
- **JWT Decode** (4.0.0) - Token management

### Backend
- **Node.js** - Runtime environment
- **Express.js** (4.19.2) - Web framework
- **MongoDB** (8.4.0) - NoSQL database
- **Mongoose** (8.4.0) - MongoDB ODM
- **JWT** (9.0.2) - Authentication tokens
- **Nodemailer** (6.9.15) - Email functionality
- **Multer** (1.4.5) - File upload handling
- **CORS** (2.8.5) - Cross-origin resource sharing

### External APIs
- **Google Places API** - Location search and details
- **Google OAuth** - User authentication
- **Google Maps API** - Map integration

### Development Tools
- **Metro** - React Native bundler
- **Babel** - JavaScript compiler
- **ESLint** - Code linting
- **Jest** - Testing framework

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **React Native CLI**
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, macOS only)
- **MongoDB** (local installation or MongoDB Atlas account)
- **Google Cloud Console** account (for Places API)

## 🔧 Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd Travel-Planner-App-main
```

### 2. Install Dependencies

#### Frontend Dependencies
```bash
npm install --legacy-peer-deps
```

#### Backend Dependencies
```bash
cd api
npm install
```

### 3. Environment Configuration

Create a `.env` file in the `api` directory:

```bash
# MongoDB Configuration
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster-url>/?retryWrites=true&w=majority
MONGODB_DB=travelplanner

# Email Configuration (Optional - for invite emails)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Google API Keys (Already configured in the app)
# GOOGLE_PLACES_API_KEY=your_google_places_api_key
# GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

### 4. MongoDB Setup

#### Option A: MongoDB Atlas (Recommended)
1. Create a MongoDB Atlas account
2. Create a new cluster
3. Add your IP address to Network Access
4. Create a database user with read/write permissions
5. Get your connection string and update `MONGODB_URI`

#### Option B: Local MongoDB
1. Install MongoDB locally
2. Start MongoDB service
3. Use connection string: `mongodb://127.0.0.1:27017`

### 5. Google API Setup (Optional)
If you want to use your own Google API keys:

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select existing one
3. Enable the following APIs:
   - Places API
   - Maps JavaScript API
   - Geocoding API
4. Create API keys and restrict them appropriately
5. Update the API keys in the relevant files

## 🚀 Running the Project

### 1. Start the Backend Server
```bash
cd api
npm start
```
The server will start on `http://localhost:8000`

### 2. Start the Metro Bundler
```bash
# From the root directory
npm start
```

### 3. Run on Android
```bash
npm run android
```

### 4. Run on iOS (macOS only)
```bash
npm run ios
```

## 📱 App Structure

```
Travel-Planner-App-main/
├── api/                    # Backend server
│   ├── index.js           # Main server file
│   ├── models/            # MongoDB schemas
│   └── package.json
├── screens/               # React Native screens
│   ├── LoginScreen.js     # Authentication
│   ├── HomeScreen.js      # Main dashboard
│   ├── CreateTrip.js      # Trip creation
│   ├── TripScreen.js      # Trip details
│   └── ...
├── components/            # Reusable components
├── navigation/            # Navigation configuration
├── App.js                 # Main app component
└── package.json
```

## 🔐 Authentication

The app uses Google OAuth for authentication:
- Users sign in with their Google account
- JWT tokens are generated for session management
- Tokens are stored securely using AsyncStorage
- Automatic token refresh and validation

## 📊 Database Schema

### User Model
- Google ID, email, name, photo
- Created trips and joined trips
- Profile preferences

### Trip Model
- Trip details (name, dates, destination)
- Itinerary with daily activities
- Places to visit with Google Places data
- Budget and expenses
- Travelers list

## 🧪 Testing

Run tests using:
```bash
npm test
```

## 📦 Building for Production

### Android
```bash
cd android
./gradlew assembleRelease
```

### iOS
```bash
cd ios
xcodebuild -workspace travelplanner.xcworkspace -scheme travelplanner -configuration Release
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🆘 Troubleshooting

### Common Issues

1. **Metro bundler issues**: Clear cache with `npx react-native start --reset-cache`
2. **Android build errors**: Clean project with `cd android && ./gradlew clean`
3. **MongoDB connection**: Check your connection string and network access
4. **Google API errors**: Verify API keys and billing setup

### Support

For issues and questions:
- Check the troubleshooting section
- Review the error logs
- Ensure all prerequisites are met
- Verify environment variables are set correctly

## 🔄 Updates

Stay updated with the latest changes:
- Check the repository regularly
- Follow the changelog
- Update dependencies as needed





