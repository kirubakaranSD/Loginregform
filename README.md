# Document Storage System

A secure web application for storing personal documents (Aadhar card, Voter ID, etc.) with user authentication and secure link generation for sharing.

## Features

- **User Authentication**: Secure registration and login system
- **Document Upload**: Upload PDF and image files (JPEG, PNG)
- **Document Management**: View, download, and delete your documents
- **Secure Link Generation**: Create password-protected, time-limited links to share documents
- **Document Categories**: Organize documents by type (Aadhar Card, Voter ID, PAN Card, etc.)

## Technology Stack

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Backend**: Node.js with Express
- **Storage**: JSON file-based storage
- **Security**: bcrypt for password hashing, crypto for secure tokens

## Installation

1. Install Node.js dependencies:
```bash
npm install
```

2. Start the server:
```bash
npm start
```

For development with auto-reload:
```bash
npm run dev
```

3. Open your browser and navigate to:
```
http://localhost:3000
```

## Project Structure

```
/
├── public/              # Frontend files
│   ├── index.html      # Login page
│   ├── register.html   # Registration page
│   ├── dashboard.html  # User dashboard
│   ├── upload.html     # Document upload page
│   ├── secure-link.html # Secure link access page
│   ├── css/
│   │   └── style.css   # Styles
│   └── js/
│       ├── auth.js     # Authentication logic
│       ├── dashboard.js # Dashboard functionality
│       ├── upload.js   # Upload functionality
│       └── secure-link.js # Secure link access
├── server/             # Backend files
│   ├── server.js       # Express server
│   ├── routes/         # API routes
│   │   ├── auth.js     # Authentication routes
│   │   ├── documents.js # Document routes
│   │   └── links.js    # Secure link routes
│   ├── middleware/
│   │   └── auth.js     # Authentication middleware
│   └── utils/
│       ├── storage.js  # Data storage utilities
│       └── encryption.js # Encryption utilities
├── data/               # JSON data files (auto-created)
│   ├── users.json
│   ├── documents.json
│   └── links.json
└── uploads/            # Uploaded documents (auto-created)
```

## Usage

### Registration
1. Click "Register here" on the login page
2. Fill in your name, email, and password
3. Password must be at least 6 characters

### Upload Documents
1. Login to your account
2. Click "Upload Document"
3. Select a file (PDF, JPEG, or PNG)
4. Choose a category
5. Add an optional description
6. Click "Upload Document"

### Generate Secure Link
1. Go to Dashboard
2. Click "Generate Secure Link"
3. Select documents to share
4. Optionally set a password
5. Set expiration time (in hours)
6. Click "Generate Link"
7. Copy the generated link to share

### Access Secure Link
1. Open the secure link in a browser
2. Enter password if required
3. View and download shared documents

## Security Features

- Passwords are hashed using bcrypt
- Secure token generation for links
- Session-based authentication
- File type and size validation
- Time-limited secure links
- Optional password protection for links

## File Limits

- Maximum file size: 10MB
- Supported formats: PDF, JPEG, PNG

## Notes

- All data is stored locally in JSON files
- Uploaded files are stored in the `uploads/` directory
- For production use, consider:
  - Using a proper database (MongoDB, PostgreSQL)
  - Implementing HTTPS
  - Using environment variables for secrets
  - Adding rate limiting
  - Implementing file encryption at rest

## License

ISC

