#!usr/bin/env groovy
@Library('jenkins-shared-library')_

pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                echo "Testing initializing..."
                echo "Testing webhook automation..."
            }
        }

        stage('build') {
            steps {
                echo "Hello Dev! building app...."
                script {
                    buildApp()
                }
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
                script {
                    buildDockerImage('mydockerimage')
                }
            }
        }
    }
}
