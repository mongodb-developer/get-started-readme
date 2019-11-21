
# Contributing to the Get-Started project 

First off, thanks for taking the time to contribute! 🎉

The following is a set of guidelines for contributing to the Get-Started projects. These are mostly guidelines, not rules.

## Project Structure

### README.md

A `README.md` file to provide information related to the environment. Should include: 

  * Description of repository contents 
  * How to run the project in user's local environment
      
      * Prerequisites       
      * How to start a Docker image with development prerequisites installed
      
  * Links to relevant MongoDB Blog Quick Start series posts (if any)
  * Links to relevant MongoDB driver reference documentation 
  * Links to MongoDB Atlas free-tier sign-up 

### LICENSE 

A `LICENSE` file for Apache License 2.0 

### Code Examples

Code examples should include: 

  * A working example on how to perform [MongoDB CRUD Operations](https://docs.mongodb.com/manual/crud/)
  * A working example on how to perform [MongoDB Aggregation Pipeline](https://docs.mongodb.com/manual/core/aggregation-pipeline/)

Code examples naming convention: 

  * Script name should either be: `Getstarted.ext`, `getstarted.ext` or `get_started.ext` based on language specific file convention. 

### Dockerfile 

A `Dockerfile` to build a working environment Docker image. Should: 

  * Use Ubuntu 18.04 LTS as base
  * Only expose ports that are required by the image
  * Default working directory should be `/home/ubuntu`
  * Keep dependencies minimal ( for size ) 
  * Expose a build `ARG` called `DRIVER_VERSION` to allow an easy way to change the driver version

### Miscellaneous 

For consistency, the Docker environment should have `nano` simple editor installed. 

## Pull Requests are always welcome

Not sure if that typo is worth a pull request? Found a bug and know how to fix it? Do it! We will appreciate it. 
