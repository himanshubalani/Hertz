---
title: "The Ins and Outs of APIs"
datePublished: Wed Jan 25 2023 19:32:04 GMT+0000 (Coordinated Universal Time)
cuid: cldc2bvtf000408mc91z2arqu
slug: the-ins-and-outs-of-apis
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1674651464092/d01f063d-ecf6-4d11-aa38-fb7c489e4b18.png
tags: security, apis, rest-api, http-status, keploy-api-fellowship

---

As we read in my [previous blog](https://himanshubalani.hashnode.dev/the-acronym-that-lets-you-see-the-internet-safely), APIs are a type of agreement between web services defining how they will exchange data, like when accessing a map or your login details. Lets's now take a deeper dive.

# API Protocols

API protocols make it easier to share standardized information. Two popular protocols are :

* SOAP API
    
* REST API
    

## SOAP API

SOAP or Simple Objects Access Protocol is a web communication protocol used to transmit data over HTTP/HTTPS. Unlike the REST pattern, SOAP only supports the XML data format and strongly follows preset standards such as messaging structure, a set of encoding rules, and a convention for providing procedure requests and responses. SOAP can handle communications and make responses language-and platform-independent.

![Is REST better than SOAP? Yes, in these use cases](https://nordicapis.com/wp-content/uploads/soap_vs_rest.png align="center")

## REST API

REST - REpresentational State Transfer - is an architectural style that uses current and widely known technology, notably HTTP, and does not develop any new standards. REST can arrange data into XML, YAML, or any other machine-readable format, but JSON is commonly preferred. JavaScript Object Notation (JSON) is a lightweight and easy-to-parse text format for data exchange. Each JSON file contains collections of name/value pairs and ordered lists of values. Since these are universal data structures, the format can be used with any programming language.

There's a lot more to SOAP and REST than meets the eye and which I can't include in this blog. Check out [SOAP](https://stoplight.io/api-types/soap-api) and [REST](https://www.geeksforgeeks.org/rest-api-introduction/) here.

## The Contents of an API URL

### 1\. API Path URL

An API URL Path is a URL that allows you to access an API's numerous functionalities. These are usually the contents of any API request or response. There are 2 parts to any API URL:

1. Base URL
    
2. Endpoint
    

The **Base URL** is kind of like the base address for the specific API that you’re using.

The **Endpoint** is a specific “point of entry” in an API.

### 2\. Method

A method is like means of communication, a kind of convention to specify how to fetch/put data. They are again many methods one can use. They are discussed below.

### 3\. Header

API headers are like an extra source of information for each API call you make. Their job is to represent the meta-data associated with an API request and response. API Headers tell you about:

1. Request and Response Body
    
2. Request Authorization
    
3. Response Caching
    
4. Response Cookies
    

### 4\. Body

A **request** **body** is data sent by the client (like your browser) to the API. A **response** **body** is the data that API sends back to the client. Keep in mind that a request made using the GET or HEAD method cannot have a body, and in these circumstances, `null` is returned. To send data, you should use POST, PUT, PATCH, or DELETE.

### 5\. Parameters

API parameters are parameters that can be passed along with the endpoint to affect the response. They're usually behind the question mark (?) in the URL.

### 6\. Status Codes

The status codes are the equivalent of a conversation between your browser and the server on the Internet. These are used with APIs because they're dependent on HTTPS for security.

## The Request Methods

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674674971406/083d32e1-67cb-4173-aa2a-1097fe1f0050.png align="center")

HTTP request methods (often called HTTP verbs) are actions that you can tell an API to do. There are 5 kinds of methods one can use with APIs:

### 1\. GET - Retrieve Data

In simple terms, a GET request is a method of retrieving data from a data source using the internet. Since this approach is read-only, there is no chance that the data will be altered or corrupted.

### 2\. POST - Feed Data

In simple terms, a POST request is a method of sending data to a destination via the internet. It is often used to create new data entries.

### 3\. PUT - Override data

The PUT method is most often used to update existing data. It'll override the previous data with the new one.

### 4\. PATCH - Modify Data

The PATCH technique is quite similar to the PUT method in that it also updates existing data. The difference is that with the PUT method, the body of the request contains the entire new version, while with the PATCH method, the body of the request must contain only changes to certain data, specifically a set of instructions that describe how the data should. to be changed and the API service creates a new version based on this instruction.

### 5\. DELETE - Delete Data

The DELETE method is simply used to delete existing data in a data source. While it is feasible, you should normally avoid using the DELETE method in a resource collection since it deletes all of the items.

## Status Codes

An HTTP status code is **the server's** response to a **browser** request. When you visit a website, your browser sends a request to the **website's** server, and the server then responds to the **browser's** request with a three-digit code: the HTTP status code. In the 3-digit Status-Code, the first digit of the Status-Code defines the class of response. Responses are grouped into five classes:

1. Informational responses (`100` – `199`)
    
2. Successful responses (`200` – `299`)
    
3. Redirection messages (`300` – `399`)
    
4. Client error responses (`400` – `499`)
    
5. Server error responses (`500` – `599`)
    

Examples -

![](https://i.pinimg.com/564x/8e/52/cc/8e52cc06c3ab8b80b3e07536c8771c53.jpg align="left")

**A-OK!!**

**200 - OK:** The optimal status code for a typical, regularly functioning page is this one.

**404 - Not Found**: This means the file or page that the browser is requesting wasn’t found by the server.

**500 - Internal Server Error:** This status code denotes a server issue rather than a problem with missing or unavailable pages. A 500 is a common server error that will prevent API from accessing the websites.

Refer to [this article](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) for a detailed list.

## How is an API made?

![Puzzle pieces coming together to form a computer screen](https://opensource.com/sites/default/files/lead-images/puzzle_computer_solve_fix_tool.png align="left")

[Source](https://opensource.com/sites/default/files/lead-images/puzzle_computer_solve_fix_tool.png)

### Routes

Routes are represented as URIs in REST APIs. Routing refers to choosing an application's response to a client request for a certain endpoint, which is a URI (or path) and an HTTP request type in particular (GET, POST, and so on).

Every route has the option of having one or more handler functions that are called when the route matches. Routes pass supported requests (and data encoded in request URLs) to appropriate controller functions.

### Controller

Controllers are typically callback functions that correspond to the routers to handle requests. It is a good design principle to keep the code concise and readable.

Based on the incoming request URL and HTTP verb, API can decide which API controller and action method to execute.

### Models

Models define the content and format of the data to be sent and received.

## Protect APIs at all costs

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674672015489/f4a88d48-880c-4103-94f0-5a2d6577b862.png align="center")

Here are some tips to do so.

* Always implement an **HTTPS connection** while working with APIs. It'll ensure an encrypted and secure session on the browser.
    
* Always hash all passwords. Password hashing is a common way to encrypt passwords.
    
* API Key should not be visible to anyone except you. If you use an API key, never include it in the URL. This also applies to passwords, usernames, and session tokens. Neither of them should be displayed in the API parameters. When it comes to API keys, those are used between applications that recognize each other.
    
* Use OAuth, it is used to authorize and authenticate the users while the API key is used to authenticate and use the applications. OAuth allows users to sign into one application/platform and then view data or perform actions in another.
    
* Including a timestamp in the request headers is an excellent way to increase security. The server will be able to determine whether the request was sent in a reasonable amount of time or not.
    

---

*This blog article is a part of the task given by* *Keploy* *under their* [***Keploy API Fellowship***](https://fellowship.keploy.io/) *program to test understanding of the topics covered by them. This is an excellent way of learning in public.*