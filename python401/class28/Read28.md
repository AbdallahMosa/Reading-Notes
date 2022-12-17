# Authentication & Production Server

## What is JSON Web Token?
  - JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
 
## When should you use JSON Web Tokens?
  - Authorization
  - nformation Exchange

## What is the JSON Web Token structure?
  - Header
  - Payload
  - Signature

## How do JSON Web Tokens work?
  - In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.
  
  
# How to Use JWT Authentication with Django REST Framework 
  - The JWT is just an authorization token that should be included in all requests:
  - The JWT is acquired by exchanging an username + password for an access token and an refresh token.
  - The access token is usually short-lived (expires in 5 min or so, can be customized though).
  - The refresh token lives a little bit longer (expires in 24 hours, also customizable). It is comparable to an authentication session. After it expires, you need a full login with username + password again.

# Django Runserver Is Not Your Production Server
- If you want to run Django in production, be sure to use a production-ready web server like Nginx, and let your app be handled by a WSGI application server like Gunicorn.
- If you plan on running on Heroku, a web server is provided implicitly. You don’t have to take care of it. You just need to specify a command to run your application server (again, Gunicorn is fine) in the Procfile
