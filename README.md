# node-sse-example

Server-Sent Events (SSE) is a technology based on HTTP. On the client-side, it provides an API called EventSource (part of the HTML5 standard) that allows us to connect to the server and receive updates from it.

Before making the decision to use server-sent events, we must take into account two very important aspects:

- It only allows data reception from the server (unidirectional)
- Events are limited to UTF-8 (no binary data)
If your project only receives something like stock prices or text information about something in progress it is a candidate for using Server-Sent Events instead of an alternative like WebSockets.


# run server
```shell
cd sse-server
npm install
node server.js
```

# run client
```shell
cd sse-client
npm install
npm start
```

# send message
```curl
curl -X POST \
 -H "Content-Type: application/json" \
 -d '{"info": "Hello.", "source": "client1"}'\
 -s http://localhost:3000/fact
```
