# Simple HTTP-Like Server

In this repo, You will find a simple HTTP-like server written in Python. The server is build over TCP sockets and uses a minimalistic version of the HTTP protocol.

## How It Works

1. Server Reception:

    This server uses a TCP socket and listens for incoming connections. When a connection is received, the server reads the incoming data and put it into a buffer. Every received data is added to this buffer until the end marker `\0` is found. After the end marker is found, the server processes the request. Because the server is stateless, it closes the connection after sending the response.

2. Request Handling:

    The requests uses JSON format. The request is a JSON object with the following fields:

    - `method`: The HTTP method used in the request.
    - `path`: The path of the requested resource.
    - `data`: The data sent in the request body.

## How to Run

To run the server, you need to have Python installed on your machine. You can run the server by executing the `main.py` file in the `src` folder following command in your terminal:

```bash
python main.py
```
