# react-project-defense - The Future
**100% done**
<br></br>
**Social Network - The Future**
This is a social network web application built using React on the front-end and Node.js on the back-end. It features a follow/unfollow system, real-time chat, posts with comments and like functionality, profile options, and a recommended friends modal.

**Follow/Unfollow Feature**
The social network allows users to follow and unfollow other users. This feature is implemented using a PUT request to the server with the logged-in user's ID and the ID of the user they want to follow/unfollow. The server updates the database accordingly and sends back the updated friend list. The front-end then updates the friend list in the auth object and saves it to localStorage for persistence.

**Chat Feature**
The chat feature allows users to send and receive messages in real-time. It is implemented using WebSockets and the Socket.IO library. When a user logs in, a WebSocket connection is established with the server. The server maintains a list of connected clients and their corresponding WebSocket connections. When a user sends a message, the front-end emits a chatMessage event to the server with the message content, the sender's ID, and the recipient's ID. The server then sends the message to the recipient via their WebSocket connection. When a user receives a message, the front-end adds it to the chat history for the corresponding chat.

**Posts Feature**
The posts feature allows users to create, read, update, and delete posts. Users can also like and comment on posts. This feature is implemented using RESTful API endpoints. When a user creates a post, a POST request is sent to the server with the post content and the logged-in user's ID. The server creates a new post in the database and sends back the updated post list. When a user updates or deletes a post, a PUT or DELETE request is sent to the server with the post ID and the logged-in user's ID. The server updates or deletes the post in the database and sends back the updated post list. When a user likes or unlikes a post, a PUT request is sent to the server with the post ID and the logged-in user's ID. The server updates the like list in the database and sends back the updated post list. When a user comments on a post, a POST request is sent to the server with the comment content, the post ID, and the logged-in user's ID. The server creates a new comment in the database and sends back the updated comment list.

**Profile Options**
Users can view and update their own profile information, including their name, email, password, and profile picture. This feature is implemented using RESTful API endpoints. When a user updates their profile information, a PUT request is sent to the server with the updated information and the logged-in user's ID. The server updates the user's profile information in the database and sends back the updated user object.

**Recommended Friends Modal**
The social network displays a recommended friends modal that suggests other users for the logged-in user to follow. This feature is implemented using a GET request to the server with the logged-in user's ID. The server returns a list of other users who are not already friends with the logged-in user. The front-end then displays the list of suggested users in the recommended friends modal.

<h2>Guide</h2>
**Getting Started**
To run the social network, first clone the repository to your local machine. Then, navigate to the client directory and run npm i to install the required dependencies. Next, navigate to the framework directory and run npm i to install the required dependencies for the server. You'll need to have MongoDB installed and running on your machine to run the server. Once everything is set
up, start the server by running npm start in the framework directory and start the client by running npm start in the client directory.

To use the chat feature, you'll need to have two users logged in from different IP addresses (e.g., one in incognito mode and one in a regular browser window).

Note: Make sure not to install the latest versions of the dependencies. Instead, let npm install the versions needed for the project.

**Contributing**
If you'd like to contribute to the project, feel free to fork the repository and submit a pull request with your changes. Before submitting a pull request, please make sure that your changes are thoroughly tested and documented.

**License**
This project is licensed under the MIT License. Feel free to use and modify the code as you see fit.
