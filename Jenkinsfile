node {
stage('SCM CheckOut')
git 'https://github.com/yugan6669/maven-web-application.git'
}
stage('Compile-Package'){
//Get maven home path
def MNV_HOME = tool name: 'MAVEN_HOME', type:maven
sh "{MVN_HOME}/bin/mvn packaage"
}
}
