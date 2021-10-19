node{
  stage('Clone the Repo'){
    git 'https://github.com/SandhyaGN/java-maven-junit-helloworld.git'
  }
  stage('Compile Package'){
    def mvnHome= tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
    -Dorg.jenkinsci.plugins.durabletask.BourneShellScript.LAUNCH_DIAGNOSTICS=true
  }
}
