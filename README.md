COMPANY: CODTECH IT SOLUTIONS

NAME: Aasim Kader

INTERN ID: CT04DY864

DOMAIN: FRONT END DEVELOPMENT

DURATION: 4 WEEEKS

MENTOR: NEELA SANTOSH

Description for chat application:

Structure of the File

The file follows the standard HTML5 structure:

Head Section:

Defines the character encoding and viewport settings for responsiveness.
Adds a title for the page: "Realtime Chat (React + WebSocket)".
Loads Tailwind CSS from a CDN for fast and simple styling.
Contains custom CSS to hide scrollbars (giving a clean design).

Body Section:

Contains a <div> with the id "root", which acts as the main mounting point for the React application.
Loads React, ReactDOM, and Babel via <script> tags. Babel allows JSX syntax to be compiled directly in the browser.
The React Components
The React code is wrapped inside a <script type="text/babel"> block.

Message Component:

A small functional component that displays a chat bubble.
It uses a me prop to decide whether the message belongs to the current user or another user.
If it’s the current user’s message, it is styled with a blue background and aligned to the right.
Otherwise, it is shown with a gray background aligned to the left.

ChatApp Component:
This is the main application component. It manages all the logic and state:

State Variables:

messages: An array storing the chat history.

input: Stores the current text typed by the user.

connected: A boolean that shows whether the WebSocket is connected.

References:

wsRef: Stores the WebSocket object so it can be reused.

listRef: Refers to the messages container for auto-scrolling.

Effects:

One effect automatically scrolls the message list when new messages arrive.

Another effect sets up the WebSocket connection to ws://localhost:3000.

On open, it sets connected to true.

On close, it sets connected to false.

On message, it updates the chat history with the received text.

Functions:

sendMessage(): Sends the user’s input through the WebSocket and adds it to the chat window.

handleKey(e): Allows pressing Enter to send a message quickly.

UI Layout:

Header: Shows the chat title and a connection status indicator (green for connected, red for disconnected).

Messages Area: Displays the conversation. If there are no messages, it shows a placeholder text.

Composer: Includes a text area for typing messages and a "Send" button. The button is disabled if not connected.

Styling and Design

Tailwind CSS classes give the application a modern, minimal look.

Rounded corners, shadows, and clean spacing make the chat interface user-friendly.

Auto-scroll ensures the user always sees the latest message.

Functionality

When the app starts, it tries to connect to a WebSocket server running on localhost:3000.
Once connected, users can type and send messages.
Messages sent by the user appear on the right in blue, while incoming messages from others appear on the left in gray.
The connection status updates in real time.

OUTPUT :

<img width="1316" height="666" alt="Image" src="https://github.com/user-attachments/assets/64cc5344-f388-42fd-a7d5-77ba35eb8100" />
