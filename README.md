<body>

<h1>Group Chat Application</h1>

<p>This project is a simple group chat application developed in Java. It allows multiple clients to connect to a server and communicate with each other in a group chat environment.</p>

<h2>Features</h2>
<ul>
  <li><strong>Client-Server Architecture:</strong> The application follows a client-server architecture where clients connect to a central server to communicate with each other.</li>
  <li><strong>Multi-threaded Communication:</strong> Each client and server communication is handled on separate threads to allow concurrent communication with multiple clients.</li>
  <li><strong>Username Identification:</strong> Clients can enter a username when connecting to the server, which is used to identify them in the chat.</li>
  <li><strong>Real-time Messaging:</strong> Messages are sent and received in real-time, allowing for seamless communication between clients.</li>
  <li><strong>Graceful Disconnect:</strong> Clients can gracefully disconnect from the server, and their departure is broadcasted to all other connected clients.</li>
</ul>

<h2>Project Functionality</h2>

<h3>Server Class</h3>
<p>The Server class is responsible for listening to clients attempting to connect. Upon connection, it spawns a new thread to handle each client. This allows for concurrent communication with multiple clients.</p>

<h3>ClientHandler Class</h3>
<p>The ClientHandler class is responsible for communication with individual clients. It implements the <code>Runnable</code> interface, allowing each client instance to run on a separate thread. Instances of ClientHandler are saved in an ArrayList, enabling communication with multiple clients simultaneously. BufferedReader and BufferedWriter are used to read and write streams.</p>

<h3>Client Class</h3>
<p>The Client class represents a client in the chat application. It listens to messages from the server and includes a method to send messages entered by the user. Messages are identified and broadcasted by the ClientHandler.</p>

<h3>Port Configuration</h3>
<p>The port number is hardcoded into the main methods of the Server and Client classes. If the application is run on a single machine, the port number and the IP address should have the same value. If running on multiple machines, the user must update the port and IP values in the Client class to match the Server class values if necessary.</p>

<h3>Usage</h3>
<p>To compile and run the Server program, use the following commands:</p>
<pre>
javac Server.java
java Server
</pre>

<p>To compile and run the Client program, use the following commands:</p>
<pre>
javac Client.java
java Client
</pre>

<p>To start the application, begin by running the Server program. It can be launched in CMD or IDE terminal. Navigate to the source folder and type <code>java Server</code>. Once the Server is running, multiple Clients can be launched in the same manner.</p>

<p>Upon starting a Client, the user will be prompted to enter a username, and a message indicating their entry into the chat will be displayed. Users can then communicate with each other by exchanging messages. To exit the chat, the user can type <code>\\q</code>, and a message stating "The user has left the chat" will be displayed.</p>

<h2>References</h2>

<p>The code for this project was referenced and adjusted from:</p>
<ul>
  <li>WittCode, 2022. YouTube: <a href="https://www.youtube.com/watch?v=gLfuZrrfKes&t=167s">Java Socket Programming - Multiple Clients Chat</a> [Accessed 2023]</li>
</ul>

<h2>Contributors</h2>

<p>- <strong>Marijana Marinovic</strong>: <a href="https://github.com/marijana-marinovic">GitHub Profile</a></p>



</body>
</html>
