node{
  stage('Clone the Repo'){
    echo 'Cloning the Repository'
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    echo 'Compiling the Project'
    def mvnHome= tool name: 'maven-3', type: 'maven'
    shell "${mvnHome}/bin/mvn package"
  }
}
