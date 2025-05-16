# Note-Taking-Backend

## Introduction

This project is a backend service for a note-taking application. It provides APIs for creating, reading, updating, and deleting notes.

## Features

- User authentication and authorization
- CRUD operations for notes
- Search functionality
- Tagging system

## Prerequisites

- Node.js
- npm
- MongoDB (or any other database you are using)

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd Note-taking-app/backend
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Set up environment variables:

   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```
     DB_URI=<your-database-uri>
     PORT=3000
     JWT_SECRET=<your-jwt-secret>
     ```

5. Start the server:
   ```bash
   npm start
   ```

## Workflow

1. **Development**: Use `npm run dev` to start the server with hot-reloading.
2. **Testing**: Run tests using `npm test`.
3. **Deployment**: Deploy the application using your preferred cloud service.

## Database Schema

- **User**

  - `id`: ObjectId
  - `username`: String
  - `email`: String
  - `password`: String (hashed)
  - `createdAt`: Date

- **Note**
  - `id`: ObjectId
  - `title`: String
  - `content`: String
  - `tags`: [String]
  - `author`: ObjectId (refers to User)
  - `createdAt`: Date
  - `updatedAt`: Date

## API Endpoints

- **Authentication**

  - `POST /api/auth/register`: Register a new user
  - `POST /api/auth/login`: Login a user

- **Notes**
  - `GET /api/notes`: Get all notes
  - `POST /api/notes`: Create a new note
  - `GET /api/notes/:id`: Get a note by ID
  - `PUT /api/notes/:id`: Update a note by ID
  - `DELETE /api/notes/:id`: Delete a note by ID

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License.
