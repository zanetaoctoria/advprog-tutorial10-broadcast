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