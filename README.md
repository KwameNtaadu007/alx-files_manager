# Files Manager

## Overview

This project is a back-end application built using Node.js, Express, MongoDB, Redis, and other related technologies. It provides functionalities for user authentication, file management, and background processing. The primary objective is to create a simple platform for users to upload, view, and manage files securely.

## Features

- **User Authentication**: Users can authenticate via tokens to access the system.
- **File Listing**: List all files available in the system.
- **File Upload**: Users can upload new files to the platform.
- **Permission Management**: Change permissions of files as needed.
- **File Viewing**: View files stored in the system.
- **Thumbnail Generation**: Generate thumbnails for image files.
- **Background Processing**: Utilizes Bull for background processing tasks.
- **Pagination**: Manage large sets of data with pagination support.

## Installation

1. Clone the repository:

    ```
    git clone https://github.com/yourusername/files-manager.git
    ```

2. Install dependencies:

    ```
    cd files-manager
    npm install
    ```

3. Configure environment variables:

    Create a `.env` file in the root directory and configure the following variables:

    ```
    PORT=3000
    MONGODB_URI=mongodb://localhost:27017/files_manager
    REDIS_URI=redis://localhost:6379
    ```

4. Start the server:

    ```
    npm start
    ```

## API Endpoints

- **POST /api/auth/login**: User login with credentials.
- **POST /api/auth/register**: Register a new user.
- **GET /api/files**: List all files.
- **POST /api/files/upload**: Upload a new file.
- **PUT /api/files/:id/permissions**: Change permissions of a file.
- **GET /api/files/:id**: View a file.
- **GET /api/files/:id/thumbnail**: Get thumbnail for an image file.

## Dependencies

- **Express**: Web framework for Node.js.
- **Mongoose**: MongoDB object modeling for Node.js.
- **Bull**: Redis-backed queue for background processing.
- **Multer**: Middleware for handling multipart/form-data.
- **Sharp**: Image processing library for thumbnail generation.
- **jsonwebtoken**: JSON Web Token implementation for authentication.
- **bcryptjs**: Password hashing library.
- **dotenv**: Loads environment variables from a .env file.

## Testing

Unit tests are written using Mocha and Chai. Run the tests with:

```
npm test
```


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

