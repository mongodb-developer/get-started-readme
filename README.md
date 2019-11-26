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

## How To Contribute 

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contributing guidelines.

## Frequently Asked Questions 

1. How do I modify the sample code ?

Generally there are two ways to modify the sample code:

  * Modify the code within the Docker container. Before the execution of the code sample, you could alter the script using built-in editor (i.e. nano/vim). *Please note* that any modification inside of the container will be wiped when the container is terminated. 
  * Mount the host filesystem into the Docker container as a volume (see [Use Bind Mounts](https://docs.docker.com/storage/bind-mounts/)). For example in macOS, when launching the container you can include `-v /mypath:/myvolume` to make `/mypath` from the host available in the container as `/myvolume`.


2. How can I connect the example code to MongoDB running on my machine ?

If you choose to run a local `mongod` on your machine (the Docker host), you can connect to it from the `get-started` Docker container by setting `MONGODB_URL` to `mongodb://host.docker.internal:27017/`. 

