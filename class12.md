# read 12

## Describe in your own words what each group of status codes represents:

### 100's = The request has been received, and the server will attempt to complete it

### 200's indicate that the request has been successfully completed.

### 300's = Informs the client that the requested resource is no longer available at the expected location.

### 400s denote invalid requests.

### 500s indicate a server-side error.

## What is a status code 202?

### This code informs the client that the request was valid, but that it will be processed later

## What is a status code 308?

### This instructs the client to use a different URL to access the resource rather than the current one

## What code would you use if an update didn't return data to a client?

### 204 or 404

## What code would you use if a resource used to exist but no longer does?

### 409

## What is the 'Forbidden' status code?

### 4.3

----------

## Why do we need to pull our MongoDB database string out of our server and put it into our .env?

### To somehow be concealed so that other people do not use it and to ensure that when deploying the service, the path can be easily changed.

## What is middleware?

### Software that sits between an operating system and the programs that run on it. Middleware allows for communication and data management for distributed applications, essentially acting as a hidden translation layer.

## What does app.use(express.json()) do?

### It parses incoming JSON requests and stores the results in the req variable.

## What does the /:id mean in a route?

### Because this is a dynamic route, req.params.id will be whatever comes after summary/ in that particular request.

## What is the difference between PUT and PATCH?

### PUT is a resource modification method in which the client sends data that updates the entire resource. PATCH is a resource modification method in which the client sends incomplete data to be modified without adjusting the entire data.

## How do you make a default value in a schema?

### Default values for specific paths can be defined in your schemas. If you create a new document without specifying a path, the default will be used.

## What does a 500 error status code mean?

### it is a standard error response. It indicates that the server encountered an unexpected condition that prevented it from completing the request.

## What is the difference between a status 200 and a status 201?

### By far the most common status code returned is 200. Simply put, it means that the request was received, understood, and is being processed. A 201 status code indicates that a request was successful and that a resource was created as a result.