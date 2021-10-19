node{
  stage('Clone the Repo'){
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    def mvnHome= tool name: 'maven-3', type: 'maven'
    shell "${mvnHome}/bin/mvn package"
  }
}
