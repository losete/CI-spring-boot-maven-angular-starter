pipeline {
    agent {
        docker {
            image 'maven:3.6.0-jdk-11'
        }
    }
    stages {
        stage('Setup') {
            steps {
                echo 'Setup'
            }
        }
        stage('Validate') {
            steps {
                echo 'Validate'
            }
        }
        stage('Compile') {
            steps {
                echo 'Compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        always {
            echo 'always'
        }
        failure {
            echo 'failure'
        }
        cleanup{
            cleanWs()
        }
    }
}
