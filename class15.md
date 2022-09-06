
# Reading


   ### What is OAuth? 
   
   OAuth is an open-standard authorization protocol or framework that provides applications the ability for “secure designated access.” For example, you can tell Facebook that it’s OK for ESPN.com to access your profile or post updates to your timeline without having to give ESPN your Facebook password. This minimizes risk in a major way: In the event ESPN suffers a breach, your Facebook password remains safe.
 ### Give an example of what using OAuth would look like.
  
 
 The simplest example of OAuth in action is one website saying “hey, do you want to log into our website with other website’s login?” In this scenario, the only thing the first website – let’s refer to that website as the consumer – wants to know is that the user is the same user on both websites and has logged in successfully to the service provider – which is the site the user initially logged into, not the consumer.
 
 
  ### How does OAuth work? What are the steps that it takes to authenticate the user?
  
   1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
   1.  The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
   1. The first site gives this token and secret to the initiating user’s client software.
   1. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
   1.  If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second we
   1.  The user approves (or their software silently approves) a particular transaction type at the first website.
   1. The user is given an approved access token (notice it’s no longer a request token).
    
   1. The user gives the approved access token to the first website.
   1.  The first website gives the access token to the second website as proof of authentication on behalf of the user.
   1. The second website lets the first website access their site on behalf of the user.
   1.  The user sees a successfully completed transaction occurring.
   1.   OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
   
   
   
   
   
   ### What is OpenID?  
   
OpenID Connect 1.0 is a simple identity layer on top of the OAuth 2.0 protocol. It allows Clients to verify the identity of the End-User based on the authentication performed by an Authorization Server, as well as to obtain basic profile information about the End-User in an interoperable and REST-like manner.

==========================================================================================================================

  
  1. What is Authorization Code Flow? With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user
  1. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)? During authentication, mobile and native applications can use the Authorization Code Flow, but they require additional security. Additionally, single-page apps have special challenges. To mitigate these, OAuth 2.0 provides a version of the Authorization Code Flow which makes use of a Proof Key for Code Exchange (PKCE).
  1. What is Implicit Flow with Form Post?    As an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets. While this is no longer considered a best practice for requesting Access Tokens, when used with Form Post response mode, it does offer a streamlined workflow if the application needs only an ID token to perform user authentication.

  1. What is Device Authorization Flow?
With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. This avoids a poor user experience for devices that do not have an easy way to enter text. To do this, device apps use the Device Authorization Flow (ratified in OAuth 2.0), in which they pass along their Client ID to initiate the authorization process and get a token.

  1. What is Resource Owner Password Flow? 
The Resource Owner Password Credentials flow is a server to server flow. The user is authenticated by the client passing the username and password in the request. This is an anti-pattern and the flow only exists to provide an outlet for applications that need to be migrated to use OAuth protected APIs, but cannot be re-written.



