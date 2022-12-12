# Permissions & Postgresql

## Permissions
  - Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.
  - Permissions are used to grant or deny access for different classes of users to different parts of the API.

## How permissions are determined
  - Before running the main body of the view each permission in the list is checked. If any permission check fails, an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.
  - When the permission checks fail, either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

  1. The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
  2. The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
  3. The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.

## Setting the permission policy 
  - The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.
     - ``` 
                  REST_FRAMEWORK = {
              'DEFAULT_PERMISSION_CLASSES': [
                  'rest_framework.permissions.IsAuthenticated',
              ]
          }

       ```
  
  - If not specified, this setting defaults to allowing unrestricted access:
    
        ``` 
                  REST_FRAMEWORK = {
              'DEFAULT_PERMISSION_CLASSES': [
                  'rest_framework.permissions.AllowAny',
              ]
          }

       ```
       
 ## API Reference
  - AllowAny
  - IsAuthenticated
  - IsAdminUser
  - IsAuthenticatedOrReadOnly
