## What is the HTTP

### Table of content
1. What is HTTP?
2. What is in HTTP request?
3. What is an HTTP method?
4. What are HTTP request headers?
5. What is in an HTTP request body?
6. What is in an HTTP response?
7. What’s an HTTP status code?
8. What are HTTP response headers?
9. What is in an HTTP response body?

### What is HTTP?
HTTP, or the Hypertext Transfer Protocol, is like the backbone of the internet, especially the World Wide Web. Its job is to make sure webpages load when you click on links. Think of it as a set of rules that computers follow to share information. When you want to see a webpage, your computer talks to a server, and the server sends back the webpage you asked for. It's a crucial part of how the internet works!

### What is in HTTP request?
Each HTTP request made across the Internet carries with it a series of encoded data that carries different types of information. A typical HTTP request contains:
1. HTTP version type
2. a URL
3. an HTTP method
4. HTTP request headers
5. Optional HTTP body
   
### What is an HTTP method?
An HTTP method, also known as an HTTP verb, is like telling the internet what you want to do. It's the action your computer is asking for when it talks to a server. For instance, **GET** is like asking for information, like opening a webpage. On the other hand, **POST** is like telling the server something, like when you submit a form with your username and password on a website.

### What are HTTP request headers?
![HTTP request body](../picture/http-request-headers.png)
HTTP headers are like text notes with important information **in pairs**. They come with every **request and response** in web communication. These notes share essential details, such as the type of browser being used and the data that's being asked for.

### What is in an HTTP request body?
In an HTTP request, the body is where the actual information is sent to the web server. This includes things like usernames, passwords, or any data entered into a form that is being submitted. It's like the content of a letter you send, carrying the specific details you want to share with the server.

### What is in an HTTP response?
An HTTP response is what web clients (often browsers) receive from an Internet server in answer to an HTTP request. These responses communicate valuable information based on what was asked for in the HTTP request.

A typical HTTP response contains:

1. an HTTP status code
2. HTTP response headers
3. optional HTTP body

### What’s an HTTP status code?
HTTP status codes are three-digit numbers that tell you if an HTTP request was successful or not. These codes are divided into five groups, each serving a specific purpose.

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error

### What are HTTP response headers?
![HTTP response headers](../picture/http-response-headers.png)

Just like when you ask for something on the internet and get a response, that response also comes with headers. These headers carry important details, like the language and format of the information that's included in the response. It's a way for the server to let your device know how to understand and process the data it's sending back to you.

### What is in an HTTP response body?
Successful HTTP responses to ‘GET’ requests generally have a body which contains the requested information. In most web requests, this is HTML data that a web browser will translate into a webpage.