
# Contributing to the MongoDB Get-Started project

First off, thanks for taking the time to contribute! 🎉

The following is a set of guidelines for contributing to the Get-Started projects. These are mostly guidelines, not rules.

## Project Goal

The MongoDB Get-Started project helps set up local development environments to run
applications using [official MongoDB drivers](https://docs.mongodb.com/ecosystem/drivers/) and [MongoDB Cloud products](https://www.mongodb.com/cloud)

Each Get-Started repository includes:
 - instructions on how to install prerequisites
 - working code examples demonstrating some basic CRUD (Create/Retrieve/Update/Delete)
 - links to relevant tutorials and documentation from MongoDB

## Project Structure

### README.md

A `README.md` file to provide information related to the environmentL

  * Description of repository contents 
  * How to run the project in user's local environment
      
      * Prerequisites
      * How to start a Docker image with development prerequisites installed
      
  * Links to relevant MongoDB Blog Quick Start series posts (if any)
  * Links to relevant MongoDB documentation
  * Links to MongoDB Atlas free-tier sign-up

### LICENSE

A `LICENSE` file for Apache License 2.0

### Code Examples

Code examples should include:

  * A working example on how to perform [MongoDB CRUD Operations](https://docs.mongodb.com/manual/crud/).
  * A working example on how to perform [MongoDB Aggregation Pipeline](https://docs.mongodb.com/manual/core/aggregation-pipeline/).

File naming conventions:

  * Script name should be `Getstarted.ext`, `getstarted.ext`, or `get_started.ext` based on language-specific naming conventions.

### Dockerfile

A `Dockerfile` to build a working environment Docker image.

This should:

  * Use Alpine 3.13 (preferred) or Ubuntu 20.04 LTS as base. 
  * Only expose ports that are required by the image
  * Use `/home/${USER}` as the working directory
  * Keep dependencies minimal ( for size )

### Miscellaneous

Use [GitHub Container Registry](https://docs.github.com/en/packages/guides/about-github-container-registry) to store pre-built Docker images. 

## Pull Requests are always welcome

Not sure if that typo is worth a pull request? Found a bug and know how to fix it? Do it! We will appreciate it. 
