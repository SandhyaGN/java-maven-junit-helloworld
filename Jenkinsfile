node{
  def mvnHome= tool name: 'maven-3', type: 'maven'
  stage('Clone the Repo'){
    echo 'Cloning the Repository'
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    echo 'Compiling the Project'
    echo "${mvnHome}"
    shell "${mvnHome}/bin/mvn clean"
    shell "${mvnHome}/bin/mvn compile"
  }
  stage('Run Unit Tests'){
    echo 'Running Unit Tests'
    shell 'xcodebuild -scheme UnitTestRunner -configuration debug || true'
    junit 'http://localhost:8080/job/Blue%20Optima/64/execution/node/3/ws/pom.xml'
    archiveArtifacts artifacts: 'http://localhost:8080/job/Blue%20Optima/64/execution/node/3/ws/pom.xml', followSymlinks: false  
  }
  stage('Coverage Report'){
    echo 'Generate Coverage Report'
    shell 'C:\\Program Files\\apache-maven-3.8.3\\bin\\mvn verify'
  }
  stage('idk'){
    echo 'dik'
    shell 'C:\\Program Files\\apache-maven-3.8.3\\bin\\mvn clean verify'
  }
}
