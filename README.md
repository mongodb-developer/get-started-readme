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
* [get-started-cxx](https://github.com/mongodb-developer/get-started-cxx)
* [get-started-go](https://github.com/mongodb-developer/get-started-go)
* [get-started-java](https://github.com/mongodb-developer/get-started-java)
* [get-started-nodejs](https://github.com/mongodb-developer/get-started-nodejs)
* [get-started-scala](https://github.com/mongodb-developer/get-started-scala)

## How To Contribute

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contributing guidelines.

## Frequently Asked Questions 

#### 1. How do I modify the sample code ?

If you're using the helper script `get-started.sh` to start the container, then you could just modify the code in the checked out repo location with your preferred editor.

If you are not using the helper script, generally there are two ways to modify the sample code:

  * Modify the code within the Docker container. Before the execution of the code sample, you could alter the script using built-in editor (i.e. nano/vim). **Please note** that any modification inside of the container will be lost when the container is terminated. The Docker container is more of an ephemeral environment. 

  * Mount the host filesystem into the Docker container as a volume (see [Use Bind Mounts](https://docs.docker.com/storage/bind-mounts/)). For example in macOS, when launching the container you can include `-v /mypath:/myvolume` to make `/mypath` from the host available in the container as `/myvolume`. Any files created/modified in `/mypath` will persists even after the container is terminated. 


#### 2. How can I connect the example code to MongoDB running on my machine ?

You can connect to a local `mongod` from the `get-started` Docker container by setting `MONGODB_URI` to `mongodb://host.docker.internal:27017/`. 

## Alternative Method 

### Visual Studio Code - Remote 

Only the following repositories are available with VSCode - Remote: 

* [get-started-go](https://github.com/mongodb-developer/get-started-go)

If you are familiar with VSCode, you could build using [Visual Studio Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview).

Pre-requisite: Install [Microsoft VS Code Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

#### Steps 

1. Git clone a Get-Started repository i.e. `get-started-go`

2. In the root directory level of the repository you should find `./config.env`. Use an editor to open the file, and: 
   * Specify `MONGODB_URI` value
   * (Optional) Specify `DRIVER_VERSION` value to use a different driver version than the default

3. With VS Code editor open, press `Cmd+Shift+P` to bring up the `Command Palette` and type in `open folder` and choose `Remote-Containers: Open Folder in Container...`

4. You should see a progress bar while VS Code is building the Docker image

#### Execution Steps

Once the build completed, choose `Run` menu then choose `Run Without Debugging` (default `Ctrl + F5`) to execute the code

See [VS Code Remote: FAQ](https://code.visualstudio.com/docs/remote/faq) for more information. 
