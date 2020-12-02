# MongoDB Get-Started README

Repository for meta files related to MongoDB Get-Started development environments.

The MongoDB Get-Started project helps set up local development environments to run
applications using [official MongoDB drivers](https://docs.mongodb.com/ecosystem/drivers/).

Each Get-Started repository includes:
 - instructions on how to install prerequisites
 - working code examples demonstrating some basic CRUD (Create/Retrieve/Update/Delete)
   and aggregation commands.
 - links to relevant tutorials and documentation from MongoDB

## Minimal Requirements 

* [Docker](https://docs.docker.com/) v18.03+ 

## List of Get-Started repositories:

* [get-started-csharp](https://github.com/mongodb-developer/get-started-csharp)
* [get-started-go](https://github.com/mongodb-developer/get-started-go)
* [get-started-java](https://github.com/mongodb-developer/get-started-java)
* [get-started-nodejs](https://github.com/mongodb-developer/get-started-nodejs)
* [get-started-scala](https://github.com/mongodb-developer/get-started-scala)
* [get-started-cxx](https://github.com/mongodb-developer/get-started-cxx)

## How To Contribute 

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contributing guidelines.

## Frequently Asked Questions 

#### 1. How do I modify the sample code ?

Generally there are two ways to modify the sample code:

  * Modify the code within the Docker container. Before the execution of the code sample, you could alter the script using built-in editor (i.e. nano/vim). **Please note** that any modification inside of the container will be lost when the container is terminated. The Docker container is more of an ephemeral environment. 

  * Mount the host filesystem into the Docker container as a volume (see [Use Bind Mounts](https://docs.docker.com/storage/bind-mounts/)). For example in macOS, when launching the container you can include `-v /mypath:/myvolume` to make `/mypath` from the host available in the container as `/myvolume`. Any files created/modified in `/mypath` will persists even after the container is terminated. 


#### 2. How can I connect the example code to MongoDB running on my machine ?

You can connect to a local `mongod` from the `get-started` Docker container by setting `MONGODB_URI` to `mongodb://host.docker.internal:27017/`. 


