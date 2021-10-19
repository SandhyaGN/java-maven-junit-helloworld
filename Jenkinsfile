node{
  stage('Clone the Repo'){
    echo 'Cloning the Repository'
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    echo 'Compiling the Project'
    def mvnHome= tool name: 'maven-3', type: 'maven'
    echo '${mvnHome}'
//     sh "${mvnHome}/bin/mvn package"
  }
  stage('Run Unit Tests'){
    echo 'Running Unit Tests'
    def mvnHome= tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn test"
  }
  stage('Coverage Report'){
    echo 'Generate Coverage Report'
    def mvnHome= tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn verify"
  }
  stage('idk'){
    echo 'dik'
    def mvnHome= tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn clean verify"
  }
}
