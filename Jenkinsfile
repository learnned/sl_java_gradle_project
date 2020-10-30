pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }
    stages {
        stage('Run Pipeline') {
            parallel {
                stage('Release') {
                    steps {
                        load 'jenkins/Jenkinsfile'
                    }
                }
            }
        }
    }
}