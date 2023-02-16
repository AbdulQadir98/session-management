# How sessions works

When the client makes a login request to the server, the server will create a session and store it on the server-side. When the server responds to the client, it sends a cookie. This cookie will contain the session’s unique id stored on the server, which will now be stored on the client. This cookie will be sent on every request to the server.

We use this session ID and look up the session saved in the database or the session store to maintain a one-to-one match between a session and a cookie. This will make HTTP protocol connections stateful.

# The difference between session and cookie

As you might have noticed, we’ve introduced a new concept called a cookie. We need to answer the question of what is the difference between a session and a cookie.

A cookie is a key-value pair that is stored in the browser. The browser attaches cookies to every HTTP request that is sent to the server.

In a cookie, you can’t store a lot of data. A cookie cannot store any sort of user credentials or secret information. If we did that, a hacker could easily get hold of that information and steal personal data for malicious activities.

On the other hand, the session data is stored on the server-side, i.e., a database or a session store. Hence, it can accommodate larger amounts of data. To access data from the server-side, a session is authenticated with a secret key or a session id that we get from the cookie on every request.

# node modules

Express - a web framework for Node.js used to create HTTP web servers. Express provides an easy-to-use API to interact with the webserver.

Express-session - an HTTP server-side framework used to create and manage a session middleware. This tutorial is all about sessions. Thus Express-session library will be the main focus.

Cookie-parser - used to parse cookie header to store data on the browser whenever a session is established on the server-side.

## reference

https://www.section.io/engineering-education/session-management-in-nodejs-using-expressjs-and-express-session/
