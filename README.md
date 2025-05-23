# Reflection

## Original Code: Running One Server + Three Clients

This program has two main components:

* **WebSocket Server**: Accepts multiple client connections and broadcasts messages to all connected clients.
* **WebSocket Client**: Connects to the server and can both send and receive messages.

To run the WebSocket server:

```bash
cargo run --bin server
```

To run the WebSocket client:

```bash
cargo run --bin client
```

When a message is typed by a client, the server will broadcast that message to **all** clients. For example, if Client 1 sends a message, the server sends it back to Client 1, Client 2, and Client 3. The same applies if Client 2 or Client 3 sends a message — it is broadcasted to everyone.


## Modify the Port


If you only change the port on the client side, the client won’t be able to connect to the server. This is because the connection is bidirectional — both the client and server must use the same port.

Therefore, you also need to update the port on the server side. Once both client and server are configured with the same port, they can connect to each other again without any issues.