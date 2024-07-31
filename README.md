# Automated Git-Jenkins-Maven-Tomcat CI/CD

This project demonstrates a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline using Git, Jenkins, Maven, and Tomcat. The repository includes sample Java code, a Jenkinsfile for pipeline configuration, and necessary project files to build and deploy a Java web application.

## Project Structure

- **src/**: Contains the source code for the Java application.
  - **main/java/Hello.java**: Sample Java class.
  - **main/webapp/index.jsp**: JSP file for the web application.
  - **main/webapp/WEB-INF/web.xml**: Web deployment descriptor.
- **test/**: This is created to test automation of CI/CD.
- **jenkinsfile**: Jenkins pipeline configuration file.
- **pom.xml**: Maven Project Object Model file for managing project dependencies and build configuration.
- **README.md**: Project documentation.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- Git
- Jenkins
- Maven
- Tomcat

## Getting Started

Follow these steps to set up and run the CI/CD pipeline:

### Clone the Repository

```bash
git clone https://github.com/shubhambhosle798/automated-git-jenkins-maven-tomcat-ci-cd.git
cd automated-git-jenkins-maven-tomcat-ci-cd
```

### Configure Jenkins

1. **Install Jenkins**: If Jenkins is not already installed, download and install it from Jenkins official site.
2. **Install Plugins**: Ensure the following Jenkins plugins are installed:
   - Git Plugin
   - Maven Integration Plugin
   - Deploy to Container Plugin

## Set Up Jenkins Job
1. **Build the Project**: Trigger the Jenkins job to build the project using Maven. This will compile the code, run tests, and package the application into a WAR file.
2. **Pipeline Configuration**: Use the 'jenkinsfile' from this repository to configure the pipeline script.
3. **Set Up Git Repository**: In the Source Code Management section, configure the Git repository URL and credentials.

## Build and Deploy
1. **Build the Project**: Trigger the Jenkins job to build the project using Maven. This will compile the code, run tests, and package the application into a WAR file.
2. **Deploy to Tomcat**: After a successful build, the pipeline will deploy the WAR file to the Tomcat server.

## Usage
- **Access the Application**: Once deployed, you can access the application through your Tomcat server URL, typically 'http://localhost:8080/your-app-name'.
- **Pipeline Stages**: The Jenkins pipeline includes the following stages:
  - Checkout: Retrieves the latest code from the Git repository.
  - Build: Compiles the Java code and packages it into a WAR file using Maven.
  - Test: Runs any test.
  - Deploy: Deploys the WAR file to the Tomcat server.
 
## Acknowledgments
Thanks to the Jenkins and Maven communities for their extensive documentation and support.

## Contact
For any questions or feedback, please reach out to bhosleshubham798@gmail.com or open an issue in the repository.

## Thank you for visiting this project repository!
