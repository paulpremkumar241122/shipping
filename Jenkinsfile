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
                sh 'sudo sonar-scanner -Dsonar.host.url=http://172.31.14.184:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=shipping -Dsonar.java.binaries=target'
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
