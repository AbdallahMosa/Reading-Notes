# Configuring Django Settings: Best Practices
  - Django developers may face a couple of issues when configuring their settings, some of these issues are:  
    - Different environments
    - Sensitive data
    - Sharing settings between team members
    - Django settings are a Python code

## Setting Django Configurations
  - settings_local.py : which is a file that is used to extend the main settings.py without directly changing itPros and Cons
And while this way is good as it's ignored by VCS, it raises some other problems like losing some of Django's environment settings as it's not in VCS, or having to create another file to share the default configurations with other developers.
  - A settings file for each environment: which is an extension of the previous approach as you would create a folder that would host a bunch of files that manages different things, but it differs as it is in VCS.
  - Environment variables: it is used usually for sensitive data.Pros and Cons
This approach is great as it separates code and configuration, allows you to have the same code for all environments and also does not use inheritance, but you'll still need to handle default configuration sharing between developers
## Django Settings: Best practices
  - Keep settings in environment variables.
  - Write default values for production configuration (excluding secret keys and tokens).
  - Don’t hardcode sensitive settings, and don’t put them in VCS.
  - Split settings into groups: Django, third-party, project.
  - Follow naming conventions for custom (project) settings.

#  What Is SSH
  - SSH, or Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

## Different Encryption Techniques SSH 
  - Symmetrical encryption
  - Asymmetrical encryption
  - Hashing
