node {
  stage('SCM') {
    git 'https://github.com/lorelynbentazal/React-app2.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name
      bat "${scannerHome}/bin/sonar-scanner"
    }
  }
}
