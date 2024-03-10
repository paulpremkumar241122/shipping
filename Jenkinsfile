pipeline {

    agent { node { label 'workstation' } }
    options {
        ansiColor('xterm')
    }

    stages {

        stage('Code Built') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Unit Test'
//                sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'
            }
        }

        stage('Security Scans') {
            steps {
                echo 'Security Scans'
            }
        }

        stage('Publish Artifact') {
            steps {
                echo 'Publish Artifact'
            }
        }
    }
}
