pipeline {
    parameters{
        string(name:'GIT_REPO_APP',
               defaultValue:
               'https://github.com/PabloGalegoC/spring-boot-maven-angular-starter.git')
        string(name:'APP_GIT_BRANCH',
               defaultValue: "**")
        string(name:'GIT_USER',
               defaultValue:"losete")   
    }
    agent {
        docker {
            image 'maven:3.6.0-jdk-11'
        }
    }
    stages {
        stage('Setup') {
            steps {
                git branch: "${params.APP_GIT_BRANCH}",
                    credentialsId: "${params.GIT_USER}",
                    url: "${params.GIT_REPO_APP}"
                sh 'mkdir reports' 
                sh 'ls -la' 
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
