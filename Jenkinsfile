pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage("build") {
            steps {
                script {
                    sh 'python --version'
                }
            }
        }
        stage("test") {
            when {
                expression {
                    BRANCH_NAME == 'bbb'
                }
            }
            steps {
                script {
                  echo "Testing the application..."
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                   echo "Deploying the application..."
                }
            }
        }
    }
}
