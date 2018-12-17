node {
  stage('SCM CheckOut') {
git 'https://github.com/yugan6669/maven-web-application.git'
    

}
stage('Compile-Package'){
//Get maven home path
def mvnHOME = tool name: 'MAVEN_HOME', type: 'maven'

sh "${mvnHOME}/bin/mvn package"
}
  stage('Deploy-Tomcat'){
       sshagent(['tomcat-pl']) {
       sh 'scp -o StrictHostKeyChecking=no  target/*.war root@172.31.17.187:/home/ec2-user/apache-tomcat-9.0.13/webapps/'
}
        }
        }
