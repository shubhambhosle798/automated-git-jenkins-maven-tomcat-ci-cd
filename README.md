# git-jenkins-maven-tomcat-ci/cd

Hello
In this project, I have demonstrated scalable and automated CI/CD pipeline of Git, Jenkins, Maven and Tomcat to deploy java web application.
Used both Declarative Pipeline setup & Freestyle setup for deployment.

Steps
1. Create the repository in GitHub
2. Clone your repository in local machine.
3. Push your project file from local machine to GitHub repository
4. Create 3 Servers - Jenkins Master, Jenkins Agent, Tomcat. (Servers can be scalable according to your need)
5. In Jenkins Master, install jdk and Jenkins
6. In Jenkins Agent, install jdk, Jenkins, Git and Maven
7. In Tomcat server, install jdk and Tomcat
8. Start the Jenkins service on Jenkins Master and Tomcat on Tomcat server
9. Configure the Tomcat Manager in 'tomcat-users.xml' file
10. Hit public iP of Jenkins Master server in webpage and configure Jenkins
11. After configuring, add a node of Jenkins Agent
12. After adding, check if Agent is online.
13. Download 'Maven Integration plugin' and 'Git Integration Plugin', so the respective commands can run
14. Also download 'Deploy To Container Plugin', so that your war file can be uploaded to your Tomcat server
15. Configure the jdk, Git and Maven plugins in Tools configuration
16. Create the Declarative Pipeline job or Freestyle job
17. Provide GitHub Repository and Add the Branch
18. Setup the war where you add Tomcat's iP address
19. Add a Script Path (eg. jenkinsfile where deployment stages are written)
20. Tap Build Now
21. Check the deployment on Tomcat server in Manager App.
22. To make this whole ci/cd automated, Enable the Poll SCM and * * * * * in schedule. Also enable 'Build whenever a SNAPSHOT dependency is built'

Thankyou
