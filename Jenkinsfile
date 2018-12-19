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
       sh  'scp -o StrictHostKeyChecking=no  target/*.war ec2-user@ec2-13-126-251-77.ap-south-1.compute.amazonaws.com:/opt/apache-tomcat-9.0.13/webapps/'
}
        }
        }
