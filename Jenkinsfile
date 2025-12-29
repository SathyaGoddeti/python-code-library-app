node {
  stage('SCM') {
    checkout scm
  }
  stage('CAQ') {
    def scannerHome = tool 'mysonar';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/mysonar"
    }
  }
}
