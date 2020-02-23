# OpenSSL Certificate Authorities

## Overview

OpenSSL is a standard in most places for encryption and verification of cryptography
that people use in most of their lives and may not know it. This is an example
of how to setup an OpenSSL Certificate Authority both a Root and Intermediate.
This is mostly to show how big organizations do what they do in a verify simplified
manner, but it can still be done with this setup. You could also use this setup
for a personal VPN or in small software distributions. You can also use this to
perform very strict TLS/SSL operations inside of a cluster.

For this project, I chose to wrap the commands for OpenSSL inside of a `Taskfile.yml`
which uses [GitHub: go-task/task](https://github.com/go-task/task) to automate
these commands. They still require some input, but the OpenSSL configurations and
OpenSSL commands could be configured to take a password file to both lock and
unlock the RSA keys and also fill in default Certificate values for verification.

## Requirements

* Linux/MacOS Operating Systems.
    * Sorry Windows. You just suck.
* OpenSSL
* go-task

## Setup

Simply clone the repository to your local machine and execute `task`.

## Usage

Use the `task` command to see the available tasks. Simply follow the order of 
tasks.

```bash
task --list
```

## Development and Testing

When performing development or testing this repository, make sure to create a new branch
based off of develop, similar to that of GitFlow. This will protect the main branches
and also allow you to create and test it out.

## References

* [JamieLinux OpenSSL Certificate Authority](https://jamielinux.com/docs/openssl-certificate-authority/index.html)
* [Create Multi-Domain Certificates](https://apfelboymchen.net/gnu/notes/openssl%20multidomain%20with%20config%20files.html)
* [GitHub: go-task/task](https://taskfile.dev/)