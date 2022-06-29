# Heroku

Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

## Tips:
* Doesn't allow a static ip address, so if a DB requires a IP address to use a Proxy service is needed or a alternative Cloud service should be used.

# CLI (Command Line Interface)

| Command     | Action |
| ----------- | ----------- |
| heroku login | Login to Heroku CLI through web browser |
| heroku login -i | Login to Heroku CLI through commandline |
| heroku version | Displays current version installed |
| heroku update | Updates Heroku CLI to newest version |
| heroku access -a `ApplicationName` | Shows emails who have access to application |
| heroku access:add `EmailAddress` | Adds email to those that have access to application |
| heroku access:remove `EmailAddress` | Removes email to those that have access to application |
| heroku apps:info -a `ApplicationName` | Lists info about given application |
| heroku logs -t -a `ApplicationName` | Shows logs dynamically printed to command line |