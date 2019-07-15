# Simple Spring Boot Web Page
A simple Spring Boot web page that shows how to create a CI/CD pipeline using Azure DevOps.
All tasks for the CI part of the pipeline are defined in the file _**azure-pipelines.yml**_ which can be easily imported in any Azure DevOps project.

As part of the CI/CD pipeline it performs the following tasks:
* Integration with GitHub for automatic triggers when you push to master branch or creates a PR.
* Runs and publishes unit tests.
* Deploys the application into an Azure Web App.
* Integration with Azure Boards, which allows you to automatically close tasks when a PR is approved or a commit is pushed to master branch.

## Pre-requisites
It is assumed that you have access to an Azure Subscription and to an Azure DevOps Project. 

### versions
This project was built and tested using:
* java 11.0.3 2019-04-16 LTS
* Apache Maven 3.6.1
* Spring Boot Framework 2.1.6


## Project Structure
```
.
|-- src
|   |-- main
|   |   |-- java
|   |   |   `-- com
|   |   |       `-- demo
|   |   |           `-- simplespringbootpage
|   |   `-- resources
|   |       |-- static
|   |       `-- templates
|   `-- test
|       `-- java
|           `-- com
|               `-- demo
|                   `-- simplespringbootpage
```
## Usage
To run the tests
```
mvn test
```

To run it locally
```
mvn spring-boot:run
```

To build it
```
mvn clean package
```

## Resources
* Create a Java app in App Service on Linux
    * https://docs.microsoft.com/en-us/azure/app-service/containers/quickstart-java
* Spring Boot Testing:
    * https://stackabuse.com/how-to-test-a-spring-boot-application/
    * https://www.baeldung.com/spring-boot-testing
* Spring Boot in Visual Studio Code
    * https://code.visualstudio.com/docs/java/java-spring-boot
* Deploy an Azure Web App using Azure DevOps
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/targets/webapp
* Using Azure Pipelines to build, test and deploy a Spring Boot and Angular application
    * https://dev.to/azure/using-azure-pipelines-to-build-test-and-deploy-a-spring-boot-and-angular-application-3-7-593j