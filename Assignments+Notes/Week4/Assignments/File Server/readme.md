
# File Server Application

This project is a simple file server built with Node.js and Express. The application allows users to list files in a directory and retrieve the content of specific files. The file operations are handled using Node.js's built-in `fs` module.

## Features

- **List Files**: Retrieve a list of all files in the `./files/` directory.
- **Read File Content**: Retrieve the content of a specific file by its name.
- **Error Handling**: Handles cases where files are not found or other routes are accessed.

## Assignment Details

This project was created as part of the Week 4.1 assignment given by Harkirat Bhaiya. In Week 4, he asked us to create a file server, which was the same assignment given to Cohort 2. To complete this assignment, I cloned the repository from Cohort 2 and adapted it to solve the assignment. My solution successfully passed all the tests created by Harkirat Bhaiya.

## Screenshot

<img width="1280" alt="Screenshot 2024-09-03 at 1 46 53 AM" src="https://github.com/user-attachments/assets/841c3458-84c9-4ba6-93e1-b3d2c8a5aa38">


## API Endpoints

1. **GET /files**
   - Returns a list of files present in the `./files/` directory.
   - **Response:** `200 OK` with an array of file names in JSON format.
   - **Example:** `GET http://localhost:1000/files`

2. **GET /file/:filename**
   - Returns the content of a given file by its name.
   - **Response:** `200 OK` with the file content as the response body if found, or `404 Not Found` if the file is not found.
   - **Example:** `GET http://localhost:1000/file/example.txt`
   - If the file is not found, the response will be `File not found`.

3. **Wildcard Route**
   - For any other route not defined in the server, a `404 Not Found` response is returned with the message `Route not found`.

## What I've Learned

During the development of this project, I learned:

- **Node.js `fs` Module**: How to use the `fs` module for reading directories and file contents.
- **Error Handling**: Managing errors gracefully, such as handling non-existent files or routes.
- **Path Module**: Using the `path` module to handle file paths safely across different environments.
- **Synchronous vs. Asynchronous Methods**: Understanding the difference between `fs.readdir` (asynchronous) and `fs.readFileSync` (synchronous) methods.

## How to Run

1. Clone the repository.
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Create a `files` directory in the root of the project and add some files to it for testing.
4. Start the server:
   ```bash
   node app.js
   ```
5. The server will run on `http://localhost:1000`.

## Testing

To test the application, run the following command:

```bash
npm run test-fileServer
```

### Troubleshooting

- **Port Conflicts**: If you encounter an error stating that port 1000 is in use, change the port in the `app.listen` method to another available port.


