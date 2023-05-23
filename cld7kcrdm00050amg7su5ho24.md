---
title: "The Acronym that lets you see the Internet safely"
seoTitle: "The Acronym that lets you see the Internet safely"
seoDescription: "HTTP (or HTTPS) is a protocol used everywhere for sending data between websites and your browser. An API acts as a mediator between apps and websites."
datePublished: Sun Jan 22 2023 15:57:47 GMT+0000 (Coordinated Universal Time)
cuid: cld7kcrdm00050amg7su5ho24
slug: the-acronym-that-lets-you-see-the-internet-safely
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1674396159109/76facb39-ae06-46df-a44c-086de1736f25.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1674402946389/bd75882f-fd4c-40c2-8c55-41a55cadf46f.png
tags: ssl, http, https, apis, keploy

---

## What are HTTP and HTTPS?

The Hypertext Transfer Protocol (HTTP) is the foundation of communications on the internet. It is the protocol that enables communication between websites, web browsers, and web servers. HTTP is used for transferring data between clients and servers, and it is the protocol that is used to access websites.

The Hypertext Transfer Protocol Secure (HTTPS) is an extension of the HTTP protocol that adds an extra layer of security in communications between clients and servers. HTTPS provides encryption of data between the two parties and is most commonly used for secure transactions such as payments, or to protect confidential information.

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674375547277/bfe5de9f-e88e-45f4-bcdb-fb7dc9a0d24c.gif align="center")](https://dribbble.com/shots/2321171-Secure-Area)

[Source](https://dribbble.com/shots/2321171-Secure-Area)

## How does this work?

A Computer Network connects two devices such as your mobile and a web server. To standardize a connection for all devices, the [ISO](https://www.iso.org/home.html) came up with the OSI Model of Computer Networking. The Open Systems Interconnection (OSI) model describes seven layers that computer systems use to communicate over a network.

![OSI Model and it's 7 layers](https://www.practicalnetworking.net/wp-content/uploads/2016/01/packtrav-osi-layers-236x300.png align="center")

[Source](https://www.practicalnetworking.net/series/packet-traveling/osi-model/)

End-user applications like web browsers and email clients operate at the application layer. It offers protocols that let computer software send and receive data and give users useful information. The HTTPS Protocol is a part of the Application Layer.

HTTP handles two types of methods

1. HTTP Request
    
2. HTTP Response
    

### HTTP Request

HTTP requests are messages sent by the client to initiate an action on the server. A request comprises of three parts -

1. Start Line - which includes the HTTP Method like `GET` or POST ,the request target(usually a URL) and the HTTP version (1.x or 2)
    
2. Headers - a word followed by a colon ( : ) and it's value
    
3. Body - Not needed often, but some requests send data to the server in order to update it: as often the case with `POST` requests (containing HTML form data) which require a body.
    

![Example of headers in an HTTP request](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages/http_request_headers3.png align="left")

[Source](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)

### HTTP Response

They are the responses received based on the request sent. It also has three parts-

1. Status Line - The start line of an HTTP response, It contains a protocol version, a status code( like 200, 404, 403) and coressponding status text (OK, Not Found, Forbidden)
    
2. Header - which is similar to Request Header.
    
3. Body - which is similar to Request Body
    

![Example of headers in an HTTP response](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages/http_response_headers3.png align="left")

[Source](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)

## The S in SSL and HTTPS

The S in SSL and HTTPS stands for **secure.**

**Secure Sockets Layer**, or **SSL**, is the industry-standard technology for maintaining a secure internet connection and protecting any sensitive data being communicated between two computers. It does this by stopping attackers from accessing and altering any information transferred, including sensitive personal details. This is accomplished by ensuring that any data sent between users and websites or between two systems remains unreadable. In order to prevent hackers from accessing data as it is sent over the network, it scrambles it using encryption methods.

*"Invisible to the end-user, a process called the “SSL handshake” creates a protected connection between your web server and web browser nearly instantaneously every time you visit a website. Websites secured by a SSL certificate will display* ***HTTPS*** *and the* ***small padlock icon*** *in the browser address bar. SSL certificates are used to protect both the end users’ information while it’s in transfer, and to authenticate the website’s organization identity to ensure users are interacting with legitimate website owners." ~* [DigiCert](https://www.digicert.com/how-tls-ssl-certificates-work)

![](https://cdn.dribbble.com/users/1172172/screenshots/3522879/media/92a56bed175f863b28adf68c601d332a.png align="left")

[Source](https://dribbble.com/shots/3522879-SSL-Secure-Sockets-Layer)

## What is an API and how does it fit in all of this?

An API (Application Programming Interface) is a set of rules and protocols that allows different software applications to communicate with each other. APIs enable developers to access the functionality of an application or service without having to know how the underlying code works. For example, a developer might use an API to access data from a social media platform, such as Twitter, and display that data on their own website.

![Graphic of a laptop sending a request to an API, the API getting information from a server, then responding to the request back to the computer](https://i1.wp.com/www.rstudio.com/blog/creating-apis-for-data-science-with-plumber/images/image1.png?zoom=1.25&w=578&ssl=1 align="left")

Another example would be look at sign-in options for a website or app.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674378314087/1144939c-f9b7-4a88-b99b-3aec040a7f53.png align="center")

The requests and responses are all handled by an API, even though the data transfer will vary based on the web service being utilised. Since APIs communicate data within the computer or application are not visible on the user interface, they appear to the user as a single, seamless connection.

The developer doesn't need to know the entire code of these companies, they make use of the available APIs to connecct to these apps who securely sign in the user. APIs hence simplify design and development of new applications and services, and integration and management of existing ones. But they offer other significant benefits to developers and organizations at large.

---

*This blog article is a part of the task given by* *Keploy* *under their* [*Keploy API Fellowship*](https://fellowship.keploy.io/) *program to test us on our understanding of the topics covered by them. This is an excellent way of learning in public.*