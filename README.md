# Notice: Repository Deprecation
This repository is deprecated and no longer actively maintained. It contains outdated code examples or practices that do not align with current MongoDB best practices. While the repository remains accessible for reference purposes, we strongly discourage its use in production environments.
Users should be aware that this repository will not receive any further updates, bug fixes, or security patches. This code may expose you to security vulnerabilities, compatibility issues with current MongoDB versions, and potential performance problems. Any implementation based on this repository is at the user's own risk.
For up-to-date resources, please refer to the [MongoDB Developer Center](https://mongodb.com/developer).


# MongoDB Get-Started README

Repository for meta files related to MongoDB Get-Started development environments.

The MongoDB Get-Started project helps set up local development environments to run
applications using [official MongoDB drivers](https://docs.mongodb.com/ecosystem/drivers/) and [MongoDB Cloud products](https://www.mongodb.com/cloud)

Each Get-Started repository includes:
 - instructions on how to install prerequisites
 - working code examples demonstrating some basic CRUD (Create/Retrieve/Update/Delete)
 - links to relevant tutorials and documentation from MongoDB

## Minimal Requirements 

* [Docker](https://docs.docker.com/) v18.03+ 

## List of Get-Started repositories:

* [get-started-csharp](https://github.com/mongodb-developer/get-started-csharp)
* [get-started-cxx](https://github.com/mongodb-developer/get-started-cxx)
* [get-started-go](https://github.com/mongodb-developer/get-started-go)
* [get-started-java](https://github.com/mongodb-developer/get-started-java)
* [get-started-nodejs](https://github.com/mongodb-developer/get-started-nodejs)
* [get-started-php](https://github.com/mongodb-developer/get-started-php)
* [get-started-ruby](https://github.com/mongodb-developer/get-started-ruby)
* [get-started-scala](https://github.com/mongodb-developer/get-started-scala)
* [get-started-realm-web](https://github.com/mongodb-developer/get-started-realm-web)

## How To Contribute

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contributing guidelines.

## Frequently Asked Questions 

#### 1. How do I modify the sample code ?

If you're using the helper script `get-started.sh` to start the container, then you could just modify the code in the checked out repo location with your preferred editor.

#### 2. How can I connect the example code to MongoDB running on my machine ?

You can connect to a local `mongod` from the `get-started` Docker container by setting `MONGODB_URI` to `mongodb://host.docker.internal:27017/`. Please note that connecting to a replica-set members locally may require changes to the host DNS. 

## Disclaimer

This software is not supported by [MongoDB, Inc](https://www.mongodb.com)
under any of their commercial support subscriptions or otherwise. Any usage is at your own risk.
