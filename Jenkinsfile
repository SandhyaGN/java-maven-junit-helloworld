node{
  def mvnHome= tool name: 'maven-3', type: 'maven'
  stage('Clone the Repo'){
    echo 'Cloning the Repository'
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    echo 'Compiling the Project'
    echo "${mvnHome}"
    sh '"${mvnHome}/bin/mvn" package'
  }
  stage('Run Unit Tests'){
    echo 'Running Unit Tests'
    sh 'C:\\Program Files\\apache-maven-3.8.3\\bin\\mvn test'
  }
  stage('Coverage Report'){
    echo 'Generate Coverage Report'
    sh 'C:\\Program Files\\apache-maven-3.8.3\\bin\\mvn verify'
  }
  stage('idk'){
    echo 'dik'
    sh 'C:\\Program Files\\apache-maven-3.8.3\\bin\\mvn clean verify'
  }
}
