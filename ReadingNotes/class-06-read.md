# https://www.sitepoint.com/an-introduction-to-node-js/

Node Is Built on Google Chrome’s V8 JavaScript Engine

Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.

Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections.

Node allows you to do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier). For example, you can easily share code between the server and the client.

Another of Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases (such as MongoDB). JSON is ideally suited for consumption by a JavaScript program, meaning that when you’re working with Node, data can flow neatly between layers without the need for reformatting. You can have one syntax from browser to server to database.

