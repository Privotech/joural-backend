# Journal Application Backend

This is the backend API for the journal/blog application.

## Features

- CRUD operations for posts
- Image upload functionality
- MongoDB database integration
- RESTful API endpoints

## Setup

1. Install dependencies:
```bash
npm install
```

2. Make sure MongoDB is running on your system

3. Start the server:
```bash
npm start
```

For development with auto-restart:
```bash
npm run dev
```

## API Endpoints

### Posts
- `GET /api/posts` - Get all posts
- `GET /api/posts/:id` - Get single post
- `POST /api/posts` - Create new post (supports image upload)
- `PUT /api/posts/:id` - Update post (supports image upload)
- `DELETE /api/posts/:id` - Delete post

### Image Upload
Images are uploaded via multipart/form-data and stored in the `/uploads` directory.
The API returns the image URL which can be accessed via `/uploads/[filename]`.

## Environment Variables

Create a `.env` file with:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/journal-app
```

## Dependencies

- Express.js - Web framework
- MongoDB - Database
- Mongoose - MongoDB object modeling
- Multer - File upload handling
- CORS - Cross-origin resource sharing
