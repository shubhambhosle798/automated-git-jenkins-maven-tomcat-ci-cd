Started by user jenkins
Obtained jenkinsfile from git https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git
[Pipeline] Start of Pipeline
[Pipeline] node
Running on jenkins-slave in /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
Fetching changes from the remote Git repository
 > /usr/bin/git rev-parse --resolve-git-dir /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/.git # timeout=10
 > /usr/bin/git config remote.origin.url https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git # timeout=10
Fetching upstream changes from https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git
 > /usr/bin/git --version # timeout=10
 > git --version # 'git version 2.40.1'
 > /usr/bin/git fetch --tags --force --progress -- https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision b9436f8d4f7d900f8087fe8177786af11bc3eade (refs/remotes/origin/main)
Commit message: "jenkinsfile"
First time build. Skipping changelog.
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Code checkout)
[Pipeline] git
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
Fetching changes from the remote Git repository
Checking out Revision b9436f8d4f7d900f8087fe8177786af11bc3eade (refs/remotes/origin/main)
Commit message: "jenkinsfile"
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] sh
 > /usr/bin/git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > /usr/bin/git config core.sparsecheckout # timeout=10
 > /usr/bin/git checkout -f b9436f8d4f7d900f8087fe8177786af11bc3eade # timeout=10
+ mvn -Dmaven.test.failure.ignore clean install
 > /usr/bin/git rev-parse --resolve-git-dir /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/.git # timeout=10
 > /usr/bin/git config remote.origin.url https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git # timeout=10
Fetching upstream changes from https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git
 > /usr/bin/git --version # timeout=10
 > git --version # 'git version 2.40.1'
 > /usr/bin/git fetch --tags --force --progress -- https://github.com/shubhambhosle798/git-jenkins-maven-tomcat-ci-cd.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > /usr/bin/git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > /usr/bin/git config core.sparsecheckout # timeout=10
 > /usr/bin/git checkout -f b9436f8d4f7d900f8087fe8177786af11bc3eade # timeout=10
 > /usr/bin/git branch -a -v --no-abbrev # timeout=10
 > /usr/bin/git checkout -b main b9436f8d4f7d900f8087fe8177786af11bc3eade # timeout=10
[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building Demo Maven Webapp 1.0-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ demo ---
[INFO] Deleting /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/target
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ demo ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:compile (default-compile) @ demo ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 1 source file to /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/target/classes
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ demo ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:testCompile (default-testCompile) @ demo ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ demo ---
[INFO] No tests to run.
[INFO] 
[INFO] --- maven-war-plugin:3.3.1:war (default-war) @ demo ---
[INFO] Packaging webapp
[INFO] Assembling webapp [demo] in [/home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/target/demo]
[INFO] Processing war project
[INFO] Copying webapp resources [/home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/src/main/webapp]
[INFO] Building war: /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/target/demo.war
[INFO] 
[INFO] --- maven-install-plugin:2.4:install (default-install) @ demo ---
[INFO] Installing /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/target/demo.war to /home/ec2-user/.m2/repository/com/domain/demo/1.0-SNAPSHOT/demo-1.0-SNAPSHOT.war
[INFO] Installing /home/ec2-user/workspace/jenkins-maven-tomcat-test-pipeline/pom.xml to /home/ec2-user/.m2/repository/com/domain/demo/1.0-SNAPSHOT/demo-1.0-SNAPSHOT.pom
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 2.681 s
[INFO] Finished at: 2024-06-10T10:50:50+00:00
[INFO] Final Memory: 15M/57M
[INFO] ------------------------------------------------------------------------
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Deploy)
[Pipeline] deploy
[DeployPublisher][INFO] Attempting to deploy 1 war file(s)
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS