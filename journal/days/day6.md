# Day 6 - Automation with Python

The utilization of Python for infrastructure management revolves around the automation of various aspects of IT infrastructure, encompassing servers, databases, and networking devices. This entails automating tasks like provisioning, configuration, and orchestration.

Python stands out as a favored language for infrastructure management, boasting a variety of tools and libraries designed to streamline these processes. Noteworthy tools for infrastructure management utilizing Python comprise:

 - Fabric
 - PyWinRM
 - Pulumi

## Fabric

Fabric is a Python library designed to streamline the execution of SSH commands and facilitate remote script execution. This functionality proves invaluable for automating tasks such as server configuration and deployment.

Here is an example in which we will be using the Fabric library to connect to a remote server using SSH, and then run the `ls -l` command on the remote server. The output of the command will be printed to the console.

``` python
from fabric import Connection

# Connect to the remote server
c = Connection('user@remote.host')

# Run a command on the remote server
result = c.run('ls -l')

# Print the output of the command
print(result.stdout)
```

## PyWinRM

 A Python library that can be used to automate Windows Remote Management tasks, which can be used to automate Windows server configuration and management.

## Pulumi

Pulumi is a Cloud Infrastructure as Code (CIaC) tool that empowers users to define and oversee cloud resources using multiple programming languages, Python included.

By utilizing Pulumi, you have the flexibility to write Python code that describes your infrastructure in a code-like manner. Afterward, the Pulumi Command-Line Interface (CLI) becomes instrumental in deploying and effectively managing the specified infrastructure in your cloud environment.


## Resources:

- [Learn more about Fabric](https://docs.fabfile.org/en/stable/index.html)
- [PyWinRM](https://github.com/diyan/pywinrm)
- [Pulumi - IaC Tool](https://www.pulumi.com/docs/reference/pkg/python/pulumi/)

