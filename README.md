# CashX - Cashback Rewards App

CashX is a platform that offers users cashback when they purchase products through affiliated vendors listed within the app. When a user clicks on a vendor (e.g., Amazon), they are redirected via our affiliate link to complete their purchase, and we track clicks and purchases to confirm cashback eligibility.

## Features

- **User Authentication**: Register, login, and Google OAuth integration
- **Product Browsing**: View products with cashback percentages
- **Affiliate Link Management**: Automatically generated tracking links
- **Cashback Tracking**: View transaction history and status
- **Multiple Verification Methods**:
  - Webhook callbacks from affiliate networks
  - Manual verification through admin dashboards
  - Self-reported purchases
- **Cashback Redemption**:
  - Bank transfer
  - UPI (Unified Payments Interface)

## Technology Stack

- **Frontend**: React, Tailwind CSS
- **Backend**: FastAPI (Python)
- **Database**: MongoDB
- **Authentication**: JWT + Google OAuth

## Setup

### Prerequisites

- Node.js and npm
- Python 3.8+
- MongoDB

### Installation

1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/cashx-app.git
cd cashx-app
```

2. Set up backend
```bash
cd backend
pip install -r requirements.txt
# Create .env file with your configuration
```

3. Set up frontend
```bash
cd frontend
npm install
# Create .env file with your configuration
```

### Environment Variables

#### Backend (.env)
```
MONGO_URL=mongodb://localhost:27017
DB_NAME=cashx
SECRET_KEY=your_secret_key_here
```

#### Frontend (.env)
```
REACT_APP_BACKEND_URL=http://localhost:8001
```

### Running the Application

1. Start the backend server
```bash
cd backend
uvicorn server:app --host 0.0.0.0 --port 8001 --reload
```

2. Start the frontend development server
```bash
cd frontend
npm start
```

3. Access the application at `http://localhost:3000`

## For Google OAuth Setup

1. Create a Google OAuth 2.0 Client ID:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project
   - Navigate to "APIs & Services" > "Credentials"
   - Click "Create Credentials" > "OAuth client ID"
   - Copy the Client ID

2. Update the Client ID in your code:
   - Replace `"YOUR_GOOGLE_CLIENT_ID"` in App.js with your actual Client ID

## License

MIT
