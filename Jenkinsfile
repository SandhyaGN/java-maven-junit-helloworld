node{
  // Storing the address of maven in mvnHome
  def mvnHome= tool name: 'maven-3', type: 'maven'
  
  stage('Clone the Repo'){
    echo 'Cloning the Repository'
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  
  stage('Compile Package'){
    echo 'Compiling the Project'
    shell "${mvnHome}/bin/mvn compile"
  }
  
  stage('Run Unit Tests'){
    echo 'Running Unit Tests'
    shell "${mvnHome}/bin/mvn test"
  }
  
  stage('Coverage Report'){
    echo 'Generate Coverage Report'
    shell "${mvnHome}/bin/mvn verify"
  }
  
  stage('Publish Unit Tests'){
    echo 'Publishing Unit Tests'
    shell 'xcodebuild -scheme UnitTestRunner -configuration debug || true'
    junit allowEmptyResults: true, testResults: 'http://localhost:8080/job/Blue%20Optima/64/execution/node/3/ws/pom.xml'
  }
  
  stage('Publish Coverage Report'){
    echo 'Publishing Coverage Report'
    jacoco runAlways: true
  }
}
