node{
  stage('Clone the Repo'){
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    def mvnHome= tool name: 'maven', type: 'maven'
    sh "${mvnHome}\bin\mvn package"
  }
}
