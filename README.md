# Basic Chat App Backend 

This README provides an overview and setup guide for the backend of a chat application using Express and Socket.IO.

## Overview

This chat application backend is built with Node.js, using Express for handling HTTP requests and Socket.IO for real-time bi-directional communication between web clients and the server. The application allows users to join chat rooms, send messages, and see other active users and rooms.

## Features

- Real-time chat functionality.
- Users can join and leave chat rooms.
- Broadcast messages to all users in a room.
- Display active users in a room.
- List all active chat rooms.
- Handle user connections and disconnections.

## Setup

### Prerequisites

- Node.js installed.
- Basic understanding of JavaScript and Node.js.

### Installation

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Run `npm install` to install the required dependencies.

### Running the Server

1. In the project directory, run `npm start`.
2. The server will start and listen on the port defined in the environment variable `PORT` or default to 8000.

## Environment Variables

- `PORT`: The port number on which the server will listen.
- `NODE_ENV`: The environment ('production' or 'development').

## Key Components

- **Express Server**: Sets up an HTTP server and listens on a specified port.
- **Socket.IO**: Manages real-time web socket connections.
- **UsersState**: An object that maintains the current state of users.
- **Event Listeners**: Socket.IO event listeners for various events like connection, disconnection, message, and room activities.

## API Endpoints

This application does not define REST API endpoints, as it primarily operates through web sockets.

## Socket Events

- `connection`: Establishes a socket connection with a client.
- `enterRoom`: Handles joining a room.
- `disconnect`: Manages user disconnection.
- `message`: Sends and receives chat messages.
- `activity`: Broadcasts user activity in a room.

## Utility Functions

- `buildMsg`: Formats a message object with name, text, and timestamp.
- User management functions: `activateUser`, `userLeavesApp`, `getUser`, `getUsersInRoom`, `getAllActiveRooms`.

## CORS Configuration

CORS (Cross-Origin Resource Sharing) is configured for both production and development environments.

## Conclusion

This backend setup provides a robust foundation for a chat application. It can be integrated with a front-end client to create a full-fledged chat application. 

## Note

For full functionality, a corresponding front-end application that connects to this server via web sockets is required.