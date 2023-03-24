node {
  stage('SCM') {
    git 'https://github.com/lorelynbentazal/React-app2.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv('sonarqube') { 
      bat "${scannerHome}/bin/sonar-scanner"
    }
  }
}
