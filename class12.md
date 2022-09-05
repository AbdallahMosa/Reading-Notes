# reading 

#

1. In your own words, describe what each group of status code represents:

   - 100's = These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.


   - 200's =These are the success codes. They tell the client that its request was accepted. In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.


   - 300's =These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location.


   - 400's =These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.


   - 500's =These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. These errors can be temporary or permanent. Usually it’s best for the client to retry the same request.



1. What is a status code 202? The HyperText Transfer Protocol (HTTP) 202 Accepted response status code indicates that the request has been accepted for processing, but the processing has not been completed; in fact, processing may not have started yet. The request might or might not eventually be acted upon, as it might be disallowed when processing actually takes plac
1. What is a status code 308?The HyperText Transfer Protocol (HTTP) 308 Permanent Redirect redirect status response code indicates that the resource requested has been definitively moved to the URL given by the Location headers. A browser redirects to this page and search engines update their links to the resource (in 'SEO-speak', it is said that the 'link-juice' is sent to the new URL).

1. What code would you use if a resource used to exist but no longer does?
1. What is the 'Forbidden' status code?The 403 Forbidden Error happens when the web page (or another resource) that you’re trying to open in your web browser is a resource that you’re not allowed to access. It’s called a 403 error because that’s the HTTP status code that the webserver uses to describe that kind of error.



========================================================================================================================

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env? to keep it hidden and no one ues it 
1. What is middleware? Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system. Data management, application services, messaging, authentication, and API management are all commonly handled by middleware.
1. What does `app.use(express.json())` do? to recive the data and use it in side the back-end
1. What does the `/:id` mean in a route? we used selecting  a specific item 


1. What does a `500` error status code mean?The 500 Internal Server error could be caused by an error during the execution of any policy within Edge or by an error on the target/backend server
1. What is the difference between a status `200` and a status `201`?
200 - OK
The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed.


201 - Created
A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).
