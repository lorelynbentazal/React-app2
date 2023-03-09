pipeline {
    agent any
    stages {
        stage('SAST') {
            environment {
                SCANNER_HOME = tool 'SonarScanner'
            }
            steps {
                withSonarQubeEnv('sonarqube') {
                    sh" ${SCANNER_HOME}}/bin/sonar-scanner \
                    -Dsonar.projectKey=Jenkins \
                    -Dsonar.sources=. "
                }
            }
        }
    }
 }
