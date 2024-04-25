
# Real-time Collaboration Tool Documentation

## Introduction
Welcome to the documentation for the Real-time Collaboration Tool project. This document will guide you through the features, setup, and usage of the application.

## Features
- **User Authentication**: Allow users to sign up, log in, and manage their accounts.
- **Document Management**: Enable users to create new documents, view existing ones, and manage them (e.g., rename, delete).
- **Real-time Editing**: Implement real-time collaboration using WebSockets or a similar technology. Users should see changes made by others in real-time without needing to refresh the page.
- **Rich Text Editing**: Integrate a rich text editor like Draft.js or Slate.js to allow users to format text, insert images, and add links.
- **Collaborator Presence**: Show who else is currently viewing/editing a document.
- **Chat Functionality**: Add a chat feature so collaborators can communicate with each other while working on the document.
- **Offline Support**: Implement offline support using service workers, allowing users to continue working on documents even when they lose internet connection.
- **Version History**: Keep a history of document changes and allow users to revert to previous versions if needed.
- **Notifications**: Notify users about changes made by collaborators or new chat messages.

## Setup
1. **Clone the Repository**: Clone the project repository from GitHub: [repository URL].
2. **Install Dependencies**: Navigate to the project directory and run `npm install` to install the necessary dependencies.
3. **Configure Environment Variables**: Create a `.env` file in the project root and define the required environment variables, including database connection details, API keys, and other configurations.
4. **Run the Application**: Execute `npm start` to start the development server. The application will be accessible at `http://localhost:3000` by default.

## Tables

### Database Schema
| Table Name    | Columns                                  | Description                            |
|---------------|------------------------------------------|----------------------------------------|
| Users         | UserID (PK), Username, Email, Password   | Stores user information                |
| Documents     | DocumentID (PK), Title, Content          | Stores document information            |
| Collaborators | CollaboratorID (PK), UserID (FK), DocumentID (FK) | Maps users to documents they collaborate on |
| ChatMessages  | MessageID (PK), UserID (FK), DocumentID (FK), Message, Timestamp | Stores chat messages related to documents |

### Environment Variables
| Variable Name    | Description                                |
|------------------|--------------------------------------------|
| PORT             | Port number for the server to listen on    |
| DB_HOST          | Database host URL                          |
| DB_NAME          | Name of the database                       |
| DB_USER          | Database username                          |
| DB_PASSWORD      | Database password                          |
| JWT_SECRET       | Secret key for JSON Web Token encryption   |
| WEBSOCKET_URL    | WebSocket server URL for real-time updates|

## Usage
1. **Sign Up/Login**: Users can sign up for a new account or log in with their existing credentials.
2. **Document Management**: After logging in, users can create new documents, view existing ones, and manage them from the dashboard.
3. **Real-time Collaboration**: When viewing a document, changes made by other collaborators will be reflected in real-time. Users can start editing the document immediately.
4. **Rich Text Editing**: Use the integrated rich text editor to format text, insert images, and add links.
5. **Chat**: Collaborators can communicate with each other using the chat feature available alongside the document editing area.
6. **Offline Support**: Even if users lose internet connection, they can continue working on documents. Changes will be synced once the connection is restored.
7. **Version History**: Users can access the version history of a document and revert to previous versions if necessary.
8. **Notifications**: Users will receive notifications about changes made by collaborators or new chat messages.

## Technologies Used
- **Frontend**: React, Redux, WebSocket (or Socket.IO) for real-time communication, Draft.js (or Slate.js) for rich text editing.
- **Backend**:  Node.js, Express.jsfor user authentication, document management, and storing real-time collaboration data.

## Contributing
Contributions to the project are welcome! If you find any bugs or have suggestions for new features, please open an issue or submit a pull request on GitHub.

## License
This project is licensed under the MIT LICENCE. See the LICENSE file for more details.

## Contact
For questions or inquiries, feel free to contact kelvin kimani at kwakaba06@gmail.com.
