# User data
- It is a bootstrap script which runs automaticaally when ec2 instance is first started
- It will not execute when we stop/start isntance or reboot instance
- It is used to
  - update Os and package
  - install software or agents
  - download files
- ec2 user data executes as a root user hence we do not need sudo
- It will run only once when instace first starts.
