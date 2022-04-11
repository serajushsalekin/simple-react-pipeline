pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                echo "Testing initializing..."
                sh "docker --version"
            }
        }

        stage('build') {
            steps {
                echo "Hello Dev! building app...."
            }
        }

        stage('deploy') {
            when {
                expression {
                    BRANCH_NAME == "master"
                }
            }
            steps {
                echo "Deploying...."
            }
        }
    }
}
